<script setup>

</script>

<template>

    <header>
        <div class="logo">
            <h1>IFbooks</h1>
            <p>
                Apreço a leitura
            </p>
        </div>
        <input type="text" placeholder="Buscar">
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
            <ul>
                <li>
                    <a href="">
                        <i class="fa-solid fa-cart-shopping"></i>
                    </a>
                </li>
                <li>
                    <a href="">

                    </a>
                </li>
                <li>
                    <a href="">

                    </a>
                </li>
            </ul>
        </nav>
    </header>
</template>

<style scoped>
header {
    display: flex;
    justify-content: space-between;
    border-bottom: 1px solid #27AE60;
    align-items: center;
}

.logo {
    display: flex;
    align-items: center;
}

.logo h1 {
    border-right: 1px solid #27AE60;
    color: #231F2D;
}

.logo p {
    color: #27AE60;
}

ul {
    display: flex;
}

ul li {
    list-style: none;
}

ul li a p {
    color: gray;
    text-decoration: none;
}
</style>