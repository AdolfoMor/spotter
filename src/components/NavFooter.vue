<template>
  <footer>
    <nav>
      <a v-for="item in navItems" :key="item">{{ item }}</a>
    </nav>
  </footer>
</template>

<script>
export default {
  data() {
    return {
      navItems: [
        "Spotter",
        "Product",
        "Use Cases",
        "Developers",
        "Resources",
        "Demo",
        "Pricing"
      ]
    };
  }
};
</script>

<style scoped>
footer {
  margin-top: 50px;
  text-align: center;
}

nav {
  display: flex;
  justify-content: center;
  gap: 20px;
  flex-wrap: wrap;
}

nav a {
  text-decoration: none;
  color: #333;
  font-weight: bold;
}
</style>