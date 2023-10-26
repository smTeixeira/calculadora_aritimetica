<script>
export default {
  data() {
    return {
      numero1: 0,
      numero2: 0,
      operacao: 'soma',
    };
  },
  methods: {
    calcularResultado() {
      switch (this.operacao) {
        case 'soma':
          return this.numero1 + this.numero2;
        case 'subtracao':
          return this.numero1 - this.numero2;
        case 'multiplicacao':
          return this.numero1 * this.numero2;
        case 'divisao':
          return this.numero1 / this.numero2;
        default:
          return null;
      }
    },
  },
};
</script>

<template>
  <div class="container">
    <label for="numero1">Número 1:</label>
    <input v-model.number="numero1" id="numero1" type="number" />

    <label for="numero2">Número 2:</label>
    <input v-model.number="numero2" id="numero2" type="number" />

    <label for="operacao">Operação:</label>
    <select v-model="operacao" id="operacao">
      <option value="soma">Soma</option>
      <option value="subtracao">Subtração</option>
      <option value="multiplicacao">Multiplicação</option>
      <option value="divisao">Divisão</option>
    </select>

    <div>
      <h2>Resultado: {{ calcularResultado() }}</h2>
    </div>
  </div>
</template>



<style>
.container {
  max-width: 1024px;
  width: 100%;
  font-family: Arial, sans-serif;
  text-align: center;
  color: #0d0a1f;
  margin-top: 60px;
}
</style>
