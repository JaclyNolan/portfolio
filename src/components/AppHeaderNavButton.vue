<template>
    <v-btn :prepend-icon="icon" variant="text" class="lighten-4 mr-2" @click="goTo(routeName)">
        {{ label }}
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
