<template>
  <TheNavigationNew />
  <div class="container">
    <router-view v-slot="{ Component }">
      <transition name="slide" mode="out-in">
        <component :is="Component" :key="$route.path"> </component>
      </transition>
    </router-view>
  </div>
</template>

<script>
import TheNavigationNew from "@/components/TheNavigationNew.vue";

export default {
  components: { TheNavigationNew },
};
</script>

<style lang="css">
.slide-enter-active,
.slide-leave-active {
  transition: opacity 0.5s, transform 0.5s;
}
.slide-enter-from,
.slide-leave-to {
  opacity: 0;
  transform: translateX(-30%);
}
</style>
