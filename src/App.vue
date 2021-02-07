<template>
<div>
  <Title>Регистрация</Title>
  <Description>Уже есть аккаунт? Войти</Description>
  <form>
    <div class="form-grid">
      <TextField title="Имя" placeholder="Введите Ваше имя" type="text"/>
      <TextField title="Email" placeholder="Введите ваш email" type="email"/>
      <TextField title="Номер телефона" placeholder="Введите номер телефона" type="tel" error="Введено не корректное значение"/>
      <Dropdown title="Язык" placeholder="Введите Ваше имя" type="text"/>
      <Checkbox :checked="false">Принимаю условия использования</Checkbox>
      <Button type="submit">Зарегистрироваться</Button>
    </div>
  </form>
  
</div>
</template>

<script>
import TextField from './components/controls/TextField';
import Dropdown from './components/controls/Dropdown';
import Checkbox from './components/controls/Checkbox';
import Button from './components/controls/Button';
import Title from './components/Title';
import Description from './components/Description';

export default {
  name: 'App',
  components: {
    Title,
    Description,
    TextField,
    Dropdown,
    Checkbox,
    Button,
  }
}
</script>

<style lang="scss">
@import './styles/global.scss';

.form-grid {
  display: flex;
  flex-direction: column;
  gap: 8px;
}
</style>