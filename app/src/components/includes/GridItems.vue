<template>
    <div class="grid-items" :style="`grid-template-columns: repeat(`+columns+`, 1fr);`">
        <slot></slot>
    </div>
</template>

<script>
export default {
    name: 'GridItems',
    props: ['columns'],
}
</script>

<style scoped>
    .grid-items{
        display: grid;
        grid-column-gap: 0px;
        grid-row-gap: 0px;
        gap: 10px;
    }   
    
    @media(max-width: 1080px){
        .grid-items{
            grid-template-columns: repeat(1, 1fr) !important;
        }
    }

</style>
