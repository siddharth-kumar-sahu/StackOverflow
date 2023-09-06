<template>
  <div class="question-details">
    <div class="question-header">
      <h3>{{ question.title }}</h3>
    </div>
    <div class="question-tags">
      <p v-for="tag in question.tags" :key="tag">{{ tag }}</p>
    </div>
    <div class="question-activity">
      <p>
        modified {{ question.updatedAt }} secs ago by
        <strong>{{ question.updatedBy }}</strong>
      </p>
    </div>
  </div>
  <div class="review-details">
    <div class="review-details-section">
      <div class="vote-count">{{ question.votes }}</div>
      <div class="vote">votes</div>
      <div class="vote-icon">
        <ion-icon name="thumbs-up-outline"></ion-icon>
      </div>
    </div>
    <div class="review-details-section">
      <div class="answer-count">{{ question.answer }}</div>
      <div class="answer">answers</div>
      <div class="answer-icon">
        <ion-icon name="chatbox-outline"></ion-icon>
      </div>
    </div>
    <div class="review-details-section">
      <div class="view-count">{{ question.views }}</div>
      <div class="views">views</div>
      <div class="view-icon">
        <ion-icon name="eye-outline"></ion-icon>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["question"],
};
</script>

<style>
.question-details {
  display: flex;
  flex-direction: column;
  gap: 20px;
  margin-bottom: 24px;
}

.question-header {
  padding: 0;
  color: #0074cc;
}

.question-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  color: #a6a6a6;
}

.question-tags p {
  padding: 2px 10px;
  border: 1px solid #a6a6a6;
  border-radius: 100px;
}

.question-activity {
  color: #a6a6a6;
}

.review-details {
  display: flex;
  gap: 48px;
  align-items: center;
  color: #a6a6a6;
}

.review-details-section {
  display: flex;
  flex-direction: column;
  gap: 12px;
  text-align: center;
}
</style>
