<template>
    <div class="productos">
        <h1>Productos</h1>
        <div class="card" style="width: 18rem;">
            <img :src="imagen" class="card-img-top" alt="...">
            <div class="card-body">
                <h5 class="card-title fw-bold">{{ nombre }}</h5>
                <p class="card-text">{{ descripcion }}</p>
            </div>
            <ul class="list-group list-group-flush">
                <li class="list-group-item">Precio: ${{ precio }}</li>
                <li class="list-group-item">Cantidad: {{ cantidad }}</li>

            </ul>
            <div class="card-body">
                <a href="#" class="card-link">Ver más</a>
                <a href="#" class="card-link">Comprar</a>
            </div>
        </div>
    </div>
    <div class="inicio">
        <button class="btn btn-primary" @click="volverInicio">Volver al inicio</button>
    </div>
</template>
<script>
export default {
    name: 'ProductosView',
    methods: {
        volverInicio() {
            return this.$router.push({ name: 'home' })
        }
    },
    props: {
        // id: {
        //     type: Number,
        //     required: true
        // },
        imagen: {
            type: String,
            required: true
        },
        nombre: {
            type: String,
            required: true
        },
        descripcion: {
            type: String,
            required: true
        },
        precio: {
            type: String,
            required: true
        },
        cantidad: {
            type: String,
            required: true
        }

    }
}
</script>

<style scoped>
.inicio {
    text-align: center;
    width: 100%;

    margin-bottom: 20px;
}

.productos {
    display: grid;
    justify-items: center;
    text-align: center;
    width: 100%;
    height: auto;
    margin-top: 100px;
}
.card {
    text-align: left;
    margin: 10px 0px 30px 0px;
}
</style>