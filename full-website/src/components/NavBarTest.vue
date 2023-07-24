<script lang="ts">
import { RouterLink } from 'vue-router'

export default {
    data: () => ({ value: 1 }),

    computed: {
        color() {
            switch (this.value) {
                case 0:
                    return 'blue-grey'
                case 1:
                    return 'teal'
                case 2:
                    return 'brown'
                case 3:
                    return 'indigo'
                default:
                    return 'blue-grey'
            }
        },
    },
}
</script>

<template>
    <v-layout class="overflow-visible" style="height: 10px">
        <v-bottom-navigation v-model="value" :bg-color="color" mode="shift">
            <v-btn value="home" block rounded="0" variant="tonal" @click=RouterLink to="/">
                Home
            </v-btn>

            <v-btn value="about" block rounded="0" variant="tonal" @click=RouterLink to="/about">
                About
            </v-btn>

            <v-btn>

            </v-btn>

            <v-btn>

            </v-btn>
        </v-bottom-navigation>
    </v-layout>
</template>
