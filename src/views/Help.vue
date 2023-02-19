<template>
  <app-page back title="Помощь">
    <question-item
      v-for="q in questions"
      :key="q.title"
      :question="q"
    ></question-item>
  </app-page>
</template>


<script>
import AppPage from "../components/ui/AppPage";
import QuestionItem from "../components/question/QuestionItem";

export default {
  setup() {
    const questions = [
      {
        title: "Что есть в данной системе?",
        text: "Тут есть все, для того, чтобы мониторить кому и сколько деняк надо выплатить",
      },
      {
        title: "Как это работает?",
        text: "Система написана на vue 3 с использованием composition API. Сервер с Realtime Database, а так же авторизация реализованы через Firebase.",
      },
      {
        title: "Кто создатель этого гениального приложения?",
        text: "Курденков-Ставицкий Александр Алексеевич",
      },
    ];

    return { questions };
  },
  components: { AppPage, QuestionItem },
};
</script>