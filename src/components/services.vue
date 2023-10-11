<template>
    <div class="container__body">
        <div class="container__service">
            <div class="container__service--img">
                <img src="https://cdn.pixabay.com/photo/2015/01/08/18/27/startup-593341_960_720.jpg"  alt="">
            </div>
            <div class="container__service--info">
                <h1>NUESTROS SERVICIOS</h1>
                <div>
                    <p>
                    En Uchiha publicidad, estamos comprometidos a llevar tu presencia en línea al siguiente nivel. Somos un equipo apasionado de expertos en marketing digital, diseño web y desarrollo de aplicaciones móviles, listos para transformar tu visión en realidad. </p>
                <ul>
                    <li>Marketing : Manejo de redes, Creación de contenido, Reels, Historias, Chats</li>
                    <li>Plataformas: Tiktok, Instagram, Facebook, WhatsApp, Paginas Web. Snapchat</li>
                    <li>Creación: Fotos, Videos, Videos con Drone</li>
                </ul>
                </div>
                
            </div>
        </div>
    </div>
</template>
<style scoped>
.container__body{
    margin-top: 90px;
    width: 100%;
    height: 80vh;
    font-size: 25px;
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