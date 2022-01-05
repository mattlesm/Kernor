<template>
    <v-container>
        <div
            v-for="histoire of raceList.histoires"
            :key="histoire.id"
        >
            <v-row :align="align" class="first-row"> 
                <v-col>
                    <h3>{{ histoire.titre }}</h3>
                </v-col>
            </v-row>

            <v-row>
                <v-col>
                    <v-divider inset></v-divider>
                </v-col>
            </v-row>

            <v-row class="rows"
                v-for="paragraphe of histoire.texte"
                :key="paragraphe"
            >
                <v-col cols="10">
                    <p>{{ paragraphe }}</p>
                </v-col>
            </v-row>
            </div>
    </v-container>
</template>

<style>
    h3 {
        font-size: 350%;
    }
    .first-row {
        margin-top: 4%;
        margin-left: 2%;
    }
    .rows {
        margin-left: 2%;
    }
    p {
        text-indent: 3%;
    }
</style>

<script>
    export default {
    props: ['raceList']
    }
</script>