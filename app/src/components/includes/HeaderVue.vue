<template>
    <div class="header">   
        <div class="container">
            <div class="box-header">
                <div class="box-header-image">
                    <slot name="image" />
                </div>
                <div class="box-header-presentation">
                    <slot name="principal"/>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'HeaderVue',
}
</script>

<style scoped>

    .header .container{
        width: 1080px;
        max-width: 100%;
        margin: 0px auto;
        padding: 0px 15px;
        display: inherit;
    }

    .header{
        background: var(--background-dark);
        height: auto;
        padding: 40px 0px;
        display: flex;
        justify-content: center;
        margin-bottom: 40px;
    }

    .header .box-header{
        width: 100%;
        display: flex;
        gap: 40px;
        margin-bottom: -70px;
    }
    
    .header .box-header .box-header-image{
        width: 250px;
        height: 250px;
        position: relative;
        border: 5px solid #1f1f1f;
        border-radius: 5px;
        background: #4e4e4e;
        overflow: hidden;
    }

    .header .box-header .box-header-image img{
        position: absolute;
        left: 50%;
        top: 50%;
        transform: translate(-50%, -50%);
        min-width: 102%;
        border-radius: unset !important;
        width: auto;
        margin: 0px auto;
        height: 100% !important;
    }

    .header .box-header .box-header-presentation{
        color: var(--color-white);
    }

    .header .box-header .box-header-presentation h2{
        margin-top: 0px;
        margin-bottom: 20px;
        width: 100%;
        font-size: 44px;
        line-height: 35px;
        font-weight: 700;
        font-family: Roboto Mono,monospace;
    }

    .header .box-header .box-header-presentation h3{
        font-size: 16px;
        line-height: 24px;
        margin-top: 10px;
        margin-bottom: 10px;
        display: block;
        font-family: Roboto Mono,monospace;
        font-weight: 400;
    }

    .header .box-header .box-header-presentation span a{
        transition: 0.2s all;
    }

    .header .box-header .box-header-presentation span a:hover{
        color: var(--color-white) !important;
    }

    .header a.link-icon {
        font-size: 20px !important;
        margin-right: 10px;
    }

    @media(max-width: 1080px){
        .header{
            margin-bottom: 0px;   
        }
        .header .box-header{
            width: 100%;
            display: block;
            overflow-x: hidden;
            padding: 20px 0px;
        }
        .header .box-header{
            width: 100%;
            display: block;
            overflow-x: hidden;
            margin-bottom: 0px;
        }
        .header .box-header .box-header-image{
            margin: 0px auto;
            margin-bottom: 20px;
        }
        .header .box-header .box-header-presentation h2{
            font-size: 30px;
            text-align: center;
        }
        .header .box-header .box-header-presentation h3{
            text-align: center;
            display: block;
            margin-bottom: 20px;
        }
        .header .box-header .box-header-presentation .links{
            text-align: center;
            display: block;
            margin-top: 30px;
        }
    }

</style>
