<template>
    <section>
        <div class="container">
            <slot />
        </div>
    </section>
</template>

<script>
export default {
    name: 'SectionContent',
}
</script>

<style scoped>

    section{
        padding: 40px 20px !important;
        max-width: 1080px;
        margin: 0px auto;
    }

    section h2{
        color: var(--text);
    }

</style>
