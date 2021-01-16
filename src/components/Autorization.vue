<template>
    <b-row>
        <b-col sm="12">
            <b-card class="text-center default-card">
                <b-card-body>
                    <h2>¿Nos autorizas a pedir tu certificado de liquidación?</h2>
                    <h3 class="subtitle">Puedes autorizar en línea con:</h3>
                    <ul class="option-list">
                        <li><img alt="claveunica" src="@/assets/images/claveunica.png"></li>
                        <li><img alt="claveunica" src="@/assets/images/claveunica.png"></li>
                    </ul>
                    <b-button class="btn-green">Autorización en línea</b-button>
                    <p class="text-info">Para autorizar será redirigido al sitio de Mobisigner.</p>
                    <div class="separate"><div></div><p>Ó</p><div></div></div>
                    <a href="#" class="external-link">Prefiero entregar la Autorización en una sucursal de Consorcio</a>
                </b-card-body>
            </b-card>
        </b-col>
    </b-row>
</template>

<script>
export default {
  name: 'Autorization',
  props: {
    msg: String
  }
}
</script>

<style scoped>
    ul.option-list {
        list-style: none;
        margin: 40px 0 0 0;
        padding: 0;
    }

    ul.option-list li {
        display: inline-block;
        padding: 10px 35px 10px 35px;
        margin: 0;
    }

    ul.option-list li:first-child {
        border-right: 2px solid #dedede;
    }

    ul.option-list li img {
        width: 198px;
        margin: 0;
        filter: grayscale(100%);
    }

    .btn-green {
        background-color: #91ba39;
        border: 0;
        margin-top: 30px;
        margin-bottom: 20px;
        width: 500px;
        height: 85px;
        border-radius: 0.6em;
        font-size: 22px;
        font-family: 'Open Sans', sans-serif;
    }

    .subtitle {
        margin-top: 15px;
    }

    .text-info {
        color: #797b7f !important;
        font-size: 14px;
        font-family: 'Open Sans', sans-serif !important;
    }

    .separate {
        position: relative;
        text-align: center;
        margin-top: 55px;
        margin-bottom: 50px;
    }

    .separate div, .separate p {
        display: inline-block;
        vertical-align: middle;
        margin: 0;
    }

    .separate p {
        padding: 0;
        color: #828487;
    }

    .separate div {
        margin: 0 20px;
        border: 1px solid #e4e4e4;
        width: 160px;
        height: 2px;
    }

    .external-link {
        color: #496db4;
        font-weight: bold;
        font-size: 20px;
    }
</style>