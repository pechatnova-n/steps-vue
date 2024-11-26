# steps-vue

This template should help get you started developing with Vue 3 in Vite.

## Recommended IDE Setup

[VSCode](https://code.visualstudio.com/) + [Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar) (and disable Vetur).

## Customize configuration

See [Vite Configuration Reference](https://vite.dev/config/).

## Project Setup

```sh
yarn
```

### Compile and Hot-Reload for Development

```sh
yarn dev
```

### Compile and Minify for Production

```sh
yarn build
```



1. Активный шаг - класс active
2. Пройденный шаг - класс done


1. При клике на кнопку вперед меняется активный шаг (активному шагу добавляется класс active, пройденному шагу - класс done)
2. Вывести текст активного шага под заголовком
3. Кнопка Назад на 1 шаге не активна, после активна, при нажатии - активный шаг смещается назад
4. Когда все шаги пройдены - вместо кнопки вперед появляется кнопка Завершить