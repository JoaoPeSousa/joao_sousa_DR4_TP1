<template>
  <div class="alert">
    <div class="alert-success" v-for="tarefa in tarefas" style="text-align: center" :key="tarefa.id" :class="{ 'alert-danger': !tarefa.estaCompleta, 'alert-success: =': tarefa.estaCompleta}"
         >
      <b-alert variant="primary">{{ tarefa.descricao | toUpperCase() }}</b-alert>
    </div>
  </div>
</template>

<script>
import 'bootstrap/dist/css/bootstrap.css'
import 'bootstrap-vue/dist/bootstrap-vue.css'

export default {
  name: 'App',

  data() {
    return {
      title: "Tarefas",
      tarefas: [
        {id: 1, descricao: "Limpar o quarto", estaCompleta: true},
        {id: 2, descricao: "Levar o cachorro para fazer cocô", estaCompleta: false},
        {id: 3, descricao: "Lavar as louças", estaCompleta: true},
        {id: 4, descricao: "Tirar o lixo pra fora", estaCompleta: false},
        {id: 5, descricao: "Pagar os boletos", estaCompleta: true},
        {id: 6, descricao: "Levar minha avó no jiu-jitsu", estaCompleta: true}
      ],
    };
  },
  // Filtro Vue da questão 8
  filters: {
    toUpperCase(str) {
      return str.toUpperCase()
    }
  }
}
</script>

<style>

</style>
