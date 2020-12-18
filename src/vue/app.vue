<template>
  <div>
    <picture>
      <source srcset="/src/images/xxx-sp.webp 768w, /src/images/xxx.webp" type="image/webp" />
      <img srcset="/src/images/xxx-sp.png 768w, /src/images/xxx.png" alt="" width="600" height="200" loading="lazy" />
    </picture>
    <ul>
      <li @click="toggleActive1()" v-bind:class="{ active: isActive1 }">ボタン1</li>
      <li @click="toggleActive2()" v-bind:class="{ active: isActive2 }">ボタン2</li>
    </ul>
    <div v-if="isActive1">ボタン1がクリックされました</div>
    <div v-if="isActive2">ボタン2がクリックされました</div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isActive1: true,
      isActive2: false,
    }
  },
  methods: {
    toggleActive1() {
      this.isActive1 = true
      this.isActive2 = false
    },
    toggleActive2() {
      this.isActive1 = false
      this.isActive2 = true
    },
  },
}
</script>
