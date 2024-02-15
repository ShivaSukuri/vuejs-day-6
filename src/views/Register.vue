<template>
<div class="content" >
<table class="table1">
<tr>
<td>Full Name</td>
<td><input type="text" v-model="user.name"></td>
</tr>
<tr>
<td>Mobie Number</td>
<td><input type="number" v-model="user.mobileNumber"></td>
</tr>
<tr>
<td>Email</td>
<td><input type="email" v-model="user.email"></td>
</tr>
<tr>
<td>password</td>
<td><input type="text" v-model="user.password"></td>
</tr>
<tr>
<td></td>
<td><button  v-on:click="navLogIn">Register</button></td>
</tr>
</table>
</div>
</template>
<script setup>
import router from '@/router';
import {ref,reactive} from 'vue';
import data from '../data.json'
defineEmits(['navLogIn'])

const user={
    name:'',
    mobileNumber:'',
    email:'',
  password:''
  }

const navLogIn = () => {
 router.push('/log-in')
};

</script>
<style>
.content{
  /* position:absolute;
  top:20%;
  left:20% */
}
</style>
