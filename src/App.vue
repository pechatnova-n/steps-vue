
<template>
  <main>
    <div class="card">
        <h1>План по изучению Vue.js</h1>
  
        <div class="steps">
          <div class="steps-content">
            Сюда необходимо вывести текст активного шага по его индексу
          </div>
          <ul class="steps-list">
            <li class="steps-item done"><span>1</span> Шаг 1</li>
            <li class="steps-item done"><span>2</span> Шаг 2</li>
            <li class="steps-item active"><span>3</span> Шаг 3</li>
            <li class="steps-item"><span>4</span> Шаг 4</li>
          </ul>
          <div>
            <button class="btn">Назад</button>
            <button class="btn primary">Вперед</button>
          </div>
        </div>

        <CustomInput />
      </div>
  </main>
</template>


<script>
  import CustomInput from './components/CustomInput.vue';
  
  export default {
    name: 'App',

    components: {
      CustomInput
    }, 

    data() {
      return {
        activeIndex: 0, // то, что позволяет определить текущий активный шиг
        steps: [
          {title: 'Основы', text: 'В блоке вы познакомитесь со всеми основами Vue.js на практике. На протяжении блока мы напишем реактивное приложение, в процессе разработки которого разберем вся базу фреймворка.'},
          {title: 'Компоненты', text: 'Один из самых важных блоков в курсе, где вы узнаете все о компонентах. В блоке мы напишем 2 разных приложения и создадим более 5 различных UI компонентов как в реальной разработке. Блок расскажет про абсолютно все составляющие, которые есть в компонентах: взаимодействие, slots, асинхронные и динамические компоненты и тонна примеров.'},
          {title: 'Роутер', text: 'В данном блоке вы узнаете все о том, как работает мультиязычность во Vue. Мы создадим миниклон Gmail в данном блоке, где вы на практике увидите как работать с динамическим роутером.'},
          {title: 'Vuex', text: 'В блоке вы узнаете абсолютно все про Vuex. Вы узнаете как работать с данными, какие есть лучшие практики по их программированию и структурированию. Все на практике.'},
          {title: 'Composition', text: 'Одним из наиболее важных обновлений в Vue 3 является появление альтернативного синтаксиса Composition API. В этом блоке вы узнаете все, чтобы полностью пользоваться данными синтаксисом на практических примерах. Помимо этого вы узнаете как работать совместно с Vue Router и Vuex.'},
        ]
      }
    },
    

  methods: {
    prev() {
      // когда нажимаем кнопку назад
    },
    reset() {
      // начать заново
    },
    nextOfFinish() {
      // кнопка вперед или закончить
    },
    setActive(idx) {
      // когда нажимаем на определенный шаг
    }
  },
  computed: {
    // тут стоит определить несколько свойств:
    // 1. текущий выбранный шаг
    // 2. выключена ли кнопка назад
    // 3. находимся ли мы на последнем шаге
  }
}

</script>



<style scoped>

.card {
  padding: 1rem;
  border-radius: 10px;
  box-shadow: 2px 3px 10px rgba(0, 0, 0, 0.2);
  background: #fff;
}

.card.center {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.steps {
  position: relative;
}

.steps-list {
  list-style: none;
  margin: 0;
  margin-bottom: 1rem;
  padding: 0;
  display: flex;
  justify-content: space-between;
}

.steps-item span {
  cursor: pointer;
  border-radius: 50%;
  padding: .75rem 1rem;
  font-size: .75rem;
  background: #cccccc;
}

.steps-content {
  margin-bottom: 1rem;
}

.steps-item.active span, .steps-item.done span {
  background: #42b983;
}

.steps-item.active span {
  font-weight: bold;
  color: #ffffff;
}
</style>
