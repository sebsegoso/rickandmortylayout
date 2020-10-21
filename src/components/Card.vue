<template>
<v-col cols="12" xs="6" sm="4" align="center">
    <div class="wrapper">
        <v-card max-width="350">
            <v-img :src="imagen"></v-img>

            <div class="card-body">
                <v-card-title> {{ id }} - {{ nombre }} </v-card-title>
            </div>
        </v-card>
    </div>
</v-col>
</template>

<script>
export default {
    name: "Card",
    props: ["id", "nombre", "imagen"],
    data: () => ({
        show: false,
    }),
};
</script>

<style lang="scss" scoped>
.wrapper {
    padding: 20px;
}
</style>
