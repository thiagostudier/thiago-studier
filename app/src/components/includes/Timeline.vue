<template>
    <div class="timeline">
        <p class="timeline-title"><slot name="university"></slot></p>
        <p class="timeline-date"><slot name="date"></slot></p>
        <p><slot name="course"></slot></p>
    </div>
</template>

<script>
export default {
    name: 'Timeline',
}
</script>

<style scoped>

    .timeline{
        border-left: 2px solid #6d56c1;
        padding-left: 25px;
        padding-bottom: 50px;
        position: relative;
    }

    .timeline:before {
        width: 12px;
        height: 12px;
        border: 2px solid #6d56c1;
        position: absolute;
        content: "";
        border-radius: 50%;
        background-color: #fff;
        left: -9px;
    }

    .timeline .timeline-title{
        text-transform: uppercase;
        color: #6d56c1;
        font-size: 14px;
        line-height: 20px;
        font-family: Roboto Mono,monospace;
        font-weight: 700;
        padding-bottom: 5px;
        margin: 0;
    }

    .timeline .timeline-date{
        font-family: Inconsolata,monospace;
        font-size: 14px;
        line-height: 20px;
        color: #999;
        padding-bottom: 10px;
        margin: 0;
    }

    .timeline p{margin: 0px;}

</style>
