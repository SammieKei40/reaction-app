<template>
  <p>Reaction Time: {{score}}ms</p> 
  <p class="rank"> {{rank}} &#128540; </p>
</template>

<script>
export default {
props: ['score'],
data() {
    return {
        rank: null
    }
},
mounted(){
        if(this.score < 250){
            this.rank = "Awesome Reflexes!!!"  
        } else if(this.score < 400){
            this.rank = "Rapid Reflexes!!!"
        } else {
            this.rank = "Snail Pace..." 
        }
    }
}
</script>

<style>
    .rank{
        font-size: 1.4em;
        color: #000;
        font-weight: bold;
    }
</style>