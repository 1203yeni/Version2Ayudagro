<template>
    <div class="container">
        <b-row class="my1">
            <b-col class="primera" sm="3">
                <div class="perfil">
                    <b-row>
                        <b-col>
                            <img class="img1" src="@/assets/foto-perfil.png" alt="foto">
                            <h1 class="administrador">Administrador</h1>
                        </b-col>
                    </b-row>
                </div >
                <div class="combo">
                <img>
                </div>

                <br>
                <b-button class="Categorias btn btn-light d-grid gap-2 mx-auto">Usuario</b-button>
                <br>
                <b-button class="Categorias btn btn-light d-grid gap-2 mx-auto">Pregunta</b-button>
                <br>
                <b-button class="Categorias btn btn-light d-grid gap-2 mx-auto">Sugerencias</b-button>
                <br>
                <b-button class="Categorias btn btn-light d-grid gap-2 mx-auto">Categorias</b-button>
                <br>
                <b-button class="Categorias btn btn-light d-grid gap-2 mx-auto">SubCategorias</b-button>
                <br>
                <br>
                <b-button class="Cerrar btn btn-light d-grid gap-2 mx-auto">Cerrar secion</b-button>
            </b-col>
        </b-row>
    </div>
</template>

<script>
</script>

<style scoped>
.img1{
    border-radius: 85%;
    border: 1% solid;
    width: 35%;
    height: 60%;
}
.primera{
    border: 1px solid;
}
.perfil{
    border: 1px solid;
    background-color: rgb(67, 133, 67);
    padding: 1%;
    border-radius: 1%;
}
.logo{
    width: 30%;
    height: 30%;
}
.Categorias{
    background-color: rgb(67, 133, 67);
    width: 80%;
}
.Cerrar{
    background-color: rgb(67, 133, 67);
    width: 70%;
}
</style>