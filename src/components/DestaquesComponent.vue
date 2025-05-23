<script setup>

</script>
<template>
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
</template>
<style scoped>
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
</style>
