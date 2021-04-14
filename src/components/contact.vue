<template>
    <div class="container__body">
        <div class="container__contact">
            <div class="container__contact--client">
             <h1>ATENCIÓN AL CLIENTE</h1>
             <p>Nuestro portafolio de servicios está diseñado para ayudarle a
                identificar y cubrir las necesidades de su oficina, empresa o industria.
                Por intermedio de nuestro correo electónico podrá de manera directa
                realizar su pedido de conformidad con la categorías que tenemos a su
                disposición.
                De igual forma podrá comunicarse con Grupo DESCA S.A.S. vía
                telefónica, correo electrónico, redes sociales.

                Podrá solicitar atención personalizada por parte de nuestra fuerza de
                ventas en las instalaciones de su empresa.</p>
            </div>
            <div class="container__contact--info">
                <h2>CONTÁCTENOS</h2>
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
                        “El éxito no se logra sólo con cualidades especiales. Es sobre todo un trabajo de constancia, de método y de organización”. J.P. Sergent
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
                window.location.href = `mailto:solutionspremium@hotmail.com&subject=${asunto}&body=${text}`;
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
    width: 100%;
    height: 100%;
}
.container__contact{
    display: grid;
    grid-template-columns: repeat(3,1fr);
    height: 100%;
}
.container__contact--text{
     /* background-image: url('../assets/images/contactenos.jpg'); */
     background-size:cover;
     height: 72.5vh;
}
.container__contact--text__light{
    background-color:rgba(0, 13, 50,0.7);
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
    border-bottom:1px solid rgba(0, 13, 50,0.7);;
}
.container__contact--info__form button{
    width: 40%;
    height: 40px;
    border-radius: 5px;
    color: white;
    font-size: 25px;
    background-color: rgba(0, 13, 50,1);
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