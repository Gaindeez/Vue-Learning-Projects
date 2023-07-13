<script lang="ts">
import { defineComponent, PropType } from 'vue';

interface NavItem {
    label: string;
    path: string;
}

export default defineComponent({
    name: 'NavBar',
    props: {
        items: {
            type: Array as PropType<NavItem[]>,
            required: true,
        },
    },
});
</script>

<template>
    <nav>
        <ul>
            <li v-for="(item, index) in items" :key="index">
                <!--<router-link :to="item.path">{{ item.label }}</router-link>-->
                <router-link :to="item.path"> <button>{{ item.label }}</button> </router-link>
            </li>
        </ul>
    </nav>
</template>

<style scoped>
nav {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    z-index: 999;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 5rem; /* adjust the height as needed */
    background-color: #f78d04;
    color: #fff;
}

ul {
    display: flex;
    align-content: left;
    justify-content: flex-start;
    list-style: none;
}

li {
    font-family: "Lucida Console", Monaco, monospace;
    padding: 1rem;
}

</style>

