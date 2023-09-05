<template>
  <main>
    <div class="container grid--2-cols">
      <Sidebar />
      <div class="main-content">
        <div class="nav-bar">search and nav section</div>
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

  /* max-width: 1500px; */
  display: flex;
  flex-direction: column;
  /* justify-content: center; */
}
.nav-bar {
  max-width: 1270px;
  border: 2px solid lightgreen;
}

.questions-jobs-section {
  display: flex;
}
</style>
