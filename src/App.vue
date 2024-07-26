<template>
  <div>
    <h1>{{ titulo }}</h1>
    <ul>
      <li v-for="foto of fotos">
        <img :src="foto.url" :alt="foto.titulo">
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      titulo: "Album Online",
      fotos: [
        {
          url: "https://encrypted-tbn3.gstatic.com/images?q=tbn:ANd9GcQgByBT5IiAT_a2x9pUVb4VMoOrlzHH7Jrzj-HB5jzHlR4lNLMS",
          titulo: "Cachorro",
        },
        {
          url: "https://i.pinimg.com/736x/09/62/51/096251ef479bb17e7d2f98d75bb8e77e.jpg",
          titulo: "Rottweiler",
        },
        {
          url: "https://www.petshopdopatinho.com.br/wp-content/uploads/2020/01/Fases-da-vida-de-um-cachorro.jpg",
          titulo: "Cachorro",
        },
      ],
    };
  },
};
</script>

<style></style>
