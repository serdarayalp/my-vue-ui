<template>
    <a :href="url"><slot></slot></a>
</template>

<script>
export default {
    name: "NavigationLink",
    props: ['url']
}
</script>

<style scoped>

</style>
