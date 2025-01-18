<script setup lang="ts">
import { ref } from 'vue';

defineProps<{
  username: string;
  user_id: string;
  user_tag: string;
  count_following: int;
  count_follower: int;
  count_projects: int;
  count_messages: int;
}>();
</script>

<template>
    <button type="button" id="#BasicInfoPopUp" style="background-color: #00a9ff; color: white; position: absolute; left: 5%; width: 42.5%; top: 45%">
        基本信息
    </button>
    <button type="button" id="#SecurityCenterPopUp" style="background-color: #cce5fa; color: black; position: absolute; left: 52.5%; width: 42.5%; top: 45%">
        安全中心
    </button>
</template>
<style scoped>
    #BasicInfoPopUp {
        border: none;
        text-align: center;
        text-decoration: none;
        display: inline-block;
        font-size: 16px;
        margin: 4px 2px;
        cursor: pointer;
        position: absolute;
        top: 100px;
        left: 50px;
    }
    #SecurityCenterPopUp {
        border: none;
        text-align: center;
        text-decoration: none;
        display: inline-block;
        font-size: 16px;
        margin: 4px 2px;
        cursor: pointer;
        position: absolute;
        top: 100px;
        left: 50px;
    }
</style>