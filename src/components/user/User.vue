<template>
<div>
    <h1>The User Page</h1>
    <hr>
    <!-- <p>Loaded ID: {{ id }}</p> -->
    <button @click="navigateToHome" class="btn btn-primary">Go to Home</button>
    <hr>
    <router-view></router-view>
    
</div>
</template>

<script>
export default {
    /*data() {
        return {
            id: this.$route.params.id
        }
    },
    watch: {
        '$route'(to, from) {
            this.id = to.params.id //this makes the id in the url dynamic for when you change within the same component
        }
    },*/
    methods: {
        navigateToHome() {
            this.$router.push('/')
            // or
            // this.$router.push({path: '/'})
        }
    }
}
</script>