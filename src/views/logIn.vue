<template>
<table>
<tr>
<td>Email</td>
<td><input type="text" v-model="inputEmail"></td>
</tr>
<tr>
<td>password</td>
<td><input type="text"  v-model="inputPassword"></td>
</tr>
<tr>
<td></td>
<td><button @click="navHome" >LogIn</button></td>
</tr>
</table>
<h1>{{logged}}</h1>
</template>
<script setup>
// import router from '@/router'
import {useRouter} from "vue-router"
import {ref,watch} from 'vue';
import data from '../data.json'
const inputEmail=ref('');
const inputPassword=ref('')
const logged=ref('')
const router=useRouter();
console.log(data)
console.log(inputEmail.value)

const navHome = () => {
  const user = data.find(u => u.email === inputEmail.value && u.password === inputPassword.value);

  if (user) {
    logged.value = user.name;
    alert("User Found");
    router.push({ name: 'cart', params: { userId: user.email } });
  } else {
    alert("User not found");
  }
}

</script>