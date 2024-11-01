<template>
  <v-dialog
    v-model="mostrar"
    width="auto"
    persistent
  >
    <v-card
      class="mx-auto pa-6 elevation-4"
      max-width="550"
    >
      <v-card-title class="headline bg-primary text-white py-4 d-flex align-center justify-center">
        <v-icon left class="mr-2 text-white">mdi-bag-personal</v-icon>
        Resumen de Compra
      </v-card-title>

      <v-card-text class="pa-6">
        <v-divider class="mb-4"></v-divider>
        
        <div v-for="(data, index) in compras" :key="index" class="my-4 d-flex justify-space-between align-center">
          <p class="text-h6 font-weight-medium mb-1">{{ data.titulo || 'Producto sin nombre' }}</p>
          <p class="text-subtitle-1 font-weight-light">${{ data.precio ? data.precio.toFixed(2) : '0.00' }}</p>
        </div>
        
        <v-divider class="mt-4"></v-divider>
      </v-card-text>

      <v-card-actions class="justify-center py-3">
        <v-btn
          color="secondary"
          rounded
          @click="cerrar"
        >Cerrar</v-btn>
      </v-card-actions>
    </v-card>
  </v-dialog>
</template>

<script>
export default {
  props: {
    show: {
      type: Boolean,
      default: false
    },
    compras: {
      type: Array,
      required: true
    }
  },
  data() {
    return {
      mostrar: false
    }
  },
  methods: {
    cerrar() {
      this.$emit('cerrar');
    }
  },
  watch: {
    show(newVal) {
      this.mostrar = newVal;
    }
  }
}
</script>

<style scoped>
.v-card {
  border-radius: 16px;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.15);
  background-color: #f8f9fa;
}

.v-card-title {
  font-family: 'Montserrat', sans-serif;
  letter-spacing: 1px;
}

.v-card-text div {
  border-bottom: 1px solid #e0e0e0;
  padding-bottom: 10px;
}

.v-card-actions .v-btn {
  font-family: 'Roboto', sans-serif;
  text-transform: uppercase;
  font-size: 14px;
  font-weight: 500;
}
</style>




