<template>
  <main>
    <div class="container grid--2-cols">
      <Sidebar />
      <div class="main-content">
        <div class="primary-header">
          <div class="menu-option">
            <ion-icon class="menu-icon" name="menu-outline"></ion-icon>
          </div>
          <div class="search">
            <ion-icon class="search-icon" name="search-outline"></ion-icon>
            <input type="text" name="q" placeholder="Search" />
          </div>
          <div class="profile">
            <div class="help">
              <ion-icon name="help-buoy-outline"></ion-icon>
              <p>Help</p>
            </div>
            <div class="tour">
              <ion-icon name="desktop-outline"></ion-icon>
              <p>Tour</p>
            </div>
            <div class="profile-pic">
              <img src="./assets/Siddharth-min.jpeg" alt="Siddharth" />
            </div>
          </div>
        </div>
        <div class="questions-jobs-section">
          <QuestionSection />
          <JobNetworkSection />
        </div>
      </div>
    </div>
  </main>
  <FooterSection />
</template>

<script>
import Sidebar from "./components/Sidebar";
import QuestionSection from "./components/QuestionSection";
import JobNetworkSection from "./components/JobNetworkSection";
import FooterSection from "./components/FooterSection";

export default {
  name: "App",
  components: {
    Sidebar,
    QuestionSection,
    JobNetworkSection,
    FooterSection,
  },
};
</script>

<style>
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
#app {
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-kerning: auto;
  font-stretch: normal;
  font-style: normal;
  font-variant: normal;
  font-variant-ligatures: normal;
  font-weight: normal;
}
.container {
  max-width: 1500px;

  /* padding: 0 32px; */
  /* margin: 0 32px; */
  display: grid;
  /* border-bottom: 1px solid #a6a6a6; */
}
.grid--2-cols {
  grid-template-columns: 230px 1270px;
}

.main-content {
  /* border: 2px solid blue; */

  max-width: 1500px;
  display: flex;
  flex-direction: column;
  /* justify-content: center; */
}
.primary-header {
  max-width: 1270px;
  /* border: 2px solid lightgreen; */
  margin: 20px;
  display: flex;
  gap: 20px;
  align-items: center;
}

.menu-icon,
.search-icon {
  color: #a6a6a6;
  height: 24px;
  width: 24px;
}

.search {
  display: flex;
  gap: 8px;
  align-items: center;
}
.search input {
  display: block;
  padding: 10px 6px;
  /* width: 100%; */
  box-sizing: border-box;
  border: none;
  color: #a6a6a6;
  height: 42px;
  width: 900px;
}

.profile {
  display: flex;
  align-items: center;
  gap: 24px;
}

.help,
.tour {
  display: flex;
  align-items: center;
  gap: 8px;
}

.profile-pic img {
  height: 30px;
  width: 30px;
  border-radius: 50%;
}

.questions-jobs-section {
  display: flex;
}
</style>
