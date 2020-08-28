<template>
    <div id="grid-images">
        
    </div>
    
</template>

<script>
import axios from 'axios';

export default {
    name: 'GridImages',
    data: function() {
        return {
            avatarImg: 'https://avatars0.githubusercontent.com/u/3336816?s=460&u=a3def04c56afd7220d835005dbf1879a0b497554&v=4',
            usernames: ['Messi', 'Falcao12', 'Neymar', 'Sean Garnier', 'Muhammad'],
            apis: null,
            fakeApi: null,
        }
    },
    mounted: function() {
        axios
        .get('https://dog.ceo/api/breed/pomeranian/images/random/10')
        .then(response => this.apis = response.data.message)

        axios
        .get('https://api.mocki.io/v1/9caa0ba8')
        .then(response => this.fakeApi = response)
    }
}
</script>

<style>
    #grid-images {
        display: flex;
        flex-flow: row wrap;
        justify-content: space-around;
    }

</style>