<script setup>
  import { ref } from 'vue';
const produtos = ref([
  {
    id: 1,
    titulo: 'Chain of Iron: Volume 2',
    autor: 'Cassandra Clare',
    preco: 23.24,
    capa: "/src/assets/imgs/chainofironv2.png"
  },
  {
    id: 2,
    titulo: 'Chain of Thorns',
    autor: 'Cassandra Clare',
    preco: 23.24,
    capa: "/src/assets/imgs/chainofthorns.png"
  },
  {
    id: 3,
    titulo: 'City of Fallen',
    autor: 'Cassandra Clare',
    preco: 13.94,
    capa: "/src/assets/imgs/cityoffallenangels.png"
  },
  {
    id: 4,
    titulo: 'Nona the Ninth',
    autor: 'Cassandra Clare',
    preco: 16.84,
    capa: "/src/assets/imgs/nonatheninth.png"
  },
  {
    id: 5,
    titulo: 'Harlem Shuffle',
    autor: 'Colson Whitehead',
    preco: 26.92,
    capa: "/src/assets/imgs/harlemshuffle.png"
  },
  {
    id: 6,
    titulo: 'Two Old Women',
    autor: 'Velma Wallis',
    preco: 13.95,
    capa: "/src/assets/imgs/twooldwomen.png"
  },
  {
    id: 7,
    titulo: 'Carrie Soto Is Back',
    autor: 'Taylor Jenkins Reid',
    preco: 26.04,
    capa: "/src/assets/imgs/carriesotoisback.png"
  },
  {
    id: 8,
    titulo: 'Book Lovers',
    autor: 'Emily Henry',
    preco: 15.81,
    capa: "/src/assets/imgs/booklovers.png"
  },
])
</script>
<template>
  <header>
    <div class="logo">
      <a href="">
        <h1>IFbooks</h1>
        <p>Apreço a leitura</p>
      </a>
    </div>
    <div class="busca">
      <input type="text" placeholder="Buscar" />
      <svg class="lupa" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512">
        !Font Awesome Free 6.7.2 by @fontawesome - https://fontawesome.com License -
        https://fontawesome.com/license/free Copyright 2025 Fonticons, Inc.
        <path
          d="M416 208c0 45.9-14.9 88.3-40 122.7L502.6 457.4c12.5 12.5 12.5 32.8 0 45.3s-32.8 12.5-45.3 0L330.7 376c-34.4 25.2-76.8 40-122.7 40C93.1 416 0 322.9 0 208S93.1 0 208 0S416 93.1 416 208zM208 352a144 144 0 1 0 0-288 144 144 0 1 0 0 288z"
        />
      </svg>
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
          <a href="" class="border">
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
          <a href="" class="border">
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
          <a href="">
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
  <div class="home">
    <section class="destaques">
      <div>
        <span>Autor de Abril</span>
        <h1>Eric-Emanuel Schmitt</h1>
        <p>
          Eric-Emmanuel Schmitt has been awarded more than 20 literary prizes and distinctions, and in 2001 he received
          the title of Chevalier des Arts et des Lettres. His books have been translated into over 40 languages.
        </p>
        <a href="">
          <p>Acessar página do livro</p>
        </a>
      </div>
      <div>
        <img src="/src/assets/imgs/Schmitt_Nocognia_3D_500pcx 1.png" alt="livro">
        <p>*within the stock limit</p>
      </div>
    </section>
    <section class="servicos">
      <ul>
        <li>
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 640 512">!Font Awesome Free 6.7.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2025 Fonticons, Inc.<path d="M48 0C21.5 0 0 21.5 0 48L0 368c0 26.5 21.5 48 48 48l16 0c0 53 43 96 96 96s96-43 96-96l128 0c0 53 43 96 96 96s96-43 96-96l32 0c17.7 0 32-14.3 32-32s-14.3-32-32-32l0-64 0-32 0-18.7c0-17-6.7-33.3-18.7-45.3L512 114.7c-12-12-28.3-18.7-45.3-18.7L416 96l0-48c0-26.5-21.5-48-48-48L48 0zM416 160l50.7 0L544 237.3l0 18.7-128 0 0-96zM112 416a48 48 0 1 1 96 0 48 48 0 1 1 -96 0zm368-48a48 48 0 1 1 0 96 48 48 0 1 1 0-96z"/></svg>
          <p>
            Frete grátis para SC
          </p>
        </li>
        <li class="center">
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 576 512">!Font Awesome Free 6.7.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2025 Fonticons, Inc.<path d="M316.9 18C311.6 7 300.4 0 288.1 0s-23.4 7-28.8 18L195 150.3 51.4 171.5c-12 1.8-22 10.2-25.7 21.7s-.7 24.2 7.9 32.7L137.8 329 113.2 474.7c-2 12 3 24.2 12.9 31.3s23 8 33.8 2.3l128.3-68.5 128.3 68.5c10.8 5.7 23.9 4.9 33.8-2.3s14.9-19.3 12.9-31.3L438.5 329 542.7 225.9c8.6-8.5 11.7-21.2 7.9-32.7s-13.7-19.9-25.7-21.7L381.2 150.3 316.9 18z"/></svg>
          <p>
            Livros recomendados
          </p>
        </li>
        <li>
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 576 512">!Font Awesome Free 6.7.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2025 Fonticons, Inc.<path d="M249.6 471.5c10.8 3.8 22.4-4.1 22.4-15.5l0-377.4c0-4.2-1.6-8.4-5-11C247.4 52 202.4 32 144 32C93.5 32 46.3 45.3 18.1 56.1C6.8 60.5 0 71.7 0 83.8L0 454.1c0 11.9 12.8 20.2 24.1 16.5C55.6 460.1 105.5 448 144 448c33.9 0 79 14 105.6 23.5zm76.8 0C353 462 398.1 448 432 448c38.5 0 88.4 12.1 119.9 22.6c11.3 3.8 24.1-4.6 24.1-16.5l0-370.3c0-12.1-6.8-23.3-18.1-27.6C529.7 45.3 482.5 32 432 32c-58.4 0-103.4 20-123 35.6c-3.3 2.6-5 6.8-5 11L304 456c0 11.4 11.7 19.3 22.4 15.5z"/></svg>
          <p>
            Mais vendidos
          </p>
        </li>
      </ul>
    </section>
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
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 576 512">!Font Awesome Free 6.7.2 by @fontawesome -
              https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2025 Fonticons, Inc.
              <path
                d="M0 24C0 10.7 10.7 0 24 0L69.5 0c22 0 41.5 12.8 50.6 32l411 0c26.3 0 45.5 25 38.6 50.4l-41 152.3c-8.5 31.4-37 53.3-69.5 53.3l-288.5 0 5.4 28.5c2.2 11.3 12.1 19.5 23.6 19.5L488 336c13.3 0 24 10.7 24 24s-10.7 24-24 24l-288.3 0c-34.6 0-64.3-24.6-70.7-58.5L77.4 54.5c-.7-3.8-4-6.5-7.9-6.5L24 48C10.7 48 0 37.3 0 24zM128 464a48 48 0 1 1 96 0 48 48 0 1 1 -96 0zm336-48a48 48 0 1 1 0 96 48 48 0 1 1 0-96z" />
            </svg>
            Comprar
          </button>
        </li>
      </ul>
    </section>
  </div>
  <footer>
    <div class="contatos">
      <div>
        <h2>IFbooks</h2>
        <ul>
          <li>
            <a href="https://facebook.com">
              <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512">
                !Font Awesome Free 6.7.2 by @fontawesome - https://fontawesome.com License -
                https://fontawesome.com/license/free Copyright 2025 Fonticons, Inc.
                <path
                  d="M64 32C28.7 32 0 60.7 0 96V416c0 35.3 28.7 64 64 64h98.2V334.2H109.4V256h52.8V222.3c0-87.1 39.4-127.5 125-127.5c16.2 0 44.2 3.2 55.7 6.4V172c-6-.6-16.5-1-29.6-1c-42 0-58.2 15.9-58.2 57.2V256h83.6l-14.4 78.2H255V480H384c35.3 0 64-28.7 64-64V96c0-35.3-28.7-64-64-64H64z"
                />
              </svg>
            </a>
          </li>
          <li>
            <a href="https://instagram.com">
              <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512">
                !Font Awesome Free 6.7.2 by @fontawesome - https://fontawesome.com License -
                https://fontawesome.com/license/free Copyright 2025 Fonticons, Inc.
                <path
                  d="M194.4 211.7a53.3 53.3 0 1 0 59.3 88.7 53.3 53.3 0 1 0 -59.3-88.7zm142.3-68.4c-5.2-5.2-11.5-9.3-18.4-12c-18.1-7.1-57.6-6.8-83.1-6.5c-4.1 0-7.9 .1-11.2 .1c-3.3 0-7.2 0-11.4-.1c-25.5-.3-64.8-.7-82.9 6.5c-6.9 2.7-13.1 6.8-18.4 12s-9.3 11.5-12 18.4c-7.1 18.1-6.7 57.7-6.5 83.2c0 4.1 .1 7.9 .1 11.1s0 7-.1 11.1c-.2 25.5-.6 65.1 6.5 83.2c2.7 6.9 6.8 13.1 12 18.4s11.5 9.3 18.4 12c18.1 7.1 57.6 6.8 83.1 6.5c4.1 0 7.9-.1 11.2-.1c3.3 0 7.2 0 11.4 .1c25.5 .3 64.8 .7 82.9-6.5c6.9-2.7 13.1-6.8 18.4-12s9.3-11.5 12-18.4c7.2-18 6.8-57.4 6.5-83c0-4.2-.1-8.1-.1-11.4s0-7.1 .1-11.4c.3-25.5 .7-64.9-6.5-83l0 0c-2.7-6.9-6.8-13.1-12-18.4zm-67.1 44.5A82 82 0 1 1 178.4 324.2a82 82 0 1 1 91.1-136.4zm29.2-1.3c-3.1-2.1-5.6-5.1-7.1-8.6s-1.8-7.3-1.1-11.1s2.6-7.1 5.2-9.8s6.1-4.5 9.8-5.2s7.6-.4 11.1 1.1s6.5 3.9 8.6 7s3.2 6.8 3.2 10.6c0 2.5-.5 5-1.4 7.3s-2.4 4.4-4.1 6.2s-3.9 3.2-6.2 4.2s-4.8 1.5-7.3 1.5l0 0c-3.8 0-7.5-1.1-10.6-3.2zM448 96c0-35.3-28.7-64-64-64H64C28.7 32 0 60.7 0 96V416c0 35.3 28.7 64 64 64H384c35.3 0 64-28.7 64-64V96zM357 389c-18.7 18.7-41.4 24.6-67 25.9c-26.4 1.5-105.6 1.5-132 0c-25.6-1.3-48.3-7.2-67-25.9s-24.6-41.4-25.8-67c-1.5-26.4-1.5-105.6 0-132c1.3-25.6 7.1-48.3 25.8-67s41.5-24.6 67-25.8c26.4-1.5 105.6-1.5 132 0c25.6 1.3 48.3 7.1 67 25.8s24.6 41.4 25.8 67c1.5 26.3 1.5 105.4 0 131.9c-1.3 25.6-7.1 48.3-25.8 67z"
                />
              </svg>
            </a>
          </li>
          <li>
            <a href="https://twitter.com">
              <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512">
                !Font Awesome Free 6.7.2 by @fontawesome - https://fontawesome.com License -
                https://fontawesome.com/license/free Copyright 2025 Fonticons, Inc.
                <path
                  d="M64 32C28.7 32 0 60.7 0 96V416c0 35.3 28.7 64 64 64H384c35.3 0 64-28.7 64-64V96c0-35.3-28.7-64-64-64H64zM351.3 199.3v0c0 86.7-66 186.6-186.6 186.6c-37.2 0-71.7-10.8-100.7-29.4c5.3 .6 10.4 .8 15.8 .8c30.7 0 58.9-10.4 81.4-28c-28.8-.6-53-19.5-61.3-45.5c10.1 1.5 19.2 1.5 29.6-1.2c-30-6.1-52.5-32.5-52.5-64.4v-.8c8.7 4.9 18.9 7.9 29.6 8.3c-9-6-16.4-14.1-21.5-23.6s-7.8-20.2-7.7-31c0-12.2 3.2-23.4 8.9-33.1c32.3 39.8 80.8 65.8 135.2 68.6c-9.3-44.5 24-80.6 64-80.6c18.9 0 35.9 7.9 47.9 20.7c14.8-2.8 29-8.3 41.6-15.8c-4.9 15.2-15.2 28-28.8 36.1c13.2-1.4 26-5.1 37.8-10.2c-8.9 13.1-20.1 24.7-32.9 34c.2 2.8 .2 5.7 .2 8.5z"
                />
              </svg>
            </a>
          </li>
        </ul>
      </div>
      <div>
        <h2>Contato</h2>
        <ul class="contato-essenciais">
          <li>
            <svg class="contatos" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512">
              !Font Awesome Free 6.7.2 by @fontawesome - https://fontawesome.com License -
              https://fontawesome.com/license/free Copyright 2025 Fonticons, Inc.
              <path
                d="M164.9 24.6c-7.7-18.6-28-28.5-47.4-23.2l-88 24C12.1 30.2 0 46 0 64C0 311.4 200.6 512 448 512c18 0 33.8-12.1 38.6-29.5l24-88c5.3-19.4-4.6-39.7-23.2-47.4l-96-40c-16.3-6.8-35.2-2.1-46.3 11.6L304.7 368C234.3 334.7 177.3 277.7 144 207.3L193.3 167c13.7-11.2 18.4-30 11.6-46.3l-40-96z"
              />
            </svg>
            +55 47 40045263
          </li>
          <li>
            <svg class="contatos" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512">
              !Font Awesome Free 6.7.2 by @fontawesome - https://fontawesome.com License -
              https://fontawesome.com/license/free Copyright 2025 Fonticons, Inc.
              <path
                d="M256 0a256 256 0 1 1 0 512A256 256 0 1 1 256 0zM232 120l0 136c0 8 4 15.5 10.7 20l96 64c11 7.4 25.9 4.4 33.3-6.7s4.4-25.9-6.7-33.3L280 243.2 280 120c0-13.3-10.7-24-24-24s-24 10.7-24 24z"
              />
            </svg>
            8h às 23h - Seg a Sex
          </li>
          <li>
            <svg class="contatos" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512">
              !Font Awesome Free 6.7.2 by @fontawesome - https://fontawesome.com License -
              https://fontawesome.com/license/free Copyright 2025 Fonticons, Inc.
              <path
                d="M48 64C21.5 64 0 85.5 0 112c0 15.1 7.1 29.3 19.2 38.4L236.8 313.6c11.4 8.5 27 8.5 38.4 0L492.8 150.4c12.1-9.1 19.2-23.3 19.2-38.4c0-26.5-21.5-48-48-48L48 64zM0 176L0 384c0 35.3 28.7 64 64 64l384 0c35.3 0 64-28.7 64-64l0-208L294.4 339.2c-22.8 17.1-54 17.1-76.8 0L0 176z"
              />
            </svg>
            contato@ifbooks.com
          </li>
        </ul>
        <ul class="cartoes">
          <li>
            <img src="/public/imgs/footer/paipal 1.png" alt="paypal-img" />
          </li>
          <li>
            <img src="/public/imgs/footer/MasterCard-Logo-1979 1.png" alt="master-card-img" />
          </li>
          <li>
            <img src="/public/imgs/footer/VISA-card-logo- 1.png" alt="" />
          </li>
        </ul>
      </div>
    </div>
    <div class="direitos">
      <p>&copy; Alguns direitos reservados. IFbooks 2025.</p>
    </div>
  </footer>
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
  position: absolute;
  transform: translate(1100%, 50%);
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

header input {
  border: none;
  border-radius: 0%;
  background-color: #f1f1f1;
  padding: 10px 20px;
  width: 100%;
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
svg {
  width: 20px;
  fill: #fff;
}
button {
  cursor: pointer;
}

section.destaques {
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 2vw 13vw;
}

section.destaques div:nth-child(1) {
  margin: 0 14vw 0 0;
}

section.destaques div:nth-child(1) span {
  border: solid 1px #27AE60;
  border-radius: 2px;
  padding: 10px 7px;
  color: #27AE60;
}

section.destaques div:nth-child(1) h1 {
  font-size: 3.8rem;
  margin: 1.8vw 0;
  font-weight: 700;
  color: #382C2C;
}

section.destaques div:nth-child(1) p {
  color: #4D4C4C;
  margin: 0 12.5vw 0 0;
}

section.destaques div:nth-child(1) a {
  text-decoration: none;
}

section.destaques div:nth-child(1) a p {
  margin-top: 1.8vw;
  background-color: #27AE60;
  border-radius: 2px;
  color: white;
  width: 35%;
  text-align: center;
  padding: 12px 0;
}
section.destaques div:nth-child(2) p {
  color: #313131;
  text-align: right;
  margin-top: -3vw;
}

ul, ol, li{
  list-style: none;
}
button {
  cursor: pointer;
}
/*--------SERVIÇOS------------*/
section.servicos{
  padding: 6vw 4vw;
  border-top: #27AE60 solid 1px;
  border-bottom: #27AE60 solid 1px;
}
section.servicos ul{
  display: flex;
  align-items: center;
  justify-content: space-around;
}
section.servicos ul li{
  display: flex;
  align-items: center;
  height: 100px;
  padding: 0 3vw;
}
section.servicos ul li.center{
  border-right: #937DC2 1px solid;
  border-left: #937DC2 1px solid;
}
section.servicos ul li svg{
  fill: #382C2C;
  width: 50px;
  margin-right: 2vw;
}
section.servicos ul li p{
  font-size: 170%;
  font-weight: 600;
}
/*--------LANÇAMENTOS------------*/
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
  margin: 2vw 2px;
  padding: 0;
  font-size: 130%;
}

section.lancamentos ul li img {
  width: 100%;
}

section.lancamentos ul li p {
  margin: 1vw 0;
}

section.lancamentos ul li p.autor {
  color: #4F4C57;
}

section.lancamentos ul li div.info p {
  font-size: 130%;
}

section.lancamentos ul li div.button {
  background-color: #000;
}

section.lancamentos ul li button {
  width: 100%;
  background: #27AE60;
  color: #fff;
  padding: 10px 0;
  border-radius: 2px;
  border: none;
  font-size: 120%;
}

section.lancamentos ul li button:hover {
  background: #27AE60;
}
/*======FOOTER======= */
svg.contatos {
  width: 20px;
}
footer {
  background: #27ae60;
  color: #fff;
}
footer ul li {
  list-style: none;
}
footer div.contatos {
  display: flex;
  justify-content: space-between;
  padding: 3vw 6vw;
}
footer div.contatos h2 {
  font-weight: bold;
}
footer div.contatos ul {
  display: flex;
  margin: 2vw 0;
}
footer div.contatos ul li {
  margin: 0 1vw;
  font-size: 20px;
  font-weight: 300;
  transform: translateX(-25%);
}
footer div.contatos ul.contato-essenciais {
  display: block;
}
footer div.direitos {
  border-top: solid 1px;
  padding: 1vw 0;
  opacity: 60%;
  text-align: center;
}
</style>
