<template>
  <div class="question-section">
    <div class="question-title">
      <span class="small">Question</span>
      <span class="large">Top</span>
    </div>
    <nav class="question-navbar">
      <ul class="main-nav-list">
        <li><a class="main-nav-link" href="#">interesting</a></li>
        <li>
          <a class="main-nav-link" href="#">featured <span>432</span></a>
        </li>
        <li>
          <a class="main-nav-link" href="#">hot</a>
        </li>
        <li><a class="main-nav-link" href="#">week</a></li>
        <li>
          <a class="main-nav-link" href="#">month</a>
        </li>
      </ul>
    </nav>
    <div class="question-content">
      <div v-for="question in questions" :key="question.id" class="question">
        <Question :question="question" :time="activityTime" />
      </div>
    </div>
    <div class="question-section-logo">
      <img src="../assets/SCR-20230901-mssm.png" alt="stackoverflow" />
      <h2>Looking for more?</h2>
      <p>
        Browse the <span>complete list of questions, </span>or<span>
          popular tags</span
        >. Help us answer <br />unanswered questions.
      </p>
    </div>
  </div>
</template>

<script>
import Question from "./Question";
import moment from "moment";

export default {
  data() {
    return {
      questions: [],
    };
  },
  components: {
    Question,
  },
  async mounted() {
    try {
      const apiUrl =
        "https://api.stackexchange.com/2.3/questions?key=U4DMV*8nvpm3EOpvf69Rxw((&site=stackoverflow&order=desc&sort=activity&filter=default";
      const res = await fetch(apiUrl);
      const data = await res.json();

      const questions = data.items.map((item) => {
        const question = {
          id: item.question_id,
          title: item.title,
          updatedAt: moment.unix(item.last_activity_date).fromNow(),
          updatedBy: item.owner.display_name,
          tags: item.tags,
          votes: item.score,
          answer: item.answer_count,
          views: item.view_count,
        };
        console.log(
          moment.unix(item.last_activity_date).fromNow(),
          item.last_activity_date
        );
        console.log(question.updatedAt);
        return question;
      });

      this.questions = questions;
    } catch (e) {
      console.log(e);
    }
  },
};
</script>

<style>
.question-section {
  /* border: 2px solid red; */
  width: 900px;
}

.question-title {
  margin: 20px 42px 42px;
  color: #a6a6a6;
  /* position: relative; */
  font-size: 48px;
}

.question-navbar {
  /* border: 2px solid black; */
  padding: 10px 0 18px 42px;
  border-bottom: 1px solid #a6a6a6;
}

.question-navbar li a span {
  border: 1px solid #a6a6a6;
  border-radius: 50px;
  padding: 0 5px;
  margin-left: 5px;
  font-weight: 500;
  color: #e57e22;
}

.main-nav-list {
  list-style: none;
  display: flex;
  align-items: center;
  gap: 42px;
}

.main-nav-list a {
  display: inline-block;
  text-decoration: none;
  color: #a6a6a6;
  font-weight: 400;
  font-size: 18px;
}
.question-content {
  padding: 0 42px;
  height: 100vh;
  overflow-y: auto;
}
.question {
  /* border: 1px solid deeppink; */
  display: flex;
  justify-content: space-between;
  margin: 20px 0;
  border-bottom: 1px solid #a6a6a6;
}

.question-section-logo {
  display: flex;
  flex-direction: column;
  gap: 24px;
  align-items: center;
  justify-content: center;
  margin: 98px 0;
}

.question-section-logo h2,
p {
  color: #a6a6a6;
}

.question-section-logo p {
  text-align: center;
}

.question-section-logo p span {
  color: #0074cc;
}
</style>
