<template>
<div>
    <h3>Some User Details</h3>
    <p>User Loaded has ID: {{ $route.params.id }}</p>
    <!-- <router-link 
        tag="button"
        class="btn btn-primary" 
        :to="'/user/' + $route.params.id + '/edit'">Edit User</router-link> -->

        <router-link
        tag="button"
        class="btn btn-primary"
        :to="link">Edit User</router-link>
</div>
</template>

<script>
export default {
    data() {
        return {
            link: { 
                name: 'userEdit', 
                params: { id: this.$route.params.id }, 
                query: { locale: 'en', q: 100 },
                hash: '#data'
            }
        }
    },
    // 
    beforeRouteEnter(to, from, next) {
        //if user is logged in then navigate
        if (true) {
            next()
        }else {
        next(false)
        }
    }
}
</script>