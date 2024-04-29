<script setup>
// props - onMounted, reactive, ref
import { onMounted, reactive, ref } from 'vue';
import ListPersonagens from '../components/ListPersonagens.vue';

let personagens = reactive(ref())

// fetch - axios
// onde eu puxo a api
onMounted(() => {
  fetch("https://rickandmortyapi.com/api/character")
  .then(response => response.json())
  .then(response => {
    personagens.value = response.results
    console.log(personagens)
  })
})
</script>


<template>
<body>
  <section>
  <main>
    <div class="container">
      <div class="row mt-4">
        <div class="col-sm-12 col-md-6">
          <div class="carde" style="width: 70rem" text-align: center>
            <img src="https://imagensemoldes.com.br/wp-content/uploads/2021/04/Logo-Rick-and-Morty-PNG.png" class="card-img-top" alt="..." style="border-radius: 10px; text-align: center; width: 100%; object-fit: cover;">
            <h1 class="card-text">///////////////</h1>
          </div>
        </div>

        <section>        
        <div class="col-sm-12 col-md-6">
          <div class="cardi">
            <div class="card-body row">
              <!-- AQUI -->
              <ListPersonagens 
            v-for="personagem in personagens"
            :key="personagem.name"
            :name="personagem.name"
            :url="personagem.url"
            :image="personagem.image"
            :status="personagem.status"
            :species="personagem.species"
            :gender="personagem.gender"
            :location="personagem.location"
            :episode="personagem.episode"
            />
            <!-- AQUI É O FOR LISTANDO AS API -->
            </div>
          </div>
        </div>
      </section>
      </div>
    </div>
  </main>
</section>
</body>
</template>

