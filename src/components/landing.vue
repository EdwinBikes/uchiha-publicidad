<template>
  <div class="container__body">
    <div class="container__landing">
      <div class="container__landing--title">
        <div class="container__landing--title__contain">
          <h2>Uchiha publicidad</h2>
          <p>
            Estamos comprometidos a transformar tu visión en realidad. Somos una
            agencia de soluciones digitales que se especializa en impulsar tu
            presencia en línea y ofrecer servicios de desarrollo web y
            aplicaciones móviles de alta calidad. Nuestro enfoque es simple: tu
            éxito es nuestro éxito. Trabajamos de cerca contigo para alcanzar tus
            metas y objetivos en el mundo digital.
          </p>
        </div>
      </div>
    </div>
    <Mision />
  </div>
</template>
<style scoped>
.container__body {
  margin-top: 90px;
  width: 100%;
  height: 100%;
}
.container__landing {
  display: grid;
  grid-template-rows: 1fr;
}
.container__landing--title {
  background-image: url('https://images.pexels.com/photos/6476563/pexels-photo-6476563.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1');
  background-size: cover;
  background-repeat: no-repeat;
  width: 100vw;
  height: 700px;
}
.container__landing--title__contain {
  height: 200px;
  margin-top: 30vh;
  background-color: rgba(40, 40, 42, 0.7);
  display: flex;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
  color: white;
  font-size: 20px;
  max-width: 80%; /* Ajusta el ancho máximo del contenedor */
}

.container__landing--title__contain h2 {
  width: 100%;
  text-align: center;
  font-size: 30px;
  padding: 0;
  margin: 0;
}

.container__landing--title__contain p {
  width: 100%; /* Ajusta el ancho del párrafo al 100% */
  text-align: justify;
  padding: 0;
  margin: 0;
}

@media (max-width: 850px) {
  .container__landing--title__contain {
    max-width: 90%; 
  }
  .container__body {
    height: 1650px;
  }
  .container__landing--title {
    height: 800px;
  }
  .container__landing--title__contain {
    height: 550px;
    background-color: rgba(40, 40, 42, 0.8);
  }
  .container__landing--text__image img {
    width: 100%;
  }
}

@media (max-width: 850px) and (orientation: landscape) {
  .container__landing--title__contain {
    max-width: 90%;
  }
  .container__landing--text {
    grid-template-columns: 1fr;
  }
  .container__body {
    height: 100%;
  }
  .container__landing--title {
    height: 500px;
  }
  .container__landing--text__image img {
    width: 100%;
  }
}
</style>
