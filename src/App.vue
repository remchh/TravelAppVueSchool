<template>
  <TheNavigationNew />
  <div class="container">
    <router-view></router-view>
  </div>
</template>

<script>
import TheNavigationNew from "@/components/TheNavigationNew.vue";

export default {
  components: { TheNavigationNew },
};
</script>
