<template>
    <nav>
        <div class="container">
            <h1 class="logo">
                Vue Countries Cities
            </h1>
            <a class="documentation" href="#" target="_blank">
                <icon name="book" size="20" />
                Documentation
            </a>
        </div>
    </nav>
</template>

<script>
export default {
    name: 'Nav'
}
</script>

<style lang="scss" scoped>
nav{
    height: 120px;
    border-bottom: 1px solid rgba(black, .1);
    .container{
        height: 100%;
        display: flex;
        align-items: center;
        justify-content: space-between;
        .logo{
            font-size: 35px;
        }
        .documentation{
            display: flex;
            align-items: center;
            font-size: 18px;
            .book{
                margin-top: -6px;
                margin-right: 3px;
            }
        }
    }
}
@media (max-width: 1400px){
    .documentation{
        margin-right: 60px;
    }
}
@media (max-width: 680px){
    nav .container{
        flex-direction: column;
        justify-content: center;
        .logo{
            font-size: 30px;
        }
        .documentation{
            margin-right: 0;
            font-size: 17px;
            svg{
                width: 16px;
                height: 16px;
            }
        }
    }
}
</style>