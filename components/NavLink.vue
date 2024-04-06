<template>
  <NuxtLink :to="to" class="nav-link" :class="{ active: isActive }">
    <img :src="iconSrc" alt="icon" />
    {{ label }}
  </NuxtLink>
</template>

<script>
export default {
  props: {
    to: {
      type: [String, Object],
      required: true,
    },
    label: {
      type: String,
      required: true,
    },
    iconSrc: {
      type: String,
      required: true,
    },
  },
  data() {
    return {
      isActive: false,
    }
  },
  mounted() {
    // Memeriksa jika path saat ini sama dengan path to
    this.isActive = this.$router.currentRoute.path === this.to
  },
}
</script>
