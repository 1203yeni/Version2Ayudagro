<template>
  <div class="container">
    <b-row class="my1">
      <b-col class="primera" sm="3">
        <div class="perfil">
          <b-row>
            <b-col>
              <img class="img1" src="@/assets/foto-perfil.png" alt="foto" />
              <h1 class="administrador">Administrador</h1>
            </b-col>
          </b-row>
        </div>
        <div class="combo">
          <img />
        </div>

        <br />
        <b-button class="Categorias btn btn-light d-grid gap-2 mx-auto"
          >Usuario</b-button
        >
        <br />
        <b-button class="Categorias btn btn-light d-grid gap-2 mx-auto"
          >Pregunta</b-button
        >
        <br />
        <b-button class="Categorias btn btn-light d-grid gap-2 mx-auto"
          >Sugerencias</b-button
        >
        <br />
        <b-button class="Categorias btn btn-light d-grid gap-2 mx-auto"
          >Categorias</b-button
        >
        <br />
        <b-button class="Categorias btn btn-light d-grid gap-2 mx-auto"
          >SubCategorias</b-button
        >
        <br />
        <br />
        <b-button class="Cerrar btn btn-light d-grid gap-2 mx-auto"
          >Cerrar secion</b-button
        >
      </b-col>
      <b-col sm="1"> </b-col>

      <b-col class="segunda" sm="8">
        <b-table
          :filter="filter"
          id="my-table"
          :items="items"
          :fields="fields"
          class="my-table"
          :per-page="perPage"
          :current-page="currentPage"
        >
          <template #cell(ACCIONES)="row">
            <b-button
              @click="ver(row.item.id)"
              size="sm"
              variant="info"
              class="mb-2"
            >
              <b-icon icon="eye-fill" aria-hidden="trued"></b-icon>
            </b-button>

            <b-button
              @click="editar(row.item.id)"
              size="sm"
              variant="success"
              class="mb-2"
            >
              <b-icon icon="pencil-fill" aria-hidden="trued"></b-icon>
            </b-button>
            <b-button
              size="sm"
              @click="eliminar()"
              variant="danger"
              class="mb-2"
            >
              <b-icon icon="trash-fill" aria-idem="true"></b-icon>
            </b-button>
          </template>
        </b-table>

        <b-pagination
          v-model="currentPage"
          :total-rows="rows"
          :per-page="perPage"
          aria-controls="my-table"
        ></b-pagination>
      </b-col>
    </b-row>
  </div>
</template>

<script>
import Swal from 'sweetalert2'
export default {
  
  name: "CategoriasAdmView",
  data() {
    return {
      fields: [
        { key: "id", label: "Id" },
        { key: "Nombre", label: "Nombre" },
        { key: "Subcategorias", label: "Subcategorias" },
        "ACCIONES",
      ],
      items: [
        {
          isActive: true,
          id: 1,
          Nombre: "Hortalizas",
          Subcategorias: "Zanahoria",
        },
      ],
    };
  },
  methods: {
    eliminar() {
      Swal.fire({
        title: "Are you sure?",
        text: "You won't be able to revert this!",
        icon: "warning",
        showCancelButton: true,
        confirmButtonColor: "#3085d6",
        cancelButtonColor: "#d33",
        confirmButtonText: "Yes, delete it!",
      }).then((result) => {
        if (result.isConfirmed) {
          Swal.fire("Deleted!", "Your file has been deleted.", "success");
        }
      });
    },
  },
};
</script>

<style scoped>
.img1 {
  border-radius: 85%;
  border: 1% solid;
  width: 35%;
  height: 60%;
}
.primera {
  border: 1px solid;
}
.perfil {
  border: 1px solid;
  background-color: rgb(67, 133, 67);
  padding: 1%;
  border-radius: 1%;
}
.logo {
  width: 30%;
  height: 30%;
}
.Categorias {
  background-color: rgb(67, 133, 67);
  width: 80%;
}
.Cerrar {
  background-color: rgb(67, 133, 67);
  width: 70%;
}
</style>
