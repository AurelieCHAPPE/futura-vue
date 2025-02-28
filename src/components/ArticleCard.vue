<script setup>
const props = defineProps({
  article: Object,
})
</script>

<template>
  <div class="articleCard">
    <img :src="article.image" :alt="article.title" />

    <p>
      <span>{{ article.category.toUpperCase() }}</span
      ><span>{{ article.subCategory.toUpperCase() }}</span>
    </p>

    <h2>{{ article.title }}</h2>

    <p class="date">{{ article.date }}</p>
  </div>
</template>

<style scoped>
.articleCard {
  width: calc((100% - 90px) / 4);
  height: 480px;
}
img {
  width: 100%;
  height: 350px;
  object-fit: cover;
  margin-bottom: 15px;
}
span {
  font-size: 12px;
}
span:first-child {
  margin-right: 10px;
  font-weight: bold;
  letter-spacing: 0.7px;
  background: linear-gradient(45deg, var(--light-purple), var(--dark-purple));
  background-clip: text;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}
span:last-child {
  font-weight: 300;
  letter-spacing: 0.3px;
}
h2 {
  margin: 10px 0;
  font-family: var(--font-title);
  font-size: 14px;
  font-weight: bold;
  line-height: 20px;
}
.date {
  letter-spacing: 0.3px;
  font-weight: 300;
  font-size: 12px;
  color: var(--grey);
}
</style>
