<template>
    <div>UserRepositories</div>
</template>

<script>
    import { onMounted } from 'vue';
    export default {
        setup() {
            onMounted(() => {
                console.log('onMounted')
            }) 
        },
    }
</script>