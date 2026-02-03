
<template>
  <p>Reaction Time: {{ score }} ms</p>
  <p class="rank"> {{ rank }} </p>
</template>

<script>
export default {
    props : ['score'],
    data () {
        return {
            rank: null
        }
    },
    mounted() {
        if(this.score < 250) {
            this.rank = "Super fast"
        }
        else if (this.rank < 400) {
            this.rank = "Rapid reflexes"
        }
        else {
            this.rank = "Snail pace.."
        }
    }
}
</script>

<style>

</style>