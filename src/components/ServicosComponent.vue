<script setup>

</script>
<template>
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
</template>
<style scoped>
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
</style>
