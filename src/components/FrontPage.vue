<script setup>
const props = defineProps({
  infos: Object,
})
</script>

<template>
  <div class="container" :style="{ backgroundImage: `url(${infos.image})` }">
    <div>
      <div class="verticalLine"></div>
      <div>
        <h3>
          <span>{{ infos.category.toUpperCase() }}</span
          ><span>{{ infos.subCategory.toUpperCase() }}</span>
        </h3>

        <h1>
          <span>{{ infos.title }}</span>
        </h1>
      </div>
    </div>

    <p>{{ infos.teaser }}</p>
  </div>
</template>

<style scoped>
.container {
  height: 550px;
  border: 1px solid black;
  background-repeat: no-repeat;
  background-position: bottom;
  padding: 90px;
}
.container > div {
  position: relative;
}
.container > div::before {
  content: '';
  position: absolute;
  top: 0px;
  width: 5px;
  height: 100%;
  left: -5px;
  background: linear-gradient(var(--light-purple), var(--dark-purple));
}
h1 {
  font-size: 32px;
  line-height: 46px;
  color: white;
  width: 750px;
  font-family: var(--font-title);
  font-weight: bold;
}
h3 {
  font-size: 12px;
  line-height: 24px;
  color: white;
  background-color: black;
  padding: 5px 0;
  display: inline;
}
h3 span:first-child {
  letter-spacing: 0.7px;
  background: linear-gradient(45deg, var(--light-purple), var(--dark-purple));
  background-clip: text;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}
h3 span:last-child {
  padding: 0 10px;
  font-weight: 300;
  letter-spacing: 0.3px;
}
span {
  padding: 5px;
  background-color: black;
  white-space: pre-wrap;
}
.container > p {
  margin-top: 40px;
  padding: 25px;
  background-color: rgba(0, 0, 0, 0.487);
  color: white;
  font-weight: 300;
  line-height: 22px;
  letter-spacing: 0.7px;
  font-size: 14px;
  width: 800px;
}
</style>
