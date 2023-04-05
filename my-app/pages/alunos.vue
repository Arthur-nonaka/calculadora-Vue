<template>
    <form @submit.prevent="$e => salvarAluno()">
        <input type="text" placeholder="Nome" v-model="name">
        <input type="text" placeholder="Idade" v-model="age">
        <input type="text" placeholder="Serie" v-model="clas">
        <button> Salvar </button>
    </form>
    <hr>
    <ul v-for="(aluno,index) in this.dados">
            <li>codigo: {{ index }}</li>
            <li>Nome: {{ aluno.name }} </li>
            <li>Idade: {{ aluno.age }}</li>
            <li>Serie: {{ aluno.class }}</li>
            <button @click="$e => editarAluno(index)">Editar</button>
            <button @click="$e => deletarAluno(index)">Deletar</button>

    </ul>
</template>

<script>
import dados from "~/alunos.json";

export default {
    methods: {
        salvarAluno() {
            this.dados.push({ "name": this.name, "age": this.age, "class": this.clas });
            console.log(dados);
        },
        deletarAluno(index) {
            this.dados.splice(index,1);
        },
        editarAluno(index){
            this.dados[index].name = prompt("Nome: ", this.dados[index].name);
            this.dados[index].age = prompt("Idade: ", this.dados[index].age);
            this.dados[index].class = prompt("Serie: ", this.dados[index].class);
        }
    },
    data() {
        return {
            dados: dados,
            name: "",
            age: "",
            clas: "",
        }
    }
}


</script>