<template>
    <div class="skill-item">
        <slot></slot>
    </div>
</template>

<script>
export default {
    name: 'SkillItem',
}
</script>

<style scoped>

    .skill-item{
        display: inline-grid;
        flex-direction: column;
        margin-bottom: 20px;
    }

    img{
        margin: 0px auto;
        max-width: 100%;
        max-height: 100px;
        margin-bottom: 10px;
    }

    span{
        width: 100%;
        text-align: center;
        color: var(--text);
        font-family: Roboto,sans-serif;
        font-size: 0.8rem;
    }

</style>
