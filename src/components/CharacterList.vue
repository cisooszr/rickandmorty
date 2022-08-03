<template>
  <div><h3>Karakter Listesi</h3></div>
</template>
<script>
export default {
  name: "CharacterList",

  setup() {
    async function rickAndMorty() {
      console.log("ben fonksiyon yazmayı öğreniyorum");
      const fetchAPI = await fetch("https://rickandmortyapi.com/api/character");
      const jsonData = await fetchAPI.json();
      console.log(jsonData?.results);
    }

    rickAndMorty();
  },
};
</script>
