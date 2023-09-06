<template>
  <div class="network-section">
    <div class="title">
      <span class="title-heading">hot</span>
      <span class="title-subheading">Network questions</span>
    </div>
    <div class="network-content">
      <div class="network-content-question">
        <div class="network-section-img">
          <img src="../assets/H-icon.png" alt="H-icon" />
        </div>
        <div class="network-section-question">
          <p>Were there women who were against giving women right to vote?</p>
        </div>
      </div>
      <div class="network-content-question">
        <div class="network-section-img">
          <img src="../assets/stack.png" alt="stack-icon" />
        </div>
        <div class="network-section-question">
          <p>Why does everybody typedef over C types?</p>
        </div>
      </div>
      <div class="network-content-question">
        <div class="network-section-img">
          <img src="../assets/bookmark.jpg" alt="book-icon" />
        </div>
        <div class="network-section-question">
          <p>An English word describing a pseudo-job</p>
        </div>
      </div>
      <div class="network-content-question">
        <div class="network-section-img">
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
        <div class="network-section-img">
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
</template>

<script>
export default {};
</script>

<style>
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

.network-section-img img {
  width: 24px;
  height: img;
}

.network-section-question p {
  color: #0a95ff;
}
</style>
