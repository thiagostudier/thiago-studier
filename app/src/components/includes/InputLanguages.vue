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

    #input-languages{
        background: #fff;
        border-radius: 3px;
        width: 100px;
        position: fixed;
        top: 0px;
        right: 0px;
        margin: 5px;
        display: flex;
        align-items: center;
        padding: 5px;
        justify-content: space-between;
        -webkit-box-shadow: 24px 24px 80px rgb(0 0 0 / 10%);
        box-shadow: 24px 24px 80px rgb(0 0 0 / 10%);
        z-index: 1000;
    }

    #input-languages label{
        font-weight: bold;
    }
    
</style>
