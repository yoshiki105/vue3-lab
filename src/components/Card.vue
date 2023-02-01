<template>
  <div class="thumbnail">
    <img :src="item.image" alt="">
  </div>
  <div class="description">
    <h2>{{ item.name }}</h2>
    <p>{{ item.description }}</p>
    <span>¥<span class="price">{{ pricePrefix(item.price) }}</span></span>
  </div>
</template>

<script>
function pricePrefix(price) {
  return price.toLocaleString()
}
</script>

<style>
.item {
  padding: 10px;
  cursor: pointer;
}

.item:hover {
  transition: 0.2s transform ease-out;
  transform: scale(1.05);
}

.item>div.thumbnail>img {
  width: 100%;
  height: calc(100%);
  object-fit: cover;
}

.item>div.description {
  text-align: left;
  margin-top: 20px;
}

.item>div.description>p {
  margin-top: 0px;
  margin-bottom: 0px;
  font-size: 18px;
  line-height: 25px;
}

.item>div.description>span {
  display: block;
  margin-top: 10px;
  font-size: 20px;
}

.item>div.description>span>.price {
  font-size: 28px;
  font-weight: bold;
}
</style>
