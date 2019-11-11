<template>
    <section>
        <div v-if="$route.query.message" class="alert alert-danger mb-3 mt-3">
            Need login first
        </div>
        <form @submit.prevent="onSubmit">
            <div class="form-group">
                <input type="text" class="form-control">
            </div>
            <p>
                <nuxt-link to="/">Home</nuxt-link>
            </p>
            <button class="btn btn-success" type="submit">Sign In</button>
        </form>
    </section>
</template>

<script>
export default {
    layout: 'empty',
    methods: {
        onSubmit(){
            this.$store.dispatch('login');
            this.$router.push('/');
        }
    }
}
</script>

