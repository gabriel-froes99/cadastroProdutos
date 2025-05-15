<script setup>
import { ref } from 'vue';

defineProps({
    msg: String,
});

const nomeProduto = ref('');
const categoria = ref('');
const dataCadastro = ref('');
const funcionarios = ref(false);

const cadastroFuncionario = () => {
    funcionarios.value = !mostrarTemplateAdicional.value;
};

</script>
<template>
    <div class="card">
        <h1>{{ msg }}</h1>
        <form @submit.prevent>
            <div class="form-group">
                <label for="nomeProduto">Nome do Produto:</label>
                <input type="text" id="nomeProduto" v-model="nomeProduto" />
            </div>
            <div class="form-group">
                <label for="categoria">Categoria:</label>
                <input type="text" id="categoria" v-model="categoria" />
            </div>
            <div class="form-group">
                <label for="dataCadastro">Data do Cadastro:</label>
                <input type="date" id="dataCadastro" v-model="dataCadastro" />
            </div>
            <button type="submit">Cadastrar</button>
        </form>

        <button @click="cadastroFuncionario" style="margin-top: 30px;">
            {{ funcionarios ? 'Fechar cadastro de Funcionários' : 'Abrir cadastro de Funcionários' }}
        </button>

        <div v-if="funcionarios" class="cadastro-funcionarios">
            
            
        </div>
    </div>
</template>

<style scoped>
    .card {
        width: 900px;
        height: 400px;
        background-color: #3c3c3c;
        padding: 20px; 
        color: white; 
        border-radius: 10px; 
        border: 2px solid black;
    }
    .form-group {
        margin-bottom: 15px;
        & label {
            display: block;
            margin-bottom: 5px;
        }
        & input {
            width: 100%;
            padding: 8px;
            box-sizing: border-box; 
    }
    & button {
        margin-top: 15px;
        
    }
}

.cadastro-funcionarios {
    margin-top: 20px;
    padding: 15px;
    border: 1px dashed #ccc;
    background-color: #4a4a4a; /* Um pouco mais claro que o card para diferenciar */
    border-radius: 5px;
}
</style>