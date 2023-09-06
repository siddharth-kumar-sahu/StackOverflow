<template>
  <div class="primary-header">
    <div class="menu-option">
      <ion-icon class="menu-icon" name="menu-outline"></ion-icon>
    </div>
    <div class="search">
      <ion-icon class="search-icon" name="search-outline"></ion-icon>
      <input
        v-model="searchTerm"
        @keyup="emitSearchTerm"
        type="text"
        name="q"
        placeholder="Search"
      />
    </div>
    <div class="help-tour-profile">
      <div class="help">
        <ion-icon name="help-buoy-outline"></ion-icon>
        <p>Help</p>
      </div>
      <div class="tour">
        <ion-icon name="desktop-outline"></ion-icon>
        <p>Tour</p>
      </div>
      <div class="profile-pic">
        <img src="../assets/Siddharth-min.jpeg" alt="Siddharth" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      searchTerm: "",
    };
  },
  methods: {
    emitSearchTerm() {
      this.$emit("search", this.searchTerm);
    },
  },
};
</script>

<style>
.primary-header {
  margin: 20px;
  display: flex;
  gap: 20px;
  align-items: center;
  height: 32px;
}

.menu-icon {
  color: #a6a6a6;
  height: 24px;
  width: 24px;
}

.search-icon {
  color: #a6a6a6;
  height: 18px;
  width: 18px;
}

.search {
  display: flex;
  gap: 8px;
  align-items: center;
  width: 100%;
}

.search input {
  display: block;
  padding: 10px 6px;
  width: 100%;
  box-sizing: border-box;
  border: none;
  color: #a6a6a6;
  height: 42px;
}

.help-tour-profile {
  display: flex;
  align-items: center;
  gap: 24px;
}

.help,
.tour {
  display: flex;
  align-items: center;
  gap: 8px;
  color: #a6a6a6;
}

.profile-pic img {
  height: 30px;
  width: 30px;
  border-radius: 50%;
}
</style>
