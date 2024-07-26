<template>
  <main>
    <!-- A interpolação é usada para exibir dados dinamicos no HTML {{  }} -->
    <h1>{{ titulo }}</h1>
    <ul>
      <!-- a diretiva v-for é usada para renderizar uma lista de itens com base um uma array ou objeto. -->
      <li v-for="foto of fotos">
        <img :src="foto.url" :alt="foto.titulo" />
        <!-- dentro de um atributo não podemos usar a interpolação -->
        <!--  o data binding é o processo de ligar dados entre lógica do aplicativo e o template -->
        <!--No Vue existem as diretivas que são descritas com o `v-`  -->
        <!-- Diretiva é um atributo especial que adiciona funcionalidade aos elementos do DOM. -->
        <!-- uma diretiva faz Manipulação de atributos, classes, estilos, eventos e controle de renderização condicional. -->
        <!-- A diretiva v-bind faz uma interpolação dentro de um atributo. -->
        <!--  <img v-bind:src="foto.url" v-bind:alt="foto.titulo"> -->
        <!-- mas a uma forma mais simples de usar a diretiva v-bind que é usar o : antes do atributo, como no exemplo usado na tag acima. -->
      </li>
    </ul>
  </main>
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
