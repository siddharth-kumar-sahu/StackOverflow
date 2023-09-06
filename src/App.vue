<template>
  <div class="container">
    <Sidebar />
    <div class="main-content">
      <Navigation @search="search" />
      <div class="questions-jobs-section">
        <QuestionSection :searchTerm="searchTerm" />
        <JobNetwork />
      </div>
    </div>
  </div>
  <Footer />
</template>

<script>
import Sidebar from "./components/Sidebar";
import QuestionSection from "./components/QuestionSection";
import JobNetwork from "./components/JobNetwork";
import Footer from "./components/Footer";
import Navigation from "./components/Navigation";

export default {
  name: "App",
  components: {
    Sidebar,
    QuestionSection,
    JobNetwork,
    Footer,
    Navigation,
  },
  data() {
    return {
      searchTerm: "html",
    };
  },
  methods: {
    search(searchTerm) {
      this.searchTerm = searchTerm;
      console.log(this.searchTerm);
    },
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
  font-family: "Manrope", sans-serif;
  font-style: normal;
  font-weight: normal;
}

.container {
  display: grid;
  grid-template-columns: 1fr 5fr;
}

.main-content {
  display: flex;
  flex-direction: column;
}

.questions-jobs-section {
  display: grid;
  grid-template-columns: 3.5fr 1.5fr;
}

.title {
  padding: 0px 32px;
  margin-bottom: 32px;
  position: relative;
}

.title-heading {
  color: #e4e4e4;
  font-size: 96px;
  font-weight: 600;
}

.title-subheading {
  font-size: 20px;
  color: #a6a6a6;
  left: 24px;
  top: 40%;
  position: absolute;
}
</style>
