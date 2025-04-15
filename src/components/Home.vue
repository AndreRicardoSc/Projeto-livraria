<script setup>
    import { ref } from "vue";
    const produtos = ref([
        {
            id: 1,
            titulo: "Chain of Iron: Volume 2",
            autor: "Cassandra Clare",
            preco: 23.24,
        },
        {
            id: 2,
            titulo: "Chain of Thorns",
            autor: "Cassandra Clare",
            preco: 23.24,
        },
        {
            id: 3,
            titulo: "City of Fallen",
            autor: "Cassandra Clare",
            preco: 13.94,
        },
        {
            id: 4,
            titulo: "Nona the Ninth",
            autor: "Cassandra Clare",
            preco: 16.84,
        },
        {
            id: 5,
            titulo: "Harlem Shuffle",
            autor: "Colson Whitehead",
            preco: 26.92,
        },
        {
            id: 6,
            titulo: "Two Old Women",
            autor: "Velma Wallis",
            preco: 13.95,
        },
        {
            id: 7,
            titulo: "Carrie Soto Is Back",
            autor: "Taylor Jenkins Reid",
            preco: 26.04,
        },
        {
            id: 8,
            titulo: "Book Lovers",
            autor: "Emily Henry",
            preco: 15.81,
        },
    ]);
</script>

<template>
    <div class="home">
        <section class="lancamentos">
            <h2>Lançamentos</h2>
            <ul>
                <li class="livros" v-for="(item, index) of produtos" :key="index">
                    {{ item.titulo }}
                </li>
            </ul>
        </section>
    </div>
</template>

<style scoped>

</style>