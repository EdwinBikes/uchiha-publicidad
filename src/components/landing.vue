<template>
    <div class="container__body">
        <div class="container__landing">
            <div class="container__landing--title">
                <div class="container__landing--title__contain">
                    <h2>¿QUIÉNES SOMOS?</h2>
                </div>
                
            </div>
            <div class="container__landing--text">
                <div class="container__landing--text__image">
                    <!-- <img :src="require('../assets/images/logobody.png')" alt=""> -->
                </div>
                <div class="container__landing--text__p">
                    <p>
                        GRUPO DESCA S.A.S., somos una empresa
                        que presta servicios de asesoría y consultoría
                        para las empresas en el diseño e implementación
                        del Sistema de Gestión de Seguridad y Salud
                        en el Trabajo, realizamos acompañamiento
                        con profesionales con conocimiento y
                        experiencia en prevención y control
                        de riesgos laborales.
                    </p>
                </div>
            </div>
        </div>
    </div>
</template>
<style scoped>
.container__body{
    width: 100%;
    height: 100%;
}
.container__landing{
    display: grid;
    grid-template-rows: repeat(2,1fr);
}
.container__landing--title{
    /* background-image: url('https://images.pexels.com/photos/2760242/pexels-photo-2760242.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940'); */
    background-size: cover;
    background-repeat: no-repeat;
   
}
.container__landing--title__contain{
    height: 50px;
    margin-top: 30vh;
    background-color: rgba(0, 13, 50,0.7);
    display: flex;
    justify-content: center;
    align-items: center;
    color:white;
}
.container__landing--text{
    display: grid;
    grid-template-columns: repeat(2,1fr);
}
.container__landing--text__image{
    display: flex;
    justify-content: center;
    align-items: center;
}
.container__landing--text__p{
    display: flex;
    justify-content: center;
    align-items: center;
    margin:0 60px;
}
.container__landing--text__p p{
    text-align: justify;
}
@media (max-width: 850px) {
    .container__landing--text{
        grid-template-columns: 1fr;

    }
    .container__body{
        height: 1200px;
    }
    .container__landing--title{
        height: 500px;
    }
    .container__landing--text__image img{
        width: 100%;
    }
}
@media (max-width: 850px) and (orientation: landscape){
    .container__landing--text{
        grid-template-columns: 1fr;

    }
    .container__body{
        height: 100%;
    }
    .container__landing--title{
        height: 500px;
    }
    .container__landing--text__image img{
        width: 100%;
    }
}
</style>