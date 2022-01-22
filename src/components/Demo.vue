<!--
 Copyright 2022 peter
 
 Licensed under the Apache License, Version 2.0 (the "License");
 you may not use this file except in compliance with the License.
 You may obtain a copy of the License at
 
     http://www.apache.org/licenses/LICENSE-2.0
 
 Unless required by applicable law or agreed to in writing, software
 distributed under the License is distributed on an "AS IS" BASIS,
 WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 See the License for the specific language governing permissions and
 limitations under the License.
-->
<script setup lang="ts">
import { storeToRefs } from "pinia";
import { useStore } from "../store/demo";

const counterStore = useStore();

const { counter, doubleCounter } = storeToRefs(counterStore);
const { increment, resetCounter, randomizeCounter } = counterStore;
</script>

<template>
  <div>
    <div>counter: {{ counter }}</div>
    <div>double counter: {{ doubleCounter }}</div>
    <button @click="increment" type="button">counter++ is: {{ counter }}</button>
    <button @click="resetCounter" type="button">reset counter is: {{ counter }}</button>
    <button @click="randomizeCounter" type="button">
      randomizeCounter counter is: {{ counter }}
    </button>
  </div>
</template>

<style></style>
