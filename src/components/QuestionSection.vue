<template>
  <div class="question-section">
    <div class="title">
      <span class="title-heading">top</span>
      <span class="title-subheading">Questions</span>
    </div>
    <QuestionNav />
    <div class="question-content">
      <div v-for="question in questions" :key="question.id" class="question">
        <Question :question="question" />
      </div>
      <Loader v-if="loading" />
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
import QuestionNav from "./QuestionNav";
import Question from "./Question";
import Loader from "./Loader";
import moment from "moment";

export default {
  data() {
    return {
      questions: [],
      loading: true,
    };
  },
  components: {
    QuestionNav,
    Question,
    Loader,
  },
  async mounted() {
    try {
      this.loading = true;
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
        return question;
      });

      this.questions = questions;
      this.loading = false;
    } catch (e) {
      this.loading = false;
    }
  },
};
</script>

<style>
.question-section {
  border-top: 1px solid #f8f9f9;
}

.question-content {
  padding: 0 42px;
  height: 1000px;
  overflow-y: auto;
}
.question {
  /* border: 1px solid deeppink; */
  display: flex;
  gap: 80px;
  justify-content: space-between;
  margin: 20px 0;
  border-bottom: 1px solid #f8f9f9;
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
