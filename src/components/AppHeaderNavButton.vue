<template>
    <v-btn class="lighten-4 mr-2" @click="goTo(route)">
        <v-icon class="mr-1">{{ icon }}</v-icon>
        <div class="text-button">{{ label }}</div>
    </v-btn>
</template>

<script>
export default {
    props: {
        route: {
            type: String,
            require: false,
        },
        icon: {
            type: String,
            require: true, 
        },
        label: {
            type: String,
            require: true,
        },
    },
    methods: {
        goTo(route) {
            this.$router.push(route);
        }
    }
}
</script>
