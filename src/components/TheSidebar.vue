<template>
  <div class="sidebar" v-if="sidebar">
    <span class="sidebar-close" @click="close">&times;</span>

    <div class="sidebar-content">
      <p>
        Добро пожаловать в систему мониторинга выплат.<br />
        Она создана для того, чтобы не пропустить день выплат
        ЗП/авансов/отпускных.
      </p>
    </div>
  </div>
</template>

<script>
import { computed } from "vue";
import { useStore } from "vuex";

export default {
  setup() {
    const store = useStore();

    const sidebar = computed(() => store.state.sidebar);

    return {
      sidebar,
      close: () => store.commit("closeSidebar"),
    };
  },
};
</script>

<style scoped>
</style>