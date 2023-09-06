<template>
  <nav class="question-navbar">
    <ul class="pages">
      <li
        class="page"
        v-for="page in pages"
        :key="page"
        @click="activePage = page.title"
      >
        <a
          href="javascript:void(0)"
          class="page-name"
          :class="{ 'page-active': page.title === activePage }"
        >
          {{ page.title }}
        </a>
        <span class="page-item" v-if="page.items">{{ page.items }}</span>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      pages: [
        {
          title: "interesting",
        },
        {
          title: "featured",
          items: 432,
        },
        {
          title: "hot",
        },
        {
          title: "week",
        },
        {
          title: "month",
        },
      ],
      activePage: "interesting",
    };
  },
};
</script>

<style>
.question-navbar {
  padding: 10px 0 18px 42px;
  border-bottom: 1px solid #e4e4e4;
}

.pages {
  list-style: none;
  display: flex;
  align-items: center;
  gap: 24px;
  font-size: 14px;
}

.page .page-name {
  text-decoration: none;
  font-weight: 400;
  color: #a6a6a6;
  padding: 6px 12px;
}

.page .page-name.page-active {
  color: white;
}

.page .page-item {
  border: 1px solid #a6a6a6;
  border-radius: 50px;
  margin-left: 4px;
  padding: 0 5px;
  color: #f48224;
}

.page-active {
  background: #f48224;
  border-radius: 20px;
  color: white;
}
</style>
