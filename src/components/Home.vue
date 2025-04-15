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
          <button>Comprar</button>
        </li>
      </ul>
    </section>
  </div>
</template>

<style scoped>
* {
  color: #000;
}
button {
  cursor: pointer;
}
section.lancamentos {
  margin: 4vw 2vw;
}
section.lancamentos h2 {
  font-size: 40px;
  font-weight: 300;
}
section.lancamentos ul {
  display: flex;
  align-items: center;
  justify-content: space-around;
  flex-wrap: wrap;
}
section.lancamentos ul li {
  width: 25%;
  list-style: none;
  margin: 2vw 0;
  font-size: 130%;
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
section.lancamentos ul li button{
    width: 64%;
    background: #27AE60;
    color: #fff;
    padding: 10px 0;
    border-radius: 2px;
    border: none;
    font-size: 120%;
}
</style>
