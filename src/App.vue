<template>
  <div class="row">
    <div class="input-group">
      <label for="nome" class="input-group-text">Nome</label>
      <input
        type="text"
        placeholder="Digite seu nome"
        class="form-control form-control-se"
        v-model="curso.nome"
      />
    </div>
    <div class="input-group">
      <label for="duracao" class="input-group-text">Duração</label>
      <input
        type="text"
        placeholder="Duração do curso"
        class="form-control form-control-se"
        v-model="curso.duracao"
      />
    </div>
    <div class="input-group">
      <label for="vagas" class="input-group-text">Vagas</label>
      <input
        type="text"
        placeholder="Número de vagas"
        class="form-control form-control-se"
        v-model="curso.vagas"
      />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      cursoList: [],

      curso: {
        nome: "",
        duracao: "",
        vagas: "",
      },
    };
  },
  methods: {
    adicionarCurso() {
      this.cursoList.pusg(this.curso);
    },
  },
};
</script>

<style scoped></style>
