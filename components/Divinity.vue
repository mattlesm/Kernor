<template>
    <v-container>
        <v-row :align="align"> 
            <v-col cols="3  ">
                <h3>{{ divinityList.name }}<span class="alignment">{{ divinityList.alignment }}</span></h3>
            </v-col>
        </v-row>

        <v-row>
            <v-col>
                <h4>{{ divinityList.surname }}</h4>
            </v-col>
        </v-row>

         <v-row>
             <v-col cols="6">
                <h5><span class="element">ÉLÉMENT</span>{{ divinityList.element }}</h5>
            </v-col>
         </v-row>
         <v-row>
            <v-col cols="6">
                <h5><span class="symbole">SYMBOLE</span>{{ divinityList.symbol }}</h5>
            </v-col>
        </v-row>

        <v-row>
            <v-col>
                <v-divider inset></v-divider>
            </v-col>
        </v-row>

         <v-row>
             <v-col cols="10">
                <p>{{ divinityList.description }}</p>
            </v-col>
        </v-row>
    </v-container>
</template>

<style>
    h3 {
        font-size: 350%;
        margin-top: 10%;
        margin-left: 10%;
    }
    .alignment {
        font-size: 30%;
        margin-left:5%;
    }
    h4 {
        margin-left: 3%;
        margin-top: -2%;
        font-style: italic;
    }
    h5 {
        margin-left: 12%;
    }
    .element {
        color: #FCA311;
        margin-right:8%;
    }
    .symbole {
        color: #FCA311;
        margin-right:8%;
    }
    p {
        margin-left:3%;
    }
</style>

<script>
    export default {
    props: ['divinityList']
    }
</script>