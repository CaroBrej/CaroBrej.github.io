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
  </div>
</template>

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
