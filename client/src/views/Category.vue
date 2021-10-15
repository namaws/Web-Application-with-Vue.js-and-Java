<!--  contains html-->
<template>
  <main>
    <div>
      <category-nav></category-nav>
      <category-book-list :books="books"> </category-book-list>
    </div>
  </main>
</template>

<!--contains javaScript-->
<script>
import CategoryNav from "@/components/CategoryNav";
import CategoryBookList from "@/components/CategoryBookList";

export default {
  name: "category",
  components: {
    CategoryNav,
    CategoryBookList,
  },
  // the way to use data dynamically
  data: function () {
    return {
      books: [
        {
          bookId: 1001,
          title: "1984",
          imageFile: "1984.jpg",
          author: "George Orwell",
          price: 699,
          isPublic: true,
        },
        {
          bookId: 1002,
          title: "Romeo and Juliet",
          imageFile: "romeo and juliet.gif",
          author: "Shakespeare",
          price: 1399,
          isPublic: false,
        },
        {
          bookId: 1003,
          title: "Shards of Unity",
          imageFile: "shards of unity.gif",
          author: "JD Jones",
          price: 599,
          isPublic: true,
        },
        {
          bookId: 1004,
          title: "The Four Winds",
          imageFile: "the four winds.jpg",
          author: "Kristin Hannah",
          price: 699,
          isPublic: true,
        },
        // {
        //   bookId: 1005,
        //   title: "The Midnight Library",
        //   imageFile: "the midnight library.jpg",
        //   author: "Matt Haig",
        //   price: 799,
        //   isPublic: true,
        // },
      ],
    };
  },
};
</script>

<!--contains CSS-->
<style scoped></style>
