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
  height: 500px;
}

.container__mision--text,
.container__mision--img {
  height: 500px;
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
}

.container__mision--text {
  color: white;
  text-align: center;
  padding: 20px; /* Añade espaciado interno para separar del contenedor padre */
}

.container__mision--img {
  display: flex;
  align-items: center;
  margin: 20px; /* Añade márgenes externos para separar del contenedor padre */
}

.container__mision--text h2 {
  font-size: 30px;
}

.container__mision--text p {
  font-size: 25px;
}

.container__mision--img img {
  height: 90%;
  width: 90%;
  object-fit: contain;
}

@media (max-width: 850px) {
  .container__mision {
    display: grid;
    grid-template-columns: 1fr;
    height: auto;
  }

  .container__mision--img,
  .container__mision--text {
    width: 90vw;
    height: auto;
    padding: 20px;
    margin: 20px auto;
  }

  .container__mision--text p {
    width: 90%; /* Ajusta el ancho del párrafo para que sea más ancho en pantallas pequeñas */
    font-size: 20px; /* Ajusta el tamaño de fuente según sea necesario */
  }
}
</style>
