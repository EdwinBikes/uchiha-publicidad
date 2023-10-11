<template>
    <div class="container__body">
        <div class="container__contact">
            <div class="container__contact--client">
             <h1>CONTÁCTENOS</h1>
             <p>
                Nuestro equipo está formado por profesionales altamente calificados y apasionados por el marketing digital y la tecnología. Desde estrategas creativos hasta expertos en seguridad cibernética y analistas de datos, cada miembro de nuestro equipo aporta su experiencia única para ofrecer soluciones de vanguardia. Trabajamos en conjunto, aprovechando la diversidad de nuestras habilidades para brindar resultados excepcionales a nuestros clientes.
             </p>
            </div>
            <div class="container__contact--info">
                <h2>Escribenos para mayor información</h2>
                <p>¿Quieres hacernos alguna pregunta? Ponte en contacto con nosotros y te responderemos en el menor tiempo posible. A tu disposición ponemos a todo un equipo de profesionales dispuestos a aportar soluciones a tus problemas.</p>
                <div class="container__contact--info__form">
                    <input type="text" name="first_name" id="name" placeholder="Nombre">
                    <input type="text" name="last_name" id="last" placeholder="Apellido">
                    <input type="number" name="phone" id="phone" placeholder="Telefono">
                    <input type="email" name="email" id="email" placeholder="Correo">
                    <input type="text" name="request" id="option" placeholder="Opcional">
                    <button @click="sendInfo()">Enviar</button>
                </div>
            </div>
            <div class="container__contact--text">
                <div class="container__contact--text__light">
                    <p>
                        “El secreto del éxito en publicidad es decir la verdad, pero de manera que resulte interesante.”. Leo Burnett
                    </p>
                </div>
                
            </div>
        </div>
    </div>
</template>
<script>
export default {
    data (){
        return{

        }
    },
    methods:{
        sendInfo(){
            const name = document.getElementById('name').value
            const last = document.getElementById('last').value
            const phone = document.getElementById('phone').value
            const email = document.getElementById('email').value
            const option = document.getElementById('option').value
            if (!this.validEmail(email)){
                alert('Por favor verificar el correo sea correcto')
                
            }else{
                var text 
                if(!option){
                    text =`Hola soy ${name} ${last} quisiera averiguar sobre sus servicios mi numero de telefono es ${phone}`
                }else{
                    text =`Hola soy ${name} ${last} quisiera averiguar sobre sus servicios acerca de ${option} mi numero de telefono es ${phone}`
                }
                const asunto =`Conocer sus servicios`      
                window.location.href = `mailto:uchihapublicidad@gmail.com&subject=${asunto}&body=${text}`;
            }
            
        },
        validEmail(email) {
            console.log('entre aca')
            var re = /^[a-z0-9!#$%&'*+/=?^_`{|}~-]+(?:\.[a-z0-9!#$%&'*+/=?^_`{|}~-]+)*@(?:[a-z0-9](?:[a-z0-9-]*[a-z0-9])?\.)+[a-z0-9](?:[a-z0-9-]*[a-z0-9])?$/;
            console.log(re.test(email))
            return re.test(email);
        }
    }
}
</script>
<style scoped>
.container__body{
    margin-top: 90px;
    width: 100%;
    height: 100%;
}
.container__contact{
    display: grid;
    grid-template-columns: repeat(3,1fr);
    height: 100%;
}
.container__contact--text{
     background-image: url('https://images.pexels.com/photos/11448038/pexels-photo-11448038.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1');
     background-size:cover;
     background-position: center;
     height: 72.5vh;
}
.container__contact--text__light{
    background-color:rgba(40, 40, 42,0.7);
    font-size: 20px;
    width: 100%;
    color:white;
    text-align: center;

}
.container__contact--text__light p{
    margin: 60vh 20px 0 20px;
}
.container__contact--client{
    display: grid;
    grid-template-rows: 2fr 10fr;
    margin: 0 60px;
}
.container__contact--client h1{
    text-align: center;
}
.container__contact--client p{
    text-align: justify;
    justify-content: center;
    margin: 0  20px 30px 20px;
}
.container__contact--info{
    display: grid;
    grid-template-rows: 2fr 2fr 8fr;
    margin: 0 60px;
}
.container__contact--info h2{
    text-align: center;
}
.container__contact--info p{
    text-align: justify;
    justify-content: center;
}
.container__contact--info__form{
    display: flex;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;
}
.container__contact--info__form input{
    outline: none;
    width: 100%;
    border:0;
    border-bottom:1px solid rgba(40, 40, 42,1);
}
.container__contact--info__form button{
    width: 40%;
    height: 40px;
    border-radius: 5px;
    color: white;
    font-size: 25px;
    background-color: rgba(40, 40, 42,1);
}
@media (max-width: 850px) {
   .container__contact{
        grid-template-columns: 1fr;
    }
    .container__contact--text{
        height: 100%;
        background-size:contain;
        background-repeat: no-repeat;
        margin-bottom: 80px;
    }
    .container__contact--client{
        display: flex;
        justify-content: center;
        align-items: center;
        flex-wrap: wrap;
        margin: 0px;
    }
}
@media (max-width: 850px)  and (orientation: landscape){
  
   .container__contact{
        grid-template-columns: 1fr;
    }
    .container__contact--text{
        height: 100%;
        background-size:contain;
        background-position: center;
        background-repeat: no-repeat;
        margin-bottom: 80px;
    }
    .container__contact--client{
        display: flex;
        justify-content: center;
        align-items: center;
        flex-wrap: wrap;
        margin: 0px;
    }
}
</style>