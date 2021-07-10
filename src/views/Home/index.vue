<template>
    <main class="bg-gif">
        <div class="container mainContent">
            <img class="bg-logo" src="@/assets/img-fluid.png" alt="">
        </div>
    </main>
</template>

<script>
export default {

}
</script>

<style scoped>
    .bg-gif{
        background-color: var(--color-background-home);
        background: url(../../assets/bg-video.gif) no-repeat center center;
        background-size: cover;
        min-height: 100%;
        justify-content: center;
        align-items: center;
    }
    
    .mainContent{
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }

</style>