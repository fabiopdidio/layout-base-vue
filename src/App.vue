<template>
  <div class="row d-flex align-itens-center ms-5 me-5">
    <div class="input-group mb-3 mt-3 col">
      <label for="nome" class="input-group-text">Nome</label>
      <input
        type="text"
        placeholder="Digite seu nome"
        class="form-control form-control-se"
        v-model="curso.nome"
      />
    </div>
    <div class="input-group mb-3 mt-3 col">
      <label for="duracao" class="input-group-text">Duração</label>
      <input
        type="text"
        placeholder="Duração do curso"
        class="form-control form-control-se"
        v-model="curso.duracao"
      />
    </div>
    <div class="input-group mb-3 mt-3 col">
      <label for="vagas" class="input-group-text">Vagas</label>
      <input
        type="text"
        placeholder="Número de vagas"
        class="form-control form-control-se"
        v-model="curso.vagas"
      />
    </div>
    <button class="col-1 btn btn-primary mt-3" @click="adicionarCurso">
      Cadastrar
    </button>
  </div>
  <div class="d-flex ms-5">
    <div class="card" v-for="curso in cursoList">
      <div class="card-header">
        <div class="card-title">{{ curso.nome }}</div>
      </div>
      <div class="card-body">
        <span>Vagas: {{curso.vagas}}</span><br>
        <span>Duracao: {{curso.duracao}}</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      cursoList: [], // Array vazio para os cursos serem adicionados

      curso: {
        // Variáveis iniciam somente com ""
        nome: "",
        duracao: "",
        vagas: "",
      },
    };
  },
  methods: {
    adicionarCurso() {
      this.cursoList.push({...this.curso}); //Adiciona o curso à lista de cursos
    },
  },
};
</script>

<style scoped></style>
