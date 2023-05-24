<script setup>
import {livros} from '@/_data/livro'

</script>

<template>
  <h1><mark style="background-color: rgb(190, 2, 39);color: rgb(0, 0, 0);">Minha Livraria</mark></h1>
  <div class="listagem-livros">
    <div v-for="livro in livros" :key="livro.id" class="card-livro">
      <img :src="livro.cover" alt="capa" class="livro-capa" />
      <p class="livro-titulo">{{ livro.title }}</p>
      <p class="livro-autor">{{ livro.author }}</p>
      <p class="livro-preco">{{ livro.price }}</p>

    </div>

 </div>
  
</template>

<style scoped>
.livro-titulo{
  font-weight: bold;
  font-size: 1.2rem;
  margin-bottom: 5px;
}
.livro-capa{
  width: 200px;
}
.card-livro{
  background-color:beige;
  padding: 10px;
  border-radius: 10px;
  width: 200px;
  margin: 10px;
}
.listagem-livros {
  margin: 0;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
}

</style>
