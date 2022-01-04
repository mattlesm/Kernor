<template>
    <v-container>
        <v-row :align="align" class="first-row"> 
            <v-col cols="3">
                <h3>{{ divinityList.name }}<span class="alignment">{{ divinityList.alignment }}</span></h3>
            </v-col>
            <v-spacer/>
            <v-col class="specs" cols="1">
                <h5><span class="element">ÉLÉMENT</span></h5>
                <h5><span class="symbole">SYMBOLE</span></h5>
            </v-col>
            <v-divider
                inset
                vertical
                class="divider"
            ></v-divider>
            <v-col class="specs-text" cols="4">
                <h5>{{ divinityList.element }}</h5>
                <h5>{{ divinityList.symbol }}</h5>
            </v-col>
        </v-row>

        <v-row class="rows">
            <v-col>
                <h4>{{ divinityList.surname }}</h4>
            </v-col>
        </v-row>

        <v-row>
            <v-col>
                <v-divider inset></v-divider>
            </v-col>
        </v-row>

         <v-row class="rows"
            v-for="text of divinityList.description"
            :key="text"
         >
             <v-col cols="10">
                <p>{{ text }}</p>
            </v-col>
        </v-row>
    </v-container>
</template>

<style>
    h3 {
        font-size: 350%;
    }
    .alignment {
        font-size: 30%;
        margin-left:5%;
    }
    h4 {
        margin-top: -2%;
        font-style: italic;
    }
    .specs {
        color: #FCA311;
        font-weight: bold;
        margin-top: 2%;
    }
    .specs-text {
        margin-top: 2%;
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
    props: ['divinityList']
    }
</script>