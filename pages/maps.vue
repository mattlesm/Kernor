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
                                        <h6>
                                            <v-btn
                                                plain
                                                @click="overlay = !overlay"
                                            >
                                                {{ item.title }}
                                            </v-btn>
                                        </h6>
                                    </v-overlay>
                                </v-fade-transition>
                            </v-img>
                    </template>
                </v-hover>
            </v-col>
        </v-row>
        </div>
    </v-main>
</template>

<style>
    .wrapper {
        margin:2%;
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
            ]
        }
    }
  };
</script>