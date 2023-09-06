<template>
  <div>
    <h4 class="job-heading">{{ job.jobHeader }}</h4>
    <span class="job-company">{{ job.company }}</span>
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
    <span v-for="skill in job.skillsRequired" :key="skill">{{ skill }}</span>
  </div>
</template>

<script>
export default {
  props: ["job"],
};
</script>

<style>
.job-heading {
  color: #0a95ff;
  margin-bottom: 5px;
}

.job-company {
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

.skills-required span {
  background: white;
  color: #a6a6a6;
  font-size: 14px;
  padding: 2px 8px;
  border: 1px solid #a6a6a6;
  border-radius: 100px;
}
</style>
