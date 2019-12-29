<template>
    <div class="form-check">
        <input type="checkbox" v-on:click="hitung" class="form-check-input" value="" v-bind:id="tugasSaya.id" />
        <label v-bind:for="tugasSaya.id" onclick="" class="form-check-label item" v-bind:class="{'item-completed':tugasSaya.isDone}"> {{tugasSaya.namaTugas}} </label>
    </div>
</template>

<script>
export default {
    name: 'ItemTugas',
    props: ['tugasSaya'],
    methods: {
      hitung: function(){
        if(this.tugasSaya.isDone == true){
          return this.tugasSaya.isDone = false;
        }else{
          return this.tugasSaya.isDone = true;
        }
      }
    }
}
</script>

<style scoped>

</style>
