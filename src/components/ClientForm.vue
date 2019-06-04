<template>
  <div>
    <div class="col-12">
      <div class="row">
        <form class="form col-4">
          <div class="form-group">
            <label for="razonSocial">Razon Social:*</label>
            <input id="razonSocial" v-model="cliente.RazonSocial" class="form-control">
          </div>

          <div class="form-group">
            <label for="rfc">RFC:*</label>
            <input id="rfc" class="form-control" v-model="cliente.RFC">
          </div>

          <div class="form-group">
            <label for="direccion">Dirección:*</label>
            <input id="direccion" v-model="cliente.Direccion" class="form-control">
          </div>

          <div class="form-group">
            <label for="curp">CURP:</label>
            <input type="text" id="curp" v-model="cliente.CURP" class="form-control">
          </div>

          <div class="form-group">
            <label for="buzonTributario">Correo Buzón Tributario:</label>
            <input
              type="text"
              v-model="cliente.BuzonTributario"
              id="buzonTributario"
              class="form-control"
            >
          </div>

          <div class="form-group">
            <label for="comision">Porcentaje Comisión:*</label>
            <input type="text" id="comision" v-model="cliente.Comision" class="form-control">
          </div>

          <div class="form-group">
            <label for="tomaComision">Toma Comisión:*</label>
            <select class="form-control" v-model="cliente.TomaComision">
              <option value="Total">Total</option>
              <option value="Subtotal">Subtotal</option>
            </select>
          </div>

          <div class="form-group">
            <label for="vendedor">Vendedor:*</label>
            <select id="vendedor" v-model="cliente.Vendedor" class="form-control">
              <option value="1">Vendedor 1</option>
              <option value="2">Vendedor 2</option>
            </select>
          </div>

          <div class="form-group">
            <button
              type="button"
              @click.prevent="saveClient"
              class="btn btn-primary float-right"
            >Guardar</button>
          </div>
        </form>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ClientForm",
  data: () => ({
    cliente: {
      RazonSocial: "",
      RFC: "",
      Direccion: "",
      CURP: "",
      Comision: "",
      TomaComision: "Total",
      BuzonTributario: "",
      Vendedor: ""
    }
  }),
  methods: {
    saveClient: () => alert("Guardando...")
  }
};
</script>

<style scoped>
.form {
  border: 1px solid #eee;
  border-radius: 5px;
  padding: 15px;
  margin: 5px;
  font-weight: bold;
}
</style>
