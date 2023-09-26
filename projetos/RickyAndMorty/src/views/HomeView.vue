<script setup>
import { onMounted, reactive, ref } from 'vue';
import { RouterLink } from 'vue-router';

let character = reactive(ref());

onMounted(() => {
	fetch("https://rickandmortyapi.com/api/character").then(res => { res.json().then((x) => { character = x.results; console.log(character); }) })
})

</script>
<template>
  <div class="row">
    <div class="row col-35">
      <div v-for="c in character" class="col-6 d-flex justify-content-center">
        <div class="col-sm-20 col-md-8">
          <div class="card">
            <div class="card-body row">
              <div class=" "><strong>{{ c.name }}</strong></div>
              <img :src="c.image" >
                <div class="d-flex bd-highlight">
                  <div class="p-2 flex-fill bd-highlight"><strong>Espécie:</strong> {{ c.species }}</div>
                  <div class="p-2 flex-fill bd-highlight"><strong>Sexo:</strong> {{ c.gender }}</div>
                  <div class="p-2 flex-fill bd-highlight"><strong>Situação:</strong> {{ c.status }}</div>
                </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style>
body {
    margin: 0;
    padding: 0;
    background-color: #7aec7a; 
}
</style>