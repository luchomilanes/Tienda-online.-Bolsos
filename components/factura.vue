<template>
  <v-dialog
    v-model="mostrar"
    width="auto"
    persistent
  >
    <v-card
      class="mx-auto pa-4 elevation-3"
      max-width="500"
    >
      <v-card-title class="headline grey lighten-2 py-3 d-flex align-center">
        <v-icon left class="mr-2">mdi-cart</v-icon>
        Productos Comprados
      </v-card-title>

      <v-card-text>
        <v-divider></v-divider>
        <div v-for="(data, index) in compras" :key="index" class="my-3">
          <p class="font-weight-bold mb-1">{{ data.titulo }}</p>
          <p class="text--secondary">${{ data.precio.toFixed(2) }}</p>
        </div>
        <v-divider></v-divider>
      </v-card-text>

      <v-card-actions class="justify-end">
        <v-btn
          color="primary"
          text
          @click="cerrar()"
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
  border-radius: 50px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
}
</style>


