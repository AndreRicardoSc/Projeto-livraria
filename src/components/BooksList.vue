<script setup>
    defineEmits(['add-book-cart','add-book-fav','remove-book-fav','like','unlike'])
    defineProps(['products'])
</script>
<template>
    <section class="lancamentos">
      <h2>Lançamentos</h2>
      <ul>
        <li class="livros" v-for="(item, index) of products" :key="index">
          <img :src="item.capa" :alt="item.titulo" />
          <h3>{{ item.titulo }}</h3>
          <p class="autor">{{ item.autor }}</p>
          <div class="info">
            <p>R${{ item.preco }}</p>

            <!--coração desfavoritado-->
            <svg
              @click="$emit('add-book-fav', item); $emit('like', item)"
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
              @click="$emit('remove-book-fav', item); $emit('unlike', item)"
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
          <button @click="$emit('add-book-cart', index, item.id)">
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
    </section>
</template>
<style scoped>
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
  color: #4f4c57;
}
section.lancamentos ul li div.info {
  display: flex;
  justify-content: space-between;
}
section.lancamentos ul li div.info p {
  font-size: 130%;
}
section.lancamentos ul li div.info svg {
  fill: #27ae60;
  width: 25px;
  cursor: pointer;
}
section.lancamentos ul li div.button {
  background-color: #000;
}

section.lancamentos ul li button {
  width: 100%;
  background: #27ae60;
  color: #fff;
  padding: 10px 0;
  border-radius: 2px;
  border: none;
  font-size: 120%;
}
</style>
