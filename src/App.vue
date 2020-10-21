<template>
<v-card class="overflow-hidden">
    <v-app-bar absolute color="white" elevate-on-scroll scroll-target="#scrolling-techniques-7">
        <v-app-bar-nav-icon></v-app-bar-nav-icon>

        <v-toolbar-title>Rick and morty</v-toolbar-title>

        <v-spacer></v-spacer>
        <p class="navbar-link">Inicio</p>

        <p class="navbar-link">Buscar</p>

        <p class="navbar-link">Acerca de</p>
    </v-app-bar>

    <v-sheet id="scrolling-techniques-7" class="overflow-y-auto main" min-height="100vh">
        <v-container fluid>
            <v-row no-gutters>
                <Card v-for="personaje in personajes" :key="personaje.id" :id="personaje.id" :nombre="personaje.nombre" :imagen="personaje.imagen" />
            </v-row>
        </v-container>
    </v-sheet>
</v-card>
</template>

<script>
import Card from "./components/Card";

export default {
    name: "App",

    components: {
        Card,
    },

    data: () => ({
        personajes: [{
                id: 1,
                nombre: "Morty",
                imagen: "https://rickandmortyapi.com/api/character/avatar/2.jpeg",
            },
            {
                id: 2,
                nombre: "Rick",
                imagen: "https://rickandmortyapi.com/api/character/avatar/1.jpeg",
            },
            {
                id: 3,
                nombre: "Summer",
                imagen: "https://rickandmortyapi.com/api/character/avatar/3.jpeg",
            },
            {
                id: 4,
                nombre: "Beth",
                imagen: "https://rickandmortyapi.com/api/character/avatar/4.jpeg",
            },
            {
                id: 5,
                nombre: "Jerry",
                imagen: "https://rickandmortyapi.com/api/character/avatar/5.jpeg",
            },
        ],
    }),
};
</script>

<style lang="scss">
body {
    font-family: Arial, Helvetica, sans-serif;
}

.main {
    padding-top: 80px;
}

.navbar-link {
    text-decoration: none;
    color: #000;
    padding: 0 10px;

    &:hover {
        border-bottom: 2px solid #000;
        cursor: pointer;
    }

    &:active {
        border-bottom: 2px solid #000;
    }
}
</style>
