<script setup>
const router = useRouter();

const mainRoutes = computed(() => {
  return router.options.routes.filter(
    (route) => route.path.split("/").length <= 2
  );
});

function capitalize(word) {
  return word.charAt(0).toUpperCase() + word.slice(1);
};
</script>

<template>
  <section></section>
  <nav>
    <ul>
      <li v-for="route in mainRoutes" :key="route.id">
        <NuxtLink :to="route.path">{{ route.name }}</NuxtLink>
      </li>
    </ul>

  </nav>

</template>

<style>
  ul{
    display: flex;
    gap: 4em;
    justify-content: center;
    background: cornflowerblue;
    height: 5rem;
    
  }
  li{
    display: flex;
    justify-content: center;
    align-content: center;
    border: 1px black solid;
    background: lightgray;
    height: 30px;
    width: 80px;
    border-radius: 10px;
    margin: 1.5rem;
  }

  li:hover{
    background: black;
  }

  a:hover{
    color: white;
  }

  a{
    text-decoration: none;
    color: black;
  }
</style>