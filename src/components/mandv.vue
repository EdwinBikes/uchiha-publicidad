<template>
  <div class="container__mision">
    <div class="container__mision--text">
      <h2>Misión</h2>
      <p>
        Nuestra misión es simple pero poderosa: colaborarte para alcanzar tus
        objetivos digitales con éxito. Creemos que cada cliente es único y, por
        lo tanto, cada solución que ofrecemos es personalizada y adaptada a tus
        necesidades específicas. Nos esforzamos por ser tu socio de confianza en
        el espacio digital, ofreciendo servicios que te permitan destacar y
        crecer en línea.
      </p>
    </div>
    <div class="container__mision--img">
      <img
        src="https://images.pexels.com/photos/6483623/pexels-photo-6483623.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1"
        alt=""
      />
    </div>
  </div>
</template>
<style scoped>
.container__mision {
  display: flex;
  justify-content: space-around;
  align-items: center;
  height: auto; /* Cambia la altura a "auto" para que se ajuste automáticamente */
}

.container__mision--text,
.container__mision--img {
  width: 45vw;
  background: linear-gradient(
    to bottom,
    #f600fe,
    #c900fe,
    #a136ff,
    #5142f0,
    #0033d9
  );
  box-shadow: 4px 4px 2px 2px rgba(0, 0, 0, 0.7);
  border-radius: 6px;
  display: flex;
  justify-content: center;
  flex-direction: column;
  margin: 20px 0; /* Reduce el margen superior e inferior */
}

.container__mision--text {
  color: white;
  text-align: center;
  padding: 20px; /* Añade espaciado interno para separar del contenedor padre */
}

.container__mision--img {
  display: flex;
  align-items: center;
  padding: 30px;
  margin: 20px 0; /* Reduce el margen superior e inferior */
}

.container__mision--text h2 {
  font-size: 30px;
}

.container__mision--text p {
  font-size: 25px;
  width: 70%; /* Ajusta el ancho del párrafo en pantallas grandes */
  margin: 0 auto; /* Centra el párrafo horizontalmente */
}

.container__mision--img img {
  max-height: 100%; /* Utiliza "max-height" en lugar de "height" para que se ajuste automáticamente */
  max-width: 100%; /* Utiliza "max-width" en lugar de "width" para que se ajuste automáticamente */
  object-fit: contain;
}

@media (max-width: 850px) {
  .container__mision {
    display: grid;
    grid-template-columns: 1fr;
    margin: 20px auto; /* Agrega margen para centrar en pantallas pequeñas */
  }

  .container__mision--img {
    width: 90vw;
    height: auto;
    padding-top: 10px;
    padding-bottom: 10px;
    margin: 20px auto;
  }

  .container__mision--text {
    width: 90vw;
    padding: 20px;
  }

  .container__mision--text p {
    width: 90%; /* Ajusta el ancho del párrafo para que sea más ancho en pantallas pequeñas */
    font-size: 20px; /* Ajusta el tamaño de fuente según sea necesario */
  }
}
</style>
