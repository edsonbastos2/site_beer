<template>
    <footer>
        <div class="social-link">
        <a class="socialLink" v-for="(social, index) in socialLinks" :href="social.link" :key="index" target="_blank">
                <img :src="social.icon" :alt="social.label" title="social.label">
            </a>
        </div>
    </footer>
</template>

<script>
import axios from '@/services/axios.js';

export default {
    data(){
        return{
            socialLinks: []
        }
    },
    mounted(){
        axios.get('/social-links.json').then( resp => {
            this.socialLinks = resp.data;
        })
    }
}
</script>

<style scoped>
    footer{
        width: 100%;
        height: 100px;
        background-color: var(--color-background-nav);
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .social-link{
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .socialLink{
        border: 2px solid var(--color-text-light);
        padding: 10px;
        border-radius: 50%;
        display: flex;
        justify-content: center;
        align-items: center;
        width: 40px;
        height: 40px;
        margin: 0 10px;
    }
    .socialLink img{
        width: 20px;
    }
</style>