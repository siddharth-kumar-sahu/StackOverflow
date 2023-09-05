<template>
  <div class="jobs-network-section">
    <div class="job-section">
      <div class="job-tittle">
        <span class="large">jobs</span>
        <span class="small">looking out for...</span>
      </div>
      <div class="job-details-section">
        <div class="job-description">
          <div class="job-header">
            <h4>Front End Developer with Angular</h4>
            <span>WalletHub</span>
          </div>
          <div class="job-type-details">
            <div class="company-location">
              <div class="location-icon">
                <ion-icon name="location-outline"></ion-icon>
              </div>
              <div class="company-location-name">Washington DC</div>
            </div>
            <div class="job-type">
              <div class="type-icon">
                <ion-icon name="globe-outline"></ion-icon>
              </div>
              <div class="office-type">Remote</div>
            </div>
          </div>
          <div class="skills-required">
            <p>angular js</p>
            <p>cordova</p>
          </div>
        </div>
        <div class="job-description">
          <div class="job-header">
            <h4>Senior iOS/iPhone Engineer</h4>
            <span>Perk.com INC</span>
          </div>
          <div class="job-type-details">
            <div class="company-location">
              <div class="location-icon">
                <ion-icon name="location-outline"></ion-icon>
              </div>
              <div class="company-location-name">Bengaluru, India</div>
            </div>
            <div class="job-type">
              <div class="type-icon">
                <ion-icon name="globe-outline"></ion-icon>
              </div>
              <div class="office-type">In office</div>
            </div>
          </div>
          <div class="skills-required">
            <p>iOS</p>
            <p>iPhone</p>
          </div>
        </div>
        <div class="job-description">
          <div class="job-header">
            <h4>FSoftware Engineer</h4>
            <span>SparkNET Technologies</span>
          </div>
          <div class="job-type-details">
            <div class="company-location">
              <div class="location-icon">
                <ion-icon name="location-outline"></ion-icon>
              </div>
              <div class="company-location-name">No Location</div>
            </div>
            <div class="job-type">
              <div class="type-icon">
                <ion-icon name="globe-outline"></ion-icon>
              </div>
              <div class="office-type">Remote</div>
            </div>
          </div>
          <div class="skills-required">
            <p>iOS</p>
            <p>ruby on rails</p>
          </div>
        </div>
        <div class="view-more">
          <h4><a href="#">VIEW ALL JOBS &#8594;</a></h4>
        </div>
      </div>
    </div>
    <div class="network-section">
      <div class="network-tittle">
        <span class="large">hot</span>
        <span class="small">network questions</span>
      </div>
      <div class="network-content">
        <div class="network-content-question">
          <div class="network-section-icons">
            <img src="../assets/H-icon.png" alt="H-icon" />
          </div>
          <div class="network-section-question">
            <p>Were there women who were against giving women right to vote?</p>
          </div>
        </div>
        <div class="network-content-question">
          <div class="network-section-icons">
            <img src="../assets/stack.png" alt="stack-icon" />
          </div>
          <div class="network-section-question">
            <p>Why does everybody typedef over C types?</p>
          </div>
        </div>
        <div class="network-content-question">
          <div class="network-section-icons">
            <img src="../assets/bookmark.jpg" alt="book-icon" />
          </div>
          <div class="network-section-question">
            <p>An English word describing a pseudo-job</p>
          </div>
        </div>
        <div class="network-content-question">
          <div class="network-section-icons">
            <img src="../assets/pecock.png" alt="peocock-icon" />
          </div>
          <div class="network-section-question">
            <p>
              When flying on a very tight schedule, are very obligated to run to
              make it to the next gate on a connection?
            </p>
          </div>
        </div>
        <div class="network-content-question">
          <div class="network-section-icons">
            <img src="../assets/bracket.png" alt="bracket-icon" />
          </div>
          <div class="network-section-question">
            <p>Does 1 pixcel have a standard size?</p>
          </div>
        </div>
        <div class="view-more">
          <h4><a href="#">VIEW ALL JOBS &#8594;</a></h4>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
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

.network-section {
  /* border: 1px solid green; */
}

.network-tittle {
  margin: 0 36px 36px;
  color: #a6a6a6;
  /* position: relative; */
  font-size: 48px;
}

.network-content {
  display: flex;
  flex-direction: column;
  gap: 20px;
  margin: 0 36px 36px;
}

.network-content-question {
  display: flex;
  gap: 8px;
  margin-bottom: 20px;
}

.network-section-icons img {
  width: 24px;
}

.network-section-question p {
  color: #0074cc;
}
</style>
