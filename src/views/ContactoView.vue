<template>
        <div class="container ">
        <h2 class="text-center mb-4 mt-5">Formulario de Contacto</h2>
        <form>
            <div class="mb-3">
                <label for="name" class="form-label">Nombre completo</label>
                <input type="text" class="form-control" id="name" placeholder="Introduce tu nombre completo" required>
            </div>
            <div class="mb-3">
                <label for="email" class="form-label">Correo Electrónico</label>
                <input type="email" class="form-control" id="email" placeholder="ejemplo@correo.com" required>
            </div>
            <div class="mb-3">
                <label for="phone" class="form-label">Teléfono</label>
                <input type="tel" class="form-control" id="phone" placeholder="Introduce tu número de teléfono" required>
            </div>
            <div class="mb-3">
                <label for="message" class="form-label">Mensaje</label>
                <textarea class="form-control" id="message" rows="4" placeholder="Escribe tu mensaje" required></textarea>
            </div>
            <button type="submit" class="btn btn-primary">Enviar</button>
        </form>
    </div>
    <div class="inicio">
        <button class="btn btn-primary" @click="volverInicio">Volver al inicio</button>
    </div>
    

</template>

<script>
export default {
    name: 'ContactoView',
    methods: {
        volverInicio() {
            return this.$router.push({ name: 'home' })
        }
    }
}

</script>

<style scoped>
.container{
    margin-top: 100px;
    
}
form{
    
    margin: 50px;
}
.inicio {
    text-align: center;
    width: 100%;
    margin-bottom: 20px;
}
</style>