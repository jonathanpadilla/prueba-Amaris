<template>
    <b-row>
        <b-col sm="12">
            <b-card class="text-center default-card">
                <b-card-body>
                    <ul class="list-help">
                        <li><h3>¿Nevesitas ayuda para continuar?</h3></li>
                        <li><b-button>Te llamamon gratis</b-button></li>
                    </ul>
                    <div class="info-help">
                        <p>Te llamamos de Lunes a Viernes de 8:00 a 18:00 hrs.</p>
                        <p>Fuera de estos horarios, será durante el día siguiente.</p>
                    </div>
                </b-card-body>
            </b-card>
        </b-col>
    </b-row>
</template>

<script>
export default {
  name: 'Help'
}
</script>

<style scoped>
    .list-help {
        list-style: none;
        margin: 0;
        padding: 0;
    }

    .list-help li {
        display: inline-block;
        vertical-align: middle;
        margin: 5px 10px 5px 10px;
    }

    .list-help li .btn {
        background-color: #15397d;
        width: 340px;
        height: 65px;
        border-radius: 0.8em;
        font-size: 22px;
        font-family: 'Open Sans', sans-serif;
    }

    .list-help li h3 {
        margin: 0;
        font-size: 24px;
    }

    .info-help {
        text-align: center;
        margin-top: 30px;
    }

    .info-help p{
        color: #96989a;
        margin: 0;
        font-size: 18px;
    }

    @media only screen and (max-width: 768px) {
        .list-help li .btn  {
            width: 200px;
            height: fit-content;
        }
    }
</style>