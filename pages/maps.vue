<template>
    <v-main>
        <div class="wrapper">
        <v-row>
            <v-col
            v-for="item of items"
            :key="item.id"
            cols="3"
            >
                <v-hover>
                    <template v-slot:default="{ hover }">
                        <v-img
                            :src="item.path"
                            aspect-ratio="1" 
                        >   
                            <v-fade-transition>
                                <v-overlay
                                    v-if="hover"
                                    absolute
                                    dark
                                >
                                    <v-btn
                                        dark
                                        plain
                                        x-large
                                        class="overlay_button"
                                        @click="overlay = !overlay"
                                    >
                                        {{ item.title }}
                                    </v-btn>
                                </v-overlay>
                            </v-fade-transition>
                        </v-img>
                    </template>
                </v-hover>
            </v-col>
        </v-row>
        </div>
        <v-overlay
            :value="overlay"
            class="overlay_wrapper"
        >
            <v-img :src="path" max-height="800px" contain>
                <v-btn
                    fab
                    dark
                    color="black"
                    top
                    small
                    @click="overlay = false"
                >
                    <v-icon>mdi-close</v-icon>
                </v-btn>
            </v-img>
        </v-overlay>
    </v-main>
</template>

<style>
    .wrapper {
        margin:2%;
        height:100%;
    }
    .overlay_wrapper {
        margin-left: 10%;
    }
    .overlay_button {
        margin-top: 15%;
    }
</style >

<script>
  export default {
    name: 'Maps',
    data() {
        return {
            items: [
                { id: 1, title: "Kernor", path: require('@/assets/Kernor.jpg')},
                { id: 2, title: "Roc d'Or", path: require('@/assets/Roc_dOr.jpg')},
                { id: 3, title: "Roc d'Or", path: require('@/assets/Roc_dOr.jpg')},
                { id: 4, title: "Roc d'Or", path: require('@/assets/Roc_dOr.jpg')},
                { id: 5, title: "Roc d'Or", path: require('@/assets/Roc_dOr.jpg')},
                { id: 6, title: "Roc d'Or", path: require('@/assets/Roc_dOr.jpg')},
                { id: 7, title: "Roc d'Or", path: require('@/assets/Roc_dOr.jpg')},
                { id: 8, title: "Roc d'Or", path: require('@/assets/Roc_dOr.jpg')},
                { id: 9, title: "Roc d'Or", path: require('@/assets/Roc_dOr.jpg')},
                { id: 10, title: "Roc d'Or", path: require('@/assets/Roc_dOr.jpg')},
                { id: 11, title: "Roc d'Or", path: require('@/assets/Roc_dOr.jpg')}
            ],
            overlay: false,
            path: require('@/assets/Kernor.jpg')
        }
    }
  };
</script>