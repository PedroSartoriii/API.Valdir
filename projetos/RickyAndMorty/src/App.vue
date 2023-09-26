<script setup>
import {ref} from 'vue'
let num = ref(0)
</script>

  <template>
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark border-bottom border-body">
      <div class="container-fluid">
        <div class="p-2 flex-fill bd-highlight"></div>
        <router-link to="/" class="navbar-brand">Ricky and Morty</router-link>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls = "navbarNav" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
          <ul class="navbar-nav">
            <li class="nav-item">
            </li>
          </ul>
        </div>
      </div>
    </nav>
  <div class="main">
    <RouterView></RouterView>
  </div>
  <footer class="bg-dark text-light">
    <div> API | Desenvolvimento de Aplicações para a Internet |{{ new Date().getFullYear() }} </div>
  </footer>
  </template>


<style>
  footer{
    position:fixed;
    bottom:0;
    width:100%;
    display:flex;
    align-items:center;
    justify-content:center;
    height:30px;
  }
</style>

