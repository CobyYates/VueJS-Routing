<template>
<div>
    <h3>Edit the User</h3>
    <p>Locale: {{ $route.query.Locale }}</p>
    <p>Analytics: {{ $route.query.q }}</p>
    <hr>
    <button class="btn btn-warning" @click="confirmed = true">Confirm</button>
    <div style="height: 700px"></div>
    <p id="data">Some Data</p>
</div>    
</template>

<script>
export default {
    data() {
        confirmed: false
    },
    beforeRouteLeave(to, from, next) {
        if (this.confirmed) {
            next()
        }else {
            if (confirm('Are you sure?')) {
                next()
            }else {
                next(false)
            }
        }
    }
}
</script>