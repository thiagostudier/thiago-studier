<template>
    <div class="grid-items" :style="`grid-template-columns: repeat(`+grid+`, 1fr);`">
        <slot></slot>
    </div>
</template>

<script>
export default {
    name: 'GridItems',
    props: ['columns', 'columns_tablet', 'columns_mobile'],
    data(){
        return{
            grid: this.columns,
        }
    },
    methods: {
        onResize() {
            if (window.innerWidth >= 1080) {
                this.grid = this.columns
            } else if (window.innerWidth >= 750 && window.innerWidth < 1080){
                this.grid = this.columns_tablet
            } else {
                this.grid = this.columns_mobile
            }
        }
    },
    created() {
        this.onResize();
        window.addEventListener('resize', this.onResize)
    },
}
</script>

<style scoped>
    .grid-items{
        display: grid;
        grid-column-gap: 0px;
        grid-row-gap: 0px;
        gap: 10px;
    }
    /* @media(max-width: 1080px){
        .grid-items{
            grid-template-columns: repeat(1, 1fr) !important;
        }
    } */
</style>
