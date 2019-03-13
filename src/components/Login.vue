<template>
  <div calss="container">
    <x-headr :left-option="{showback: ture}">登陆</x-headr>
    <group title="用户">
      <x-input title="手机号" mask="" v-model="phone" :max="13" is-type="china-mobile"></x-input>
      <x-input title="密码" type="password" v-model="password" :max="13" is-type="china-mobile"></x-input>
  </div class="btn">
</template>

<script>
import { XInput, Group, XButton, Cell , XHeader, AlertModule, Alter} from 'vux'

export default {
  components: {
    XInput,
    XButton,
    Group,
    Cell
  },   
</script>
</style>