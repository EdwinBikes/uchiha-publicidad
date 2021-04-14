<template>
    <div class="container__body">
        <div class="container__service">
            <div class="container__service--img">
                <!-- <img :src="require('../assets/images/services.jpg')"  alt=""> -->
            </div>
            <div class="container__service--info">
                <h1>NUESTROS SERVICIOS</h1>
                <div>
                    <p>
                    Destacamos por ofrecer servicios integrales de alta
                    calidad. Cumpliendo expectativas, generando alianzas
                    comerciales con nuestros clientes y proveedores.
                    Estos son algunos de los servicios profesionales que
                    ofrecemos: </p>
                <ul>
                    <li>Importación e intermediación de repuestos</li>
                    <li>Desarrollo y comercialización de tecnología</li>
                    <li>Compra y venta de piezas de necesidades industriales</li>
                    <li>Asesoría y desarrollo de programas de capacitación</li>
                    <li>Venta de elementos empresariales</li>
                </ul>
                </div>
                
            </div>
        </div>
    </div>
</template>
<style scoped>
.container__body{
    width: 100%;
    height: 80vh;
}
.container__service{
    display: grid;
    grid-template-columns: repeat(2,1fr);
    height: 100%;
    width: 100%;
}
.container__service--img{
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100%;
    width: 100%;
}
.container__service--img img{
 width: 700px;
}
.container__service--info{
    display: grid;
    grid-template-rows: 2fr 10fr;
}
.container__service--info h1{
    width: 100%;
    text-align: center;
}
.container__service--info div p{
    width: 100%;
    text-align: justify;
}
.container__service--info div{
    padding:0 40px;
}
@media (max-width: 850px) {
   .container__service{
        grid-template-columns: 1fr;
    }
    .container__body{
        height: 100%;
    }
    .container__service--img img{
        width: 100%;
    }
}
</style>