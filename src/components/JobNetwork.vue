<template>
  <div class="jobs-network-section">
    <div class="job-section">
      <div class="title">
        <span class="title-heading">jobs</span>
        <span class="title-subheading">Looking out for...</span>
      </div>
      <div class="job-details-section">
        <div v-for="job in jobs" :key="job.id" class="job-description">
          <Job :job="job" />
        </div>
        <div class="view-more">
          <h4><a href="#">VIEW ALL JOBS &#8594;</a></h4>
        </div>
      </div>
    </div>
    <Network />
  </div>
</template>

<script>
import Network from "./Network.vue";
import Job from "./Job.vue";

export default {
  data() {
    return {
      jobs: [
        {
          id: 1,
          jobHeader: "Front End Developer with Angular",
          company: "WalletHub",
          companyLocation: "Washington DC",
          officeType: "Remote",
          skillsRequired: ["angular js", "cordova"],
        },
        {
          id: 2,
          jobHeader: "Senior iOS/iPhone Engineer",
          company: "Perk.com INC",
          companyLocation: "Bengaluru, India",
          officeType: "In Office",
          skillsRequired: ["iOS", "iPhone"],
        },
        {
          id: 3,
          jobHeader: "Software Engineer",
          company: "SparkNET Technologies",
          companyLocation: "No Location",
          officeType: "Remote",
          skillsRequired: ["iOS", "ruby on rails"],
        },
      ],
    };
  },
  components: {
    Network,
    Job,
  },
};
</script>

<style>
.jobs-network-section {
  border-left: 1px solid #e4e4e4;
  display: flex;
  flex-direction: column;
  gap: 62px;
  background-color: #f8f9f9;
}

.job-details-section {
  /* border: 2px solid red; */
  height: 560px;
  padding: 20px 36px 0;
  display: flex;
  flex-direction: column;
  justify-content: center;
  gap: 12px;
}

.job-description {
  /* margin: 0 36px 36px; */
  display: flex;
  flex-direction: column;
  justify-content: center;
  gap: 12px;
  margin-bottom: 18px;
  border-bottom: 1px solid #a6a6a6;
}

.view-more h4 a {
  color: #0a95ff;
}
</style>
