<script setup>
//imports
import { ref, computed } from 'vue'
import BooksList from './components/BooksList.vue';
import FooterComponent from './components/FooterComponent.vue';

//Controle
const controleDePaginas = ref('home')
//produtos - home
const produtos = ref([
  {
    id: 1,
    titulo: 'Chain of Iron: Volume 2',
    autor: 'Cassandra Clare',
    preco: 23.24,
    capa: '/imgs/livros/chainofironv2.png',
    quantidade: 1,
    favorito: false,
  },
  {
    id: 2,
    titulo: 'Chain of Thorns',
    autor: 'Cassandra Clare',
    preco: 23.24,
    capa: '/imgs/livros/chainofthorns.png',
    quantidade: 1,
    favorito: false,
  },
  {
    id: 3,
    titulo: 'City of Fallen',
    autor: 'Cassandra Clare',
    preco: 13.94,
    capa: '/imgs/livros/cityoffallenangels.png',
    quantidade: 1,
    favorito: false,
  },
  {
    id: 4,
    titulo: 'Nona the Ninth',
    autor: 'Cassandra Clare',
    preco: 16.84,
    capa: '/imgs/livros/nonatheninth.png',
    quantidade: 1,
    favorito: false,
  },
  {
    id: 5,
    titulo: 'Harlem Shuffle',
    autor: 'Colson Whitehead',
    preco: 26.92,
    capa: '/imgs/livros/harlemshuffle.png',
    quantidade: 1,
    favorito: false,
  },
  {
    id: 6,
    titulo: 'Two Old Women',
    autor: 'Velma Wallis',
    preco: 13.95,
    capa: '/imgs/livros/twooldwomen.png',
    quantidade: 1,
    favorito: false,
  },
  {
    id: 7,
    titulo: 'Carrie Soto Is Back',
    autor: 'Taylor Jenkins Reid',
    preco: 26.04,
    capa: '/imgs/livros/carriesotoisback.png',
    quantidade: 1,
    favorito: false,
  },
  {
    id: 8,
    titulo: 'Book Lovers',
    autor: 'Emily Henry',
    preco: 15.81,
    capa: '/imgs/livros/booklovers.png',
    quantidade: 1,
    favorito: false,
  },
])

//lógica do carrinho de compras
const carrinho = ref([])
const adicionarAoCarrinho = (index, id) => {
  let contemNoCarrinho = 0
  for (let elem of carrinho.value) {
    if (elem.id == id) {
      contemNoCarrinho++
      elem.quantidade++
    }
  }
  if (contemNoCarrinho == 0) {
    carrinho.value.push(produtos.value[index])
  }

  //looping para corrigir o BUG que encontramos
  for(let elem of carrinho.value){
    if(elem.quantidade <= 0){
      elem.quantidade = 1
    }
  }
}
const removerDoCarrinho = (index) => {
  carrinho.value.splice(index, 1)
}
const precoTotalProdutos = computed(() => {
  let total = 0
  for (let item of carrinho.value) {
    total += item.quantidade * item.preco
  }
  return total
})
//lógica favoritos
const favoritos = ref([]);
const controleFavoritos = ref(0);
const adicionarFavorito = (item) => {
  favoritos.value.push(item);
}
const removerFavorito = (id) => {
  let item = {};
  let value = 0;
  for(let element of favoritos.value){
    if(element.id == id){
      item = element;
      value = favoritos.value.indexOf(item);
    }
  }
  favoritos.value.splice(value, 1);
}
const favorite = (item) => item.favorito = true; controleFavoritos.value++;
const desfavorite = (item) => item.favorito = false; controleFavoritos.value--;
</script>
<template>
  <header>
    <div class="logo">
      <a @click="controleDePaginas = 'home'">
        <h1>IFbooks</h1>
        <p>Apreço a leitura</p>
      </a>
    </div>
    <div class="busca">
      <input type="text" placeholder="Buscar" />
      <button>
        <svg class="lupa" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512">
          !Font Awesome Free 6.7.2 by @fontawesome - https://fontawesome.com License -
          https://fontawesome.com/license/free Copyright 2025 Fonticons, Inc.
          <path
            d="M416 208c0 45.9-14.9 88.3-40 122.7L502.6 457.4c12.5 12.5 12.5 32.8 0 45.3s-32.8 12.5-45.3 0L330.7 376c-34.4 25.2-76.8 40-122.7 40C93.1 416 0 322.9 0 208S93.1 0 208 0S416 93.1 416 208zM208 352a144 144 0 1 0 0-288 144 144 0 1 0 0 288z"
          />
        </svg>
      </button>
    </div>
    <nav>
      <ul>
        <li>
          <a href="">
            <p>Termos</p>
          </a>
        </li>
        <li>
          <a href="">
            <p>Equipe</p>
          </a>
        </li>
        <li>
          <a href="">
            <p>Envio</p>
          </a>
        </li>
        <li>
          <a href="">
            <p>Devoluções</p>
          </a>
        </li>
      </ul>
      <ul class="icons">
        <li>
          <a
            class="border"
            @click="
              () => {
                if (controleDePaginas != 'carrinho') {
                  controleDePaginas = 'carrinho'
                } else {
                  controleDePaginas = 'home'
                }
              }
            "
          >
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 576 512">
              !Font Awesome Free 6.7.2 by @fontawesome - https://fontawesome.com License -
              https://fontawesome.com/license/free Copyright 2025 Fonticons, Inc.
              <path
                d="M0 24C0 10.7 10.7 0 24 0L69.5 0c22 0 41.5 12.8 50.6 32l411 0c26.3 0 45.5 25 38.6 50.4l-41 152.3c-8.5 31.4-37 53.3-69.5 53.3l-288.5 0 5.4 28.5c2.2 11.3 12.1 19.5 23.6 19.5L488 336c13.3 0 24 10.7 24 24s-10.7 24-24 24l-288.3 0c-34.6 0-64.3-24.6-70.7-58.5L77.4 54.5c-.7-3.8-4-6.5-7.9-6.5L24 48C10.7 48 0 37.3 0 24zM128 464a48 48 0 1 1 96 0 48 48 0 1 1 -96 0zm336-48a48 48 0 1 1 0 96 48 48 0 1 1 0-96z"
              />
            </svg>
          </a>
        </li>
        <li>
          <a
            class="border"
            @click="
              () => {
                if (controleDePaginas != 'favoritos') {
                  controleDePaginas = 'favoritos'
                } else {
                  controleDePaginas = 'home'
                }
              }
            "
          >
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512">
              !Font Awesome Free 6.7.2 by @fontawesome - https://fontawesome.com License -
              https://fontawesome.com/license/free Copyright 2025 Fonticons, Inc.
              <path
                d="M47.6 300.4L228.3 469.1c7.5 7 17.4 10.9 27.7 10.9s20.2-3.9 27.7-10.9L464.4 300.4c30.4-28.3 47.6-68 47.6-109.5v-5.8c0-69.9-50.5-129.5-119.4-141C347 36.5 300.6 51.4 268 84L256 96 244 84c-32.6-32.6-79-47.5-124.6-39.9C50.5 55.6 0 115.2 0 185.1v5.8c0 41.5 17.2 81.2 47.6 109.5z"
              />
            </svg>
          </a>
        </li>
        <li>
          <a>
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512">
              !Font Awesome Free 6.7.2 by @fontawesome - https://fontawesome.com License -
              https://fontawesome.com/license/free Copyright 2025 Fonticons, Inc.
              <path
                d="M224 256A128 128 0 1 0 224 0a128 128 0 1 0 0 256zm-45.7 48C79.8 304 0 383.8 0 482.3C0 498.7 13.3 512 29.7 512l388.6 0c16.4 0 29.7-13.3 29.7-29.7C448 383.8 368.2 304 269.7 304l-91.4 0z"
              />
            </svg>
          </a>
        </li>
      </ul>
    </nav>
  </header>
  <div class="home" v-if="controleDePaginas == 'home'">
    <section class="destaques">
      <div>
        <span>Autor de Abril</span>
        <h1>Eric-Emanuel Schmitt</h1>
        <p>
          Eric-Emmanuel Schmitt has been awarded more than 20 literary prizes and distinctions, and
          in 2001 he received the title of Chevalier des Arts et des Lettres. His books have been
          translated into over 40 languages.
        </p>
        <a href="">
          <p>Acessar página do livro</p>
        </a>
      </div>
      <div>
        <img src="/public/imgs/livros/Schmitt_Nocognia_3D_500pcx1.png" alt="livro" />
        <p>*within the stock limit</p>
      </div>
    </section>
    <section class="servicos">
      <ul>
        <li>
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 640 512">
            !Font Awesome Free 6.7.2 by @fontawesome - https://fontawesome.com License -
            https://fontawesome.com/license/free Copyright 2025 Fonticons, Inc.
            <path
              d="M48 0C21.5 0 0 21.5 0 48L0 368c0 26.5 21.5 48 48 48l16 0c0 53 43 96 96 96s96-43 96-96l128 0c0 53 43 96 96 96s96-43 96-96l32 0c17.7 0 32-14.3 32-32s-14.3-32-32-32l0-64 0-32 0-18.7c0-17-6.7-33.3-18.7-45.3L512 114.7c-12-12-28.3-18.7-45.3-18.7L416 96l0-48c0-26.5-21.5-48-48-48L48 0zM416 160l50.7 0L544 237.3l0 18.7-128 0 0-96zM112 416a48 48 0 1 1 96 0 48 48 0 1 1 -96 0zm368-48a48 48 0 1 1 0 96 48 48 0 1 1 0-96z"
            />
          </svg>
          <p>Frete grátis para SC</p>
        </li>
        <li class="center">
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 576 512">
            !Font Awesome Free 6.7.2 by @fontawesome - https://fontawesome.com License -
            https://fontawesome.com/license/free Copyright 2025 Fonticons, Inc.
            <path
              d="M316.9 18C311.6 7 300.4 0 288.1 0s-23.4 7-28.8 18L195 150.3 51.4 171.5c-12 1.8-22 10.2-25.7 21.7s-.7 24.2 7.9 32.7L137.8 329 113.2 474.7c-2 12 3 24.2 12.9 31.3s23 8 33.8 2.3l128.3-68.5 128.3 68.5c10.8 5.7 23.9 4.9 33.8-2.3s14.9-19.3 12.9-31.3L438.5 329 542.7 225.9c8.6-8.5 11.7-21.2 7.9-32.7s-13.7-19.9-25.7-21.7L381.2 150.3 316.9 18z"
            />
          </svg>
          <p>Livros recomendados</p>
        </li>
        <li>
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 576 512">
            !Font Awesome Free 6.7.2 by @fontawesome - https://fontawesome.com License -
            https://fontawesome.com/license/free Copyright 2025 Fonticons, Inc.
            <path
              d="M249.6 471.5c10.8 3.8 22.4-4.1 22.4-15.5l0-377.4c0-4.2-1.6-8.4-5-11C247.4 52 202.4 32 144 32C93.5 32 46.3 45.3 18.1 56.1C6.8 60.5 0 71.7 0 83.8L0 454.1c0 11.9 12.8 20.2 24.1 16.5C55.6 460.1 105.5 448 144 448c33.9 0 79 14 105.6 23.5zm76.8 0C353 462 398.1 448 432 448c38.5 0 88.4 12.1 119.9 22.6c11.3 3.8 24.1-4.6 24.1-16.5l0-370.3c0-12.1-6.8-23.3-18.1-27.6C529.7 45.3 482.5 32 432 32c-58.4 0-103.4 20-123 35.6c-3.3 2.6-5 6.8-5 11L304 456c0 11.4 11.7 19.3 22.4 15.5z"
            />
          </svg>
          <p>Mais vendidos</p>
        </li>
      </ul>
    </section>
    <BooksList
      :products="produtos"
      @add-book-cart="adicionarAoCarrinho"
      @add-book-fav="adicionarFavorito"
      @remove-book-fav="removerFavorito"
      @like="favorite"
      @unlike="desfavorite"
    />
  </div>

  <!--CARRINHO-->

  <section class="carrinho" v-if="controleDePaginas == 'carrinho'">
    <h1>Carrinho</h1>
    <div class="topo">
      <h2>Título</h2>
      <h2>Quantidade</h2>
      <h2>Subtotal</h2>
    </div>
    <div class="corpo">
      <ul v-if="carrinho.length > 0">
        <li v-for="(item, index) of carrinho" :key="index">
          <div class="produto">
            <img :src="item.capa" :alt="item.titulo" />
            <div class="descricao">
              <h3>{{ item.titulo }}</h3>
              <p>{{ item.autor }}</p>
              <span>R${{ item.preco }}</span>
            </div>
          </div>
          <div class="quantidade">
            <button
              @click="
                () => {
                  item.quantidade--
                  if (item.quantidade == 0) {
                    removerDoCarrinho(index)
                  }
                }
              "
            >
              -
            </button>
            <p>{{ item.quantidade }}</p>
            <button
              @click="
                () => {
                  item.quantidade++
                }
              "
            >
              +
            </button>
          </div>
          <div class="subtotal">
            <span>R${{ (item.preco * item.quantidade).toFixed(2).replace('.', ',') }}</span>
          </div>
        </li>
      </ul>
      <h3 class="aviso-carrinho" v-else-if="carrinho.length == 0">
        Não possui nenhum item no carrinho
      </h3>
      <button class="voltar-home" @click="controleDePaginas = 'home'">
        Voltar para loja
      </button>
    </div>
    <div class="compra">
      <div class="cupom">
        <input type="text" placeholder="Código do cupom" />
        <button>Inserir Cupom</button>
      </div>
      <div class="total">
        <h3>Total da Compra</h3>
        <div>
          <p>Produtos:</p>
          <p>R${{ precoTotalProdutos.toFixed(2).replace('.', ',') }}</p>
        </div>
        <div>
          <p>Frete:</p>
          <p>Grátis</p>
        </div>
        <div>
          <p>Total:</p>
          <p>R${{ precoTotalProdutos.toFixed(2).replace('.', ',') }}</p>
        </div>
        <button>Ir para o pagamento</button>
      </div>
    </div>
  </section>

  <!--Favoritos-->
  <section class="favoritos" v-if="controleDePaginas == 'favoritos'">
    <h1>Favoritos</h1>
    <ul v-if="controleFavoritos > 0">
      <li v-for="(item, index) of favoritos" :key="index">
        <div>
          <img :src="item.capa" :alt="item.titulo" />
          <h3>{{ item.titulo }}</h3>
          <p class="autor">{{ item.autor }}</p>
        </div>
          <div class="info">
            <p>R${{ item.preco }}</p>

            <!--coração desfavoritado-->
            <svg
              @click="item.favorito = !item.favorito; controleFavoritos++"
              v-if="item.favorito == false"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 512 512"
            >
              !Font Awesome Free 6.7.2 by @fontawesome - https://fontawesome.com License -
              https://fontawesome.com/license/free Copyright 2025 Fonticons, Inc.
              <path
                d="M225.8 468.2l-2.5-2.3L48.1 303.2C17.4 274.7 0 234.7 0 192.8l0-3.3c0-70.4 50-130.8 119.2-144C158.6 37.9 198.9 47 231 69.6c9 6.4 17.4 13.8 25 22.3c4.2-4.8 8.7-9.2 13.5-13.3c3.7-3.2 7.5-6.2 11.5-9c0 0 0 0 0 0C313.1 47 353.4 37.9 392.8 45.4C462 58.6 512 119.1 512 189.5l0 3.3c0 41.9-17.4 81.9-48.1 110.4L288.7 465.9l-2.5 2.3c-8.2 7.6-19 11.9-30.2 11.9s-22-4.2-30.2-11.9zM239.1 145c-.4-.3-.7-.7-1-1.1l-17.8-20-.1-.1s0 0 0 0c-23.1-25.9-58-37.7-92-31.2C81.6 101.5 48 142.1 48 189.5l0 3.3c0 28.5 11.9 55.8 32.8 75.2L256 430.7 431.2 268c20.9-19.4 32.8-46.7 32.8-75.2l0-3.3c0-47.3-33.6-88-80.1-96.9c-34-6.5-69 5.4-92 31.2c0 0 0 0-.1 .1s0 0-.1 .1l-17.8 20c-.3 .4-.7 .7-1 1.1c-4.5 4.5-10.6 7-16.9 7s-12.4-2.5-16.9-7z"
              />
            </svg>

            <!--coração favoritado-->
            <svg
              @click="removerFavorito(item.id); item.favorito = !item.favorito; controleFavoritos--"
              v-if="item.favorito == true"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 512 512"
            >
              !Font Awesome Free 6.7.2 by @fontawesome - https://fontawesome.com License -
              https://fontawesome.com/license/free Copyright 2025 Fonticons, Inc.
              <path
                d="M47.6 300.4L228.3 469.1c7.5 7 17.4 10.9 27.7 10.9s20.2-3.9 27.7-10.9L464.4 300.4c30.4-28.3 47.6-68 47.6-109.5v-5.8c0-69.9-50.5-129.5-119.4-141C347 36.5 300.6 51.4 268 84L256 96 244 84c-32.6-32.6-79-47.5-124.6-39.9C50.5 55.6 0 115.2 0 185.1v5.8c0 41.5 17.2 81.2 47.6 109.5z"
              />
            </svg>
          </div>
          <button @click="adicionarAoCarrinho(index, item.id)">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 576 512">
              !Font Awesome Free 6.7.2 by @fontawesome - https://fontawesome.com License -
              https://fontawesome.com/license/free Copyright 2025 Fonticons, Inc.
              <path
                d="M0 24C0 10.7 10.7 0 24 0L69.5 0c22 0 41.5 12.8 50.6 32l411 0c26.3 0 45.5 25 38.6 50.4l-41 152.3c-8.5 31.4-37 53.3-69.5 53.3l-288.5 0 5.4 28.5c2.2 11.3 12.1 19.5 23.6 19.5L488 336c13.3 0 24 10.7 24 24s-10.7 24-24 24l-288.3 0c-34.6 0-64.3-24.6-70.7-58.5L77.4 54.5c-.7-3.8-4-6.5-7.9-6.5L24 48C10.7 48 0 37.3 0 24zM128 464a48 48 0 1 1 96 0 48 48 0 1 1 -96 0zm336-48a48 48 0 1 1 0 96 48 48 0 1 1 0-96z"
              />
            </svg>
            Comprar
          </button>
      </li>
    </ul>
    <h3 class="aviso-favoritos" v-if="controleFavoritos == 0">Nenhum item favoritado</h3>
    <button class="voltar-home" @click="controleDePaginas = 'home'">
        Voltar para loja
    </button>
  </section>
  <FooterComponent/>
</template>
<style scoped>
/*==========HEADER===========*/
header svg {
  width: 20px;
  fill: #27ae60;
}
.busca {
  display: flex;
}
.lupa {
  fill: #231f2d;
}

header {
  display: flex;
  justify-content: space-between;
  border-bottom: 1px solid #27ae60;
  align-items: center;
  padding: 1vw 4vw 1vw 4vw;
}

header .logo a {
  display: flex;
  align-items: center;
  cursor: pointer;
}

header .logo h1 {
  border-right: 1px solid #27ae60;
  color: #231f2d;
  font-size: 1.3rem;
  padding-right: 10px;
}

header .logo p {
  color: #27ae60;
  padding-left: 10px;
}
header button {
  border: none;
  background: #f1f1f1;
  border-radius: 0%;
}
header input {
  border: none;
  border-radius: 0%;
  background-color: #f1f1f1;
  padding: 10px 20px;
  width: 450px;
  margin-left: 80px;
  font-size: 1rem;
}

header nav {
  display: flex;
}

header ul {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

header .icons {
  align-items: center;
}
header .icons li a {
  cursor: pointer;
}
header ul li {
  list-style: none;
  margin: 10px 0 10px 20px;
}

header .border {
  border-right: 1px solid #27ae60;
  padding-right: 10px;
}

header ul li a p {
  color: gray;
}

/*=========HOME======== */
button {
  cursor: pointer;
}
div.home {
  animation: enter ease-in 0.5s;
}
@keyframes enter {
  from {
    transform: translateX(-50%);
    filter: blur(10px);
    opacity: 0;
  }
  to {
    transform: translateX(0);
    filter: blur(0);
    opacity: 1;
  }
}
section.destaques {
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 2% 10%;
}

section.destaques div:nth-child(1) {
  margin: 0 10% 0 0;
}

section.destaques div:nth-child(1) span {
  border: solid 1px #27ae60;
  border-radius: 2px;
  padding: 10px 7px;
  color: #27ae60;
}

section.destaques div:nth-child(1) h1 {
  font-size: 350%;
  margin: 1.8vw 0;
  font-weight: 700;
  color: #382c2c;
}

section.destaques div:nth-child(1) p {
  color: #4d4c4c;
  margin: 0 12.5vw 0 0;
  font-size: 100%;
}

section.destaques div:nth-child(1) a {
  text-decoration: none;
}

section.destaques div:nth-child(1) a p {
  margin-top: 1.8vw;
  background-color: #27ae60;
  border-radius: 2px;
  color: white;
  width: 35%;
  text-align: center;
  padding: 12px 0;
  font-size: 100%;
}
section.destaques div:nth-child(2) p {
  color: #313131;
  text-align: right;
  margin-top: -3vw;
}
/*--------SERVIÇOS------------*/
section.servicos {
  padding: 6vw 4vw;
  border-top: #27ae60 solid 1px;
  border-bottom: #27ae60 solid 1px;
}
section.servicos ul {
  display: flex;
  align-items: center;
  justify-content: space-around;
}
section.servicos ul li {
  display: flex;
  align-items: center;
  height: 100px;
  padding: 0 3vw;
}
section.servicos ul li.center {
  border-right: #937dc2 1px solid;
  border-left: #937dc2 1px solid;
}
section.servicos ul li svg {
  fill: #382c2c;
  width: 50px;
  margin-right: 2vw;
}
section.servicos ul li p {
  font-size: 170%;
  font-weight: 600;
}
/*--------LANÇAMENTOS------------*/

/*======CARRINHO======= */
section.carrinho {
  color: #382c2c;
  margin: 8vw 6vw 0 6vw;
  animation: enter ease-in 0.5s;
}
section.carrinho h1 {
  color: #27ae60;
  font-size: 2.4rem;
  font-weight: 500;
  margin-bottom: 3vw;
}
section.carrinho .topo {
  border-bottom: solid 2px #27ae60;
  display: flex;
  justify-content: space-between;
}
section.carrinho .topo h2 {
  color: #382c2c;
  font-size: 1.5rem;
  font-weight: 500;
  margin: 0 2vw 1vw 2vw;
}
section.carrinho .topo h2:nth-child(2) {
  margin-left: 12vw;
}
section.carrinho .corpo ul li {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin: 0.5vw;
  padding: 1.5vw;
  border-bottom: 2px solid #bdbdbd;
}
section.carrinho .corpo h3.aviso-carrinho {
  text-align: center;
  margin: 4vw 0;
  font-size: 200%;
  font-weight: 500;
}
section.carrinho .corpo ul li .produto {
  display: flex;
  height: 100%;
}
section.carrinho .corpo ul li .produto img {
  width: 120px;
  height: 70%;
  border-radius: 3px;
}
section.carrinho .corpo ul li .produto .descricao {
  margin: 0 8.5vw 0 2vw;
  width: 300px;
}
section.carrinho .corpo ul li .produto .descricao h3 {
  color: #382c2c;
  font-size: 1.5rem;
  font-weight: 500;
}
section.carrinho .corpo ul li .produto .descricao p {
  color: #4f4c57;
}
section.carrinho .corpo ul li .produto .descricao span {
  color: #382c2c;
  font-size: 1.5rem;
  font-weight: 500;
}
section.carrinho .corpo ul li .quantidade {
  border: 1px solid #000;
  display: flex;
  justify-content: space-around;
  padding: 0.5vw 1.8vw;
  margin-left: -19.5vw;
}
section.carrinho .corpo ul li .quantidade button {
  background: none;
  border: none;
  font-size: 1.5rem;
}
section.carrinho .corpo ul li .quantidade p {
  font-size: 1.5rem;
  margin: 0 10px;
}
section.carrinho .corpo ul li .subtotal span {
  color: #382c2c;
  font-size: 1.5rem;
  font-weight: 500;
  margin-right: 1.5vw;
}
section.carrinho .corpo .voltar-home {
  margin: 2vw 0 5vw 0;
  padding: 1vw 3vw;
  background-color: transparent;
  border: #000 1px solid;
  border-radius: 5px;
  font-size: 1rem;
  font-weight: 500;
}
section.carrinho .compra {
  display: flex;
  justify-content: space-between;
  margin-bottom: 10vw;
}
section.carrinho .compra .cupom {
  display: flex;
  height: 50%;
}
section.carrinho .compra .cupom input {
  margin-right: 0.8vw;
  padding: 1vw 3vw 1vw 1vw;
  background-color: transparent;
  border: #000 1px solid;
  border-radius: 5px;
  font-size: 1rem;
  font-weight: 500;
  font-weight: normal;
}
section.carrinho .compra .cupom button {
  color: white;
  font-weight: 500;
  font-size: 1rem;
  background-color: #27ae60;
  border: none;
  border-radius: 5px;
  padding: 1vw 3vw;
}
section.carrinho .compra .total {
  border: 2px #000 solid;
  border-radius: 5px;
  padding: 2vw 1vw;
  width: 30%;
  text-align: center;
}
section.carrinho .compra .total h3 {
  font-size: 1.5rem;
  font-weight: 500;
  margin: 0 0 2vw 0;
}
section.carrinho .compra .total div {
  display: flex;
  justify-content: space-between;
  border-bottom: solid 1px #000;
  font-size: 1.5rem;
  margin-bottom: 1vw;
  padding-bottom: 1vw;
}
section.carrinho .compra .total button {
  background-color: #27ae60;
  border: none;
  border-radius: 5px;
  text-align: center;
  color: #fff;
  padding: 1vw 4vw;
  font-size: 1.5rem;
}
/*=======FAVORITOS=======*/
section.favoritos{
  margin: 8vw 4vw;
  animation: enter ease-in 0.5s;
}
section.favoritos h1{
  color: #27ae60;
  font-size: 2.5rem;
  margin-bottom: 2vw;
  font-weight: 500;
}
section.favoritos ul{
  display: flex;
  flex-wrap: wrap;
}
section.favoritos ul li{
  margin: 1vw 2vw;
  width: 20%;
}
section.favoritos ul li  img{
  width: 100%;
}
section.favoritos ul li  p.autor{
  color: #4d4c4c;
  margin: 1vw 0;
}
section.favoritos ul li div.info{
  display: flex;
  justify-content: space-between;
}
section.favoritos ul li div.info p{
  font-size: 130%;
}
section.favoritos ul li div.info svg{
  fill: #27ae60;
  width: 25px;
  cursor: pointer;
}
section.favoritos ul li button {
  width: 100%;
  background: #27ae60;
  color: #fff;
  padding: 10px 0;
  border-radius: 2px;
  border: none;
  font-size: 120%;
  margin-top: 1vw;
}
section.favoritos h3.aviso-favoritos{
  text-align: center;
  font-size: 2rem;
}
section.favoritos button.voltar-home{
  margin: 2vw 0 0 0;
  padding: 1vw 3vw;
  background-color: transparent;
  border: #000 1px solid;
  border-radius: 5px;
  font-size: 1rem;
  font-weight: 500;
}

</style>
