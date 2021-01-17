<template>
    <b-row>
        <b-col sm="12">
            <div class="content-callus">
                <h3>¿Tienes dudas? Te llamamos gratis</h3>
                <span>Déjanos tus datos de contacto y te llamaremos de inmediato.</span>
                <div class="info-help">
                    <p>Te llamamos de Lunes a Viernes de 8:00 a 18:00 hrs.</p>
                    <p>Fuera de estos horarios, será durante el día siguiente.</p>
                </div>
                <b-form id="form-callus" @submit="onSubmit">
                    <b-form-group class="group" label-align="left" label-class="label-f" label="Llamaremos a" label-for="input-name">
                        <b-form-input id="input-name" v-model="form.name" type="text" placeholder="Nombre" required />
                    </b-form-group>
                    <div class="line-1"></div>
                    <b-form-group class="group" label-align="left" label-class="label-f" label="¿Cuál es tu teléfono móvil?" label-for="input-phone">
                        <b-input-group>
                            <b-input-group-prepend>
                                <b-input-group-text class="prepend-input">
                                    <b-icon icon="phone" /> +569
                                </b-input-group-text>
                            </b-input-group-prepend>
                            <b-form-input id="input-phone" v-model="form.phone" type="number" required />
                        </b-input-group>
                    </b-form-group>
                    <b-form-group class="group" label-align="left" label-class="label-f" label="¿Cuál es tu correo electrónico?" label-for="input-email">
                        <b-form-input id="input-email" v-model="form.email" type="email" placeholder="ejemplo@correo.com" required />
                    </b-form-group>
                    <div class="text-right">
                        <b-button type="submit" class="btn-submit">Llámenme</b-button>
                    </div>
                </b-form>
            </div>
        </b-col>
    </b-row>
</template>
    
<script>
    import axios from "axios";
    export default {
    name: 'CallUs',
    data() {
        return {
            form: {
                name: "",
                phone: "",
                email: ""
            }
        }
    },
    methods: {
        onSubmit(event) {
            event.preventDefault()
            console.log(this.form)

            this.getData()

            this.$emit('sent', true)
        },
        getData() {
            axios.get('https://jsonplaceholder.typicode.com/todos')
            .then(response => console.log(response.data))
        }
    }
}
</script>

<style scoped>
    .content-callus {
        text-align: center;
    }

    .content-callus h3 {
        color: #1c49a4;
        margin-top: 10px;
        font-size: 24px;
        font-weight: bold;
    }

    .content-callus span {
        color: #797b7e;
    }

    .info-help {
        margin-top: 10px;
    }

    .info-help p {
        font-family:'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        font-size: 12px;
    }

    #form-callus {
        width: 340px;
        margin: 0 auto;
        margin-bottom: 35px;
    }

    #form-callus .group {
        margin-top: 30px;
    }

    .prepend-input {
        color: #787b7d;
    }

    .btn-submit {
        background-color: #90ba39;
        border: 0;
        width: 180px;
        height: 44px;
    }

    input::-webkit-outer-spin-button,
    input::-webkit-inner-spin-button {
    -webkit-appearance: none;
    margin: 0;
    }

    input[type=number] {
    -moz-appearance: textfield;
    }
</style>