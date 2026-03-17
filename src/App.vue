<template>
  <div>
    <h1 :title="tituloPagina">{{ tituloPagina }}</h1>

    <input v-model="titulo" placeholder="Título del reporte" />
    <br /><br />

    <textarea v-model="descripcion" placeholder="Descripción"></textarea>
    <br /><br />

    <select v-model="tipo">
      <option disabled value="">Seleccione tipo</option>
      <option>Accidente</option>
      <option>Calle dañada</option>
      <option>Emergencia</option>
    </select>

    <br /><br />
    <button @click="agregarReporte">Agregar Reporte</button>

    <p v-if="error" style="color:red">{{ error }}</p>

    <h2>Lista de reportes</h2>

    <ul>
      <li v-for="(reporte, index) in reportes" :key="index">
        <strong>{{ reporte.titulo }}</strong> - {{ reporte.tipo }}
        <p>{{ reporte.descripcion }}</p>
        <button @click="eliminarReporte(index)">Eliminar</button>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      titulo: '',
      descripcion: '',
      tipo: '',
      reportes: [],
      error: '',
      tituloPagina: 'Registro de Incidentes en San Miguel'
    }
  },
  methods: {
    agregarReporte() {
      if (!this.titulo || !this.descripcion || !this.tipo) {
        this.error = "Todos los campos son obligatorios";
        return;
      }

      this.reportes.push({
        titulo: this.titulo,
        descripcion: this.descripcion,
        tipo: this.tipo
      });

      this.titulo = '';
      this.descripcion = '';
      this.tipo = '';
      this.error = '';
    },
    eliminarReporte(index) {
      this.reportes.splice(index, 1);
    }
  }
}
</script>

<style>
body {
  font-family: Arial;
  margin: 20px;
}

input, textarea, select {
  width: 300px;
  margin-bottom: 10px;
  padding: 5px;
}

button {
  padding: 5px 10px;
}
</style>