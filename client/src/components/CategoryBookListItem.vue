<template>
  <li class="book-box">
    <div class="book-image">
      <img
        :src="require('@/assets/images/books/' + book.imageFile)"
        :alt="book.title"
      />
    </div>
    <div class="book-title">{{ book.title }}</div>
    <div class="book-author">{{ book.author }}</div>
    <div class="book-price">${{ (book.price / 100).toFixed(2) }}</div>
    <button class="button">Add to Cart</button>
    <button class="button">Read Now</button>
  </li>
</template>

<script>
export default {
  name: "categoryBookListItem",
  props: {
    book: {
      type: Object,
      required: true,
    },
  },
};
</script>
<style scoped>
.book-box {
  display: flex;
  flex-direction: column;
  background-color: var(--card-background-color);
  padding: 1em;
  gap: 0.25em;
}

.book-title {
  font-weight: bold;
  color: #2c3144;
}

.book-author {
  color: #2c3144;
  font-size: medium;
  align-self: flex-end;
}
.book-price {
  color: #2c3144;
  font-size: medium;
  align-self: flex-end;
}

.book-image {
  width: 210px;
  height: auto;
}

.book-image img {
  width: 200px;
  height: auto;
}

main {
  /* border: 2px solid rgb(11, 230, 11); */
  min-height: 81.5vh;
  top: 10%;
  width: 100%;
  display: flex;
  flex-direction: row;
  align-items: center;
  /* position:relative; */
}
</style>
