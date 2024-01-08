<template>
    <v-btn class="lighten-4 mr-2" @click="goTo(routeName)">
        <v-icon class="mr-1">{{ icon }}</v-icon>
        <div class="text-button">{{ label }}</div>
    </v-btn>
</template>

<script>
export default {
    props: {
        routeName: {
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
        goTo(routeName) {
            // Navigate to the specified route
            this.$router.push({ name: routeName });
        }
    }
}
</script>
