<template>
  <div class="container">
    <h1>Chuck Norris Jokes</h1>
    <div class="row">
      <ChuckCard
        v-for="(item, index) in chuck"
        :key="index"
        :icon_url="item.icon_url"
        :value="item.value"
      />
    </div>
    <div class="footer">
      Chuck Norris no necesita copyright, el copyright lo necesita a él.
    </div>
  </div>
</template>

<script>
// Importa Bootstrap para que se pueda usar en el componente
import 'bootstrap/dist/css/bootstrap.min.css';
import ChuckCard from './components/ChuckCard.vue'

export default {
  name: 'App',
  components: {
    ChuckCard
  },
  data() {
    return {
      chuck: [
        {
          icon_url: "https://pngimg.com/d/chuck_norris_PNG18.png",
          value: "Chuck Norris puede saltar en paracaídas al espacio exterior."
        },
        {
          icon_url: "https://pngimg.com/d/chuck_norris_PNG18.png",
          value: "El principal producto de Chuck Norris es el dolor."
        },
        {
          icon_url: "https://pngimg.com/d/chuck_norris_PNG18.png",
          value: "Chuck Norris no lee libros. Los mira fijamente hasta que obtiene la información que quiere."
        },
        {
          icon_url: "https://pngimg.com/d/chuck_norris_PNG18.png",
          value: "El tiempo no espera a nadie. A menos que ese hombre sea Chuck Norris."
        },
        {
          icon_url: "https://pngimg.com/d/chuck_norris_PNG18.png",
          value: "Si escribes Chuck Norris en Scrabble, ganas. Para siempre."
        }
      ]
    };
  }
}
</script>

<style>
body {
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  background-color: #f8f5ff;
  margin: 0;
  padding: 20px;
}

.container {
  max-width: 800px;
  width: 100%;
  margin: 0 auto;
}

h1 {
  color: #4a148c;
  text-align: center;
  margin-bottom: 30px;
  font-size: 2.5rem;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.1);
}

.footer {
  margin-top: 30px;
  text-align: center;
  color: #673ab7;
  font-size: 0.9rem;
}
</style>

