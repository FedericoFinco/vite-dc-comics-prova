<script>
export default {
    name: "appHeader",
    props:[
        "list"
    ]
}
</script>

<template>
    <img src="../assets/favicon.ico" alt="">
    <template v-for="link in list">
        <p>{{ link }}</p>
    </template>
</template>