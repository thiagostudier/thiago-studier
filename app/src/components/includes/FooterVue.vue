<template>
    <footer>
        <div class="container">
            <span><slot /></span>
        </div>
    </footer>
</template>

<script>
export default {
    name: 'FooterVue',
}
</script>

<style scoped>

    footer{
        padding: 40px 20px !important;
        background: var(--background-dark);
    }

    footer span{
        font-family: Roboto,sans-serif;
        font-size: .8rem;
        text-align: right;
        display: block;
    }

</style>
