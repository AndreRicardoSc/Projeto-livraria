<script setup></script>

<template>
  <div class="footer">
    <div class="contatos">
      <div>
        <h2>IFbooks</h2>
        <ul>
          <li>
            <a href="https://facebook.com">Facebook</a>
          </li>
          <li>
            <a href="https://instagram.com">Instagram</a>
          </li>
          <li>
            <a href="https://twitter.com">Twitter</a>
          </li>
        </ul>
      </div>
      <div>
        <h2>Contato</h2>
        <ul class="contato-essenciais">
          <li>+55 47 40045263</li>
          <li>8h às 23h - Seg a Sex</li>
          <li>contato@ifbooks.com</li>
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
  </div>
</template>

<style scoped>
* {
  color: #fff;
}
a {
  text-decoration: none;
}
ul li {
  list-style: none;
}
div.footer {
  background: #27ae60;
}
div.footer div.contatos{
    display: flex;
    justify-content: space-between;
    padding: 3vw 6vw;
}
div.footer div.contatos ul{
    display: flex;
    margin: 2vw 0;
}
div.footer div.contatos ul li{
    margin: 0 1vw;
}
div.footer div.contatos ul.contato-essenciais{
    display: block;
}
div.footer div.direitos{
    border-top: solid 1px;
    padding: 1vw 0;
    opacity: 60%;
    text-align: center;
}
</style>
