<template>
  <div class="side-bar">
    <div class="logo-stackoverflow">
      <img src="../assets/stack_overflow.png" alt="stackoverflow logo" />
    </div>
    <ul class="sidebar-options">
      <li
        class="sidebar-option-components"
        v-for="pageLink in pageLinks"
        :key="pageLink.pageLinkTitle"
        @click="activeLink = pageLink.pageLinkTitle"
        :class="{ 'pageLink-active': pageLink.pageLinkTitle === activeLink }"
      >
        <ion-icon class="sidebar-icon" :name="pageLink.icon"></ion-icon>
        <a href="#">{{ pageLink.pageLinkTitle }}</a>
        <span class="pageLink-item" v-if="pageLink.item">{{
          pageLink.item
        }}</span>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      pageLinks: [
        {
          pageLinkTitle: "QUESTIONS",
          icon: "help-outline",
        },
        {
          pageLinkTitle: "JOBS",
          icon: "bag-outline",
        },
        {
          pageLinkTitle: "DOCUMENTATION",
          icon: "document-text-outline",
        },
        {
          pageLinkTitle: "TAGS",
          icon: "pricetag-outline",
        },
        {
          pageLinkTitle: "USERS",
          icon: "person-outline",
        },
        {
          pageLinkTitle: "BADGES",
          icon: "bookmark-outline",
        },
        {
          pageLinkTitle: "ASK QUESTION",
          icon: "help-outline",
        },
        {
          pageLinkTitle: "STACK EXCHANGE",
          icon: "mic-outline",
        },
        {
          pageLinkTitle: "INBOX",
          icon: "mail-outline",
          item: 24,
        },
      ],
      activeLink: "QUESTIONS",
    };
  },
};
</script>

<style>
.side-bar {
  /* border: 2px solid red; */
  padding-left: 24px;
  box-shadow: 5px 0px 20px rgba(0, 0, 0, 0.1);
}
.logo-stackoverflow {
  padding: 16px 10px;
  margin-bottom: 48px;
}

.logo-stackoverflow img {
  height: 40px;
  width: 152px;
}
.sidebar-options {
  list-style: none;
  display: flex;
  flex-direction: column;
  gap: 25px;
}

.sidebar-option-components {
  display: flex;
  align-items: center;
  gap: 16px;
  padding: 5px 10px;
  border-left: 4px solid transparent;
  padding-left: 18px;
}
.sidebar-options li a {
  font-size: 15px;
  color: #a6a6a6;
}

.sidebar-option-components .pageLink-item {
  border: 1px solid #a6a6a6;
  border-radius: 70px;
  padding: 0 5px;
  margin-left: 5px;
  font-weight: 500;
  color: #f48224;
}

.sidebar-icon {
  color: #a6a6a6;
}

.pageLink-active {
  border-left: 4px solid #f48224;
  padding-left: 18px;
}
</style>
