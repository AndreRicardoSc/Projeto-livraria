<script setup>

</script>

<template>
    <header>
        <div class="logo">
            <a href="">
                <h1>IFbooks</h1>
                <p>
                    Apreço a leitura
                </p>
            </a>
        </div>
        <div class="busca">
            <input type="text" placeholder="Buscar">
            <svg class="lupa" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512">!Font Awesome Free 6.7.2 by
                @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2025
                Fonticons, Inc.
                <path
                    d="M416 208c0 45.9-14.9 88.3-40 122.7L502.6 457.4c12.5 12.5 12.5 32.8 0 45.3s-32.8 12.5-45.3 0L330.7 376c-34.4 25.2-76.8 40-122.7 40C93.1 416 0 322.9 0 208S93.1 0 208 0S416 93.1 416 208zM208 352a144 144 0 1 0 0-288 144 144 0 1 0 0 288z" />
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
                        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 576 512">!Font Awesome Free 6.7.2 by
                            @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free
                            Copyright 2025 Fonticons, Inc.
                            <path
                                d="M0 24C0 10.7 10.7 0 24 0L69.5 0c22 0 41.5 12.8 50.6 32l411 0c26.3 0 45.5 25 38.6 50.4l-41 152.3c-8.5 31.4-37 53.3-69.5 53.3l-288.5 0 5.4 28.5c2.2 11.3 12.1 19.5 23.6 19.5L488 336c13.3 0 24 10.7 24 24s-10.7 24-24 24l-288.3 0c-34.6 0-64.3-24.6-70.7-58.5L77.4 54.5c-.7-3.8-4-6.5-7.9-6.5L24 48C10.7 48 0 37.3 0 24zM128 464a48 48 0 1 1 96 0 48 48 0 1 1 -96 0zm336-48a48 48 0 1 1 0 96 48 48 0 1 1 0-96z" />
                        </svg>
                    </a>
                </li>
                <li>
                    <a href="" class="border">
                        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512">!Font Awesome Free 6.7.2 by
                            @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free
                            Copyright 2025 Fonticons, Inc.
                            <path
                                d="M47.6 300.4L228.3 469.1c7.5 7 17.4 10.9 27.7 10.9s20.2-3.9 27.7-10.9L464.4 300.4c30.4-28.3 47.6-68 47.6-109.5v-5.8c0-69.9-50.5-129.5-119.4-141C347 36.5 300.6 51.4 268 84L256 96 244 84c-32.6-32.6-79-47.5-124.6-39.9C50.5 55.6 0 115.2 0 185.1v5.8c0 41.5 17.2 81.2 47.6 109.5z" />
                        </svg>
                    </a>
                </li>
                <li>
                    <a href="">
                        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512">!Font Awesome Free 6.7.2 by
                            @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free
                            Copyright 2025 Fonticons, Inc.
                            <path
                                d="M224 256A128 128 0 1 0 224 0a128 128 0 1 0 0 256zm-45.7 48C79.8 304 0 383.8 0 482.3C0 498.7 13.3 512 29.7 512l388.6 0c16.4 0 29.7-13.3 29.7-29.7C448 383.8 368.2 304 269.7 304l-91.4 0z" />
                        </svg>
                    </a>
                </li>
            </ul>
        </nav>
    </header>
</template>

<style scoped>
a {
    text-decoration: none;
}

svg {
    width: 20px;
    fill: #27AE60;
}
.busca{
    display: flex;
}
.lupa {
    position: absolute;
    transform: translate(1100%, 50%);
    fill: #231F2D;
}

header {
    display: flex;
    justify-content: space-between;
    border-bottom: 1px solid #27AE60;
    align-items: center;
    padding: 1vw 4vw 1vw 4vw;
}

.logo a {
    display: flex;
    align-items: center;
}

.logo h1 {
    border-right: 1px solid #27AE60;
    color: #231F2D;
    font-size: 1.3rem;
    padding-right: 10px;
}

.logo p {
    color: #27AE60;
    padding-left: 10px;
}

input {
    border: none;
    border-radius: 0%;
    background-color: #F1F1F1;
    padding: 10px 20px;
    width: 100%;
    font-size: 1rem;
}

nav {
    display: flex;
}

ul {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.icons {
    align-items: center;
}

ul li {
    list-style: none;
    margin: 10px 0 10px 20px;
}

.border {
    border-right: 1px solid #27AE60;
    padding-right: 10px;
}

ul li a p {
    color: gray;
}
</style>