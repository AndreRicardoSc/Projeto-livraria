<script setup>
import { ref } from 'vue';
const produtos = ref([
  {
    id: 1,
    titulo: 'Chain of Iron: Volume 2',
    autor: 'Cassandra Clare',
    preco: 23.24,
    capa:"/src/assets/imgs/chainofironv2.png"
  },
  {
    id: 2,
    titulo: 'Chain of Thorns',
    autor: 'Cassandra Clare',
    preco: 23.24,
    capa:"/src/assets/imgs/chainofthorns.png"
  },
  {
    id: 3,
    titulo: 'City of Fallen',
    autor: 'Cassandra Clare',
    preco: 13.94,
    capa:"/src/assets/imgs/cityoffallenangels.png"
  },
  {
    id: 4,
    titulo: 'Nona the Ninth',
    autor: 'Cassandra Clare',
    preco: 16.84,
    capa:"/src/assets/imgs/nonatheninth.png"
  },
  {
    id: 5,
    titulo: 'Harlem Shuffle',
    autor: 'Colson Whitehead',
    preco: 26.92,
    capa:"/src/assets/imgs/harlemshuffle.png"
  },
  {
    id: 6,
    titulo: 'Two Old Women',
    autor: 'Velma Wallis',
    preco: 13.95,
    capa:"/src/assets/imgs/twooldwomen.png"
  },
  {
    id: 7,
    titulo: 'Carrie Soto Is Back',
    autor: 'Taylor Jenkins Reid',
    preco: 26.04,
    capa:"/src/assets/imgs/carriesotoisback.png"
  },
  {
    id: 8,
    titulo: 'Book Lovers',
    autor: 'Emily Henry',
    preco: 15.81,
    capa:"/src/assets/imgs/booklovers.png"
  },
])
</script>

<template>
  <div class="home">
    <section class="lancamentos">
      <h2>Lançamentos</h2>
      <ul>
        <li class="livros" v-for="(item, index) of produtos" :key="index">
          <img :src="item.capa" :alt="item.titulo" />
          <h3>{{ item.titulo }}</h3>
          <p class="autor">{{ item.autor }}</p>
          <div class="info">
            <p>R${{ item.preco }}</p>
          </div>
          <button>
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 576 512">!Font Awesome Free 6.7.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2025 Fonticons, Inc.<path d="M0 24C0 10.7 10.7 0 24 0L69.5 0c22 0 41.5 12.8 50.6 32l411 0c26.3 0 45.5 25 38.6 50.4l-41 152.3c-8.5 31.4-37 53.3-69.5 53.3l-288.5 0 5.4 28.5c2.2 11.3 12.1 19.5 23.6 19.5L488 336c13.3 0 24 10.7 24 24s-10.7 24-24 24l-288.3 0c-34.6 0-64.3-24.6-70.7-58.5L77.4 54.5c-.7-3.8-4-6.5-7.9-6.5L24 48C10.7 48 0 37.3 0 24zM128 464a48 48 0 1 1 96 0 48 48 0 1 1 -96 0zm336-48a48 48 0 1 1 0 96 48 48 0 1 1 0-96z"/></svg>
            Comprar
          </button>
        </li>
      </ul>
    </section>
  </div>
</template>

<style scoped>
svg{
  width: 20px;
  fill: #fff;
}
* {
  color: #000;
}
button {
  cursor: pointer;
}
section.lancamentos {
  margin: 4vw 8vw;
}
section.lancamentos h2 {
  margin: 4vw;
  font-size: 4rem;
  font-weight: 400;
}
section.lancamentos ul {
  display: flex;
  align-items: center;
  justify-content: space-around;
  flex-wrap: wrap;
}
section.lancamentos ul li {
  width: 23%;
  list-style: none;
  margin: 2vw 2px;
  padding: 0;
  font-size: 130%;
}
section.lancamentos ul li img{
  width: 100%;
}
section.lancamentos ul li p{
    margin: 1vw 0;
}
section.lancamentos ul li p.autor{
    color: #4F4C57;
}
section.lancamentos ul li div.info p{
    font-size: 130%;
}
section.lancamentos ul li div.button{
  background-color: #000;
}
section.lancamentos ul li button{
    width: 100%;
    background: #27AE60;
    color: #fff;
    padding: 10px 0;
    border-radius: 2px;
    border: none;
    font-size: 120%;
}
section.lancamentos ul li button:hover{
  background: #27AE60;
}
</style>
