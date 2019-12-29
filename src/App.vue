<template>
  <div id="app">
    <!-- <Logos /> -->
    <div class="container">
      <div class="row header mb-5 p-3">
        <div class="col-md-12">
          <h2>What I do Today?</h2>
        </div>
      </div>
      <div class="row content">
        <div class="col-md-12">
          <div class="pekerjaan-rumah">
            <div class="row">
              <div v-for="tugasSaya in tugas" v-bind:key="tugasSaya.id" class="mb-3 tugas col-md-12 text-left">
                <ItemTugas v-bind:tugasSaya="tugasSaya"/>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import ItemTugas from './components/ItemTugas.vue'
// import Logos from './components/Logos.vue'
import 'bootstrap/dist/css/bootstrap.css'

export default {
  name: 'app',
  data: function() {
    return {
      tugas: [
        {
          id: 1,
          namaTugas: 'Membersihkan Toilet',
          isDone: false,
        },
        {
          id: 2,
          namaTugas: 'Menyampu Halaman Rumah',
          isDone: false,
        },
        {
          id: 3,
          namaTugas: 'Jogging',
          isDone: false,
        },
        {
          id: 4,
          namaTugas: 'Istirahat',
          isDone: false,
        }
      ]
    }
  },
  components: {
    // HelloWorld,
    // Logos,
    ItemTugas,
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.header{
  background: #1abc9c;
}

.header h2{
  margin: 0;
}

.item-completed{
  color: #1abc9c;
}
</style>
