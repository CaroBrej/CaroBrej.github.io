<template>
  <div class="container">
    <div class="maincontent">
      <div>
        <img class="gimg" alt="grzybek" src="../assets/grzybek.png" />
      </div>
      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed vestibulum
      nibh et nulla aliquet efficitur. Donec quis aliquam purus. Curabitur
      maximus ullamcorper orci, sed mollis orci fermentum sit amet. Vivamus
      tempor odio id ligula facilisis, quis imperdiet dolor bibendum. Curabitur
      ultricies malesuada lobortis. Interdum et malesuada fames ac ante ipsum
      primis in faucibus. Quisque rutrum, lacus faucibus maximus semper, odio
      metus scelerisque orci, ac laoreet lacus erat commodo dolor. Maecenas non
      augue pellentesque, varius augue vitae, gravida mauris. Sed molestie elit
      at semper dapibus. Phasellus aliquet purus vel metus vulputate, a sodales
      sem bibendum. Morbi vel dolor sed est hendrerit ultrices id et nulla. Orci
      varius natoque penatibus et magnis dis parturient montes, nascetur
      ridiculus mus. Fusce id est ligula. Pellentesque elit lacus, tincidunt id
      quam ut, ultricies vulputate leo. Cras id urna pharetra dolor viverra
      tristique. Sed in nisi feugiat, iaculis dolor eu, lacinia mauris. Sed
      auctor elit massa, et bibendum diam pharetra vel. Nam hendrerit, est ac
      consectetur vulputate, mauris nulla tristique nunc, et vestibulum erat
      dolor et mi. Duis vestibulum turpis et ligula dictum, id commodo leo
      fringilla. Sed placerat aliquet dolor. Sed lectus quam, sagittis in varius
      non, condimentum non nunc. Integer ut lorem venenatis, pretium sem vel,
      dapibus risus. Morbi neque lectus, elementum at magna sit amet, auctor
      tempor sapien. Suspendisse dapibus ex vitae augue tristique, ut venenatis
      lacus cursus. Cras mattis vitae diam in faucibus. Morbi commodo porta
      faucibus. Praesent a laoreet dui, ac finibus orci. Maecenas vel mi eget
      ligula ornare sollicitudin nec et nisl. Nam fermentum quam a enim
      hendrerit, vitae lacinia risus semper. Fusce imperdiet augue sed suscipit
      egestas. In hac habitasse platea dictumst. Integer blandit enim mauris, in
      placerat massa fringilla id. Praesent egestas euismod sem non
      sollicitudin. Phasellus faucibus sodales mauris semper mollis. Curabitur
      nunc est, volutpat quis mattis eget, commodo ut nisi. Cras purus erat,
      ultrices et porttitor id, bibendum vitae mauris. Integer quis enim lorem.
      Praesent lobortis pulvinar sem, ut egestas nisl luctus sollicitudin. Nunc
      a leo non eros bibendum pharetra dapibus sit amet quam. Lorem ipsum dolor
      sit amet, consectetur adipiscing elit. Aliquam venenatis maximus erat non
      posuere. Donec tempor, eros id congue aliquam, ex tortor luctus ante,
      vitae pulvinar sapien leo vitae sem. Cras aliquet vitae neque ac blandit.
      Donec vel arcu tristique, sollicitudin arcu nec, dignissim turpis. Cras
      lacinia vitae turpis vitae congue. Maecenas ultrices, felis quis feugiat
      aliquam, eros purus vehicula lorem, laoreet dapibus sem orci et velit.
      Duis mattis semper dignissim. Ut elementum vulputate nunc, id egestas diam
      laoreet eget. Orci varius natoque penatibus et magnis dis parturient
      montes, nascetur ridiculus mus. Pellentesque facilisis neque sit amet nisl
      bibendum scelerisque. Nam hendrerit justo sed fermentum fringilla. Proin
      porta elit a euismod rhoncus. Donec orci erat, vehicula eu sodales nec,
      mattis eu tortor.
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
.container {
  background-color: antiquewhite;
  min-height: 100vh;
  height: 100%;
  width: 100%;
}
.gimg {
  width: 30%;
  float: right;
  margin-right: 20px;
}
.maincontent {
  margin-left: 10px;
  margin-top: 20px;
  width: 100%;
  font-size: 1.5rem;
}
@media (max-width: 640px) {
  .gimg {
    width: 50%;
    float: right;
    margin-right: 20px;
  }
  .maincontent {
    margin-left: 10px;
    margin-top: 20px;
    width: 100%;
    font-size: 1rem;
  }
}
</style>
