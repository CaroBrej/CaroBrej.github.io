<template>
  <div class="about">
    <h1>Witaj tutaj napisze troche jak jest zrobiona ta strona</h1>
    <div class="content">
      Strona jest napisana przy pomocy Vue 3 jest to framework dla wspiera on
      zarówno js jak i ts a ja dopiero uczę się z nigo korzystać tak więc jeśli
      przypadkiem trafiłeś na tą stronę to proszę o wyrozumiałość.
    </div>
    <div class="content">
      Strona Home posiada zwyczajny layout z zawijanym tekstem za obrazkiem
    </div>
    <div class="content">
      Tutaj będzie przykłąd użycia web API które to pozwoli nam na zrobinie
      prostej operacji dodawania, odejmowania, mnożenia i dzielenia liczb
      całkowitych
    </div>
    <div class="content">Liczba1: <input v-model="number1" /></div>
    <div class="content">Liczba2: <input v-model="number2" /></div>
    <div class="content">wybierz operator</div>
    <div class="content">
      <input type="radio" id="+" value="+" v-model="operator" />
      <label for="+"> dodaj </label>
      <input type="radio" id="-" value="-" v-model="operator" />
      <label for="-"> odejmij </label>
      <input type="radio" id="*" value="*" v-model="operator" />
      <label for="*"> pomnóż </label>
      <input type="radio" id="divide" value="divide" v-model="operator" />
      <label for="divide"> podziel </label>
    </div>
    <div class="content">Twój wynik to: {{ result }}</div>
    <div class="content">{{ validationmessege }}</div>
    <div class="content"><button @click="GetResult">Policz</button></div>
  </div>
</template>

<script>
import axios from "axios";
export default {
  data() {
    return {
      number1: "",
      number2: "",
      operator: "+",
      result: "0",
      validationmessege: "",
    };
  },
  methods: {
    Checkvalidation() {
      if (!this.number1 || !this.number2) {
        this.validationmessege = "Trzeba podać dane";
        return false;
      }
      const regex = /^([-]?[1-9]\d*|0)$/;
      if (
        !regex.test(this.number1) ||
        !regex.test(this.number2) ||
        (this.number2 == 0 && this.operator == "divide")
      ) {
        this.validationmessege = "błędne dane";
        return false;
      }
      this.validationmessege = "";
      return true;
    },
    GetResult() {
      if (!this.Checkvalidation()) {
        this.result = "0";
        return;
      }
      const url =
        "https://pwiapi4.azurewebsites.net/calculator/" +
        this.number1 +
        "," +
        this.number2 +
        "," +
        this.operator;
      console.log(url);
      axios
        .get(url)
        .then((response) => {
          this.result = response.data.result;
        })
        .catch(() => {
          this.result = "0";
          this.validationmessege = "coś poszło nie tak";
        });
    },
  },
};
</script>

<style>
h1 {
  display: flex;
  text-align: center;
  justify-content: center;
}

.content {
  margin-top: 20px;
  margin-left: 20px;
  font-size: 1.5rem;
}
@media (max-width: 640px) {
  .content {
    margin-top: 20px;
    margin-left: 20px;
    font-size: 1rem;
  }

  h1 {
    display: flex;
    text-align: center;
    justify-content: center;
    font-size: 1.5rem;
  }
}
</style>
