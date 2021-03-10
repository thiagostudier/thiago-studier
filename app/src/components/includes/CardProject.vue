

<template>
    <div class="card">
        <!-- <slot name="image"></slot> -->
        <div class="card__content">
            <span class="card-title"><slot name="title"></slot></span>
            <span class="card-desc"><slot name="desc"></slot></span>
            <span class="card-link"><slot name="link"></slot> <slot name="link-github"></slot></span>
            <span class="card-list"><slot name="list"></slot></span>
        </div>
    </div>
</template>

<script>
export default {
    name: 'CardProject',
}
</script>

<style scoped>

    :root {
        --color-text: #222022;
        --color-highlight-primary: #ffef7e;
        --color-highlight-secondary: #b7f9e9;
        --border-radius-primary: 32px;
    }

    .card {
        border-radius: var(--border-radius-primary);
        box-shadow: 24px 24px 80px rgba(0, 0, 0, 0.1);
        padding: 20px 20px 28px 20px;
        box-sizing: border-box;
        display: flex;
        flex-direction: column;
    }

    .card__image {
        width: 100%;
        max-height: 300px;
        border-radius: var(--border-radius-primary);
        object-fit: cover;
        margin-bottom: 18px;
    }

    img{width: 100%;}

    .card__date {
        display: block;
        font-family: var(--font-family-secondary);
        font-size: var(--font-size-caption);
        line-height: var(--line-height-caption);
        text-transform: uppercase;
        color: var(--color-text);
        margin-bottom: 6px;
    }

    .card__title {
        font-family: var(--font-family-primary);
        font-size: var(--font-size-title);
        line-height: var(--line-height-title);
        color: var(--color-text);
        box-decoration-break: clone;
        background-image: linear-gradient(
            90deg,
            var(--color-highlight-primary),
            var(--color-highlight-secondary)
        );
        background-size: 100% 42%;
        background-repeat: no-repeat;
        background-position: 0 85%;
        padding: 0 4px;
        margin-left: -4px;
    }

    .card-title{
        font-family: Roboto,sans-serif;
        font-size: 1rem;
        display: block;
        margin-top: 10px;
        margin-bottom: 10px;
        font-weight: 900;
    }
    
    .card-desc{
        font-family: Roboto,sans-serif;
        font-size: .8rem;
        display: block;
        margin-bottom: 10px;
    }

    .card-link{
        font-family: Roboto,sans-serif;
        font-size: .8rem;
        display: block;
        margin-bottom: 10px;
        font-weight: 500;
    }

    .card-list{
        font-family: Roboto,sans-serif;
        font-size: .8rem;
        display: block;
        font-weight: 500;
    }

    .card-link a{
        background: var(--background-dark);
        padding: 7px;
        display: inline-block;
        border-radius: 4px;
        color: var(--background-dark-light);
        transition: .2s all;
    }

    .card-link a:hover{
        background: var(--background-dark-light);
        color: var(--background-dark);
    }

</style>
