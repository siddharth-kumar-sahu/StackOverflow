<template>
  <div class="jobs-network-section">
    <div class="job-section">
      <div class="job-tittle">
        <span class="large">jobs</span>
        <span class="small">looking out for...</span>
      </div>
      <div class="job-details-section">
        <div v-for="job in jobs" :key="job.id" class="job-description">
          <div class="job-header">
            <h4>{{ job.jobHeader }}</h4>
            <span>{{ job.company }}</span>
          </div>
          <div class="job-type-details">
            <div class="company-location">
              <div class="location-icon">
                <ion-icon name="location-outline"></ion-icon>
              </div>
              <div class="company-location-name">{{ job.companyLocation }}</div>
            </div>
            <div class="job-type">
              <div class="type-icon">
                <ion-icon name="globe-outline"></ion-icon>
              </div>
              <div class="office-type">{{ job.officeType }}</div>
            </div>
          </div>
          <div class="skills-required">
            <p v-for="skill in job.skillRequired" :key="skill">{{ skill }}</p>
          </div>
        </div>
        <div class="view-more">
          <h4><a href="#">VIEW ALL JOBS &#8594;</a></h4>
        </div>
      </div>
    </div>
    <NetworkSection />
  </div>
</template>

<script>
import NetworkSection from "./NetworkSection.vue";

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
          skillRequired: ["angular js", "cordova"],
        },
        {
          id: 2,
          jobHeader: "Senior iOS/iPhone Engineer",
          company: "Perk.com INC",
          companyLocation: "Bengaluru, India",
          officeType: "In Office",
          skillRequired: ["iOS", "iPhone"],
        },
        {
          id: 3,
          jobHeader: "Software Engineer",
          company: "SparkNET Technologies",
          companyLocation: "No Location",
          officeType: "Remote",
          skillRequired: ["iOS", "ruby on rails"],
        },
      ],
    };
  },
  components: {
    NetworkSection,
  },
};
</script>

<style>
.jobs-network-section {
  /* border: 2px solid green; */
  width: 370px;

  border-left: 1px solid #a6a6a6;
  display: flex;
  flex-direction: column;
  gap: 62px;
  background-color: #f2f2f2;
  /* padding: 20px; */
}

.job-section {
  /* border: 1px solid red; */
}

.job-tittle {
  margin: 0 36px 36px;
  color: #a6a6a6;
  /* position: relative; */
  font-size: 48px;
}

.job-details-section {
  /* border: 1px solid #e57e22; */
  margin: 0 36px 36px;
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
  margin-bottom: 36px;
  border-bottom: 1px solid #a6a6a6;
}

.job-header h4 {
  color: #0074cc;
  margin-bottom: 5px;
}

.job-header span {
  color: #a6a6a6;
}

.job-type-details {
  display: flex;
  gap: 32px;
  font-size: 14px;
  color: #a6a6a6;
}

.company-location,
.job-type {
  display: flex;
  gap: 5px;
}

.skills-required {
  display: flex;
  gap: 10px;
  margin-bottom: 32px;
}

.skills-required p {
  padding: 2px 10px;
  border: 1px solid #a6a6a6;
  border-radius: 100px;
}

.view-more h4 a {
  color: #0074cc;
}
</style>
