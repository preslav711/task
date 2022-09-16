<template>
  <div class="container">
    <div
      class="threat"
      v-for="question in questions"
      :key="question.question_id"
    >
      <div class="threat__left-side">
        <p class="title">{{ question.subject }}</p>
        <p>{{ question.question }}</p>
        <p>{{ question.text }}</p>
      </div>
      <div class="threat__right-side">
        <p>{{ question.team }}</p>
        <p>{{ question.created_at }}</p>
      </div>
    </div>
  </div>
</template>

<script>
import questionsData from "./assets/data.json";

export default {
  data() {
    return {
      questions: questionsData,
    };
  },
};
</script>

<style lang="scss">
  *{
    background-color: #f2f2f2;
  }
.container {
  max-width: 768px;
  min-width: 320px;
  margin: 0 auto;
  .threat {
    font-family: 'Comfortaa', cursive;
    padding: 10px;
    margin: 1.5rem 0;
    border-radius: 0.5rem;
    box-shadow: rgba(0, 0, 0, 0.07) 0px 1px 2px, rgba(0, 0, 0, 0.07) 0px 2px 4px,
      rgba(0, 0, 0, 0.07) 0px 4px 8px, rgba(0, 0, 0, 0.07) 0px 8px 16px,
      rgba(0, 0, 0, 0.07) 0px 16px 32px, rgba(0, 0, 0, 0.07) 0px 32px 64px;
    display: flex;
    justify-content: space-between;
    font-size: 0.8rem;
    color: #999999;

    &__left-side{
      display: inline-block;
    }

    &__right-side{
      display: inline-block;
    }

    .title {
      font-size: 1rem;
      color: #9335ff;
    }
  }
}
</style>
