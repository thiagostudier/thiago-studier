<template>
    <div id="input-languages">
        <label for="pt">PT</label>
        <input type="radio" id="pt" value="pt" v-model="language" v-on:change="changeLanguage('pt')" />
        <input type="radio" id="en" value="en" v-model="language" v-on:change="changeLanguage('en')" />
        <label for="en">EN</label>
    </div>
</template>

<script>
export default {
    name: 'InputLanguages',
    props: {
        language: String,
        changeLanguage: Function,
    },
}
</script>

<style scoped>
    
</style>
