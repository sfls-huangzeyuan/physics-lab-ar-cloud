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
  id_signature: string;
  have_premier_account: bool;
}>();
</script>

<template>
    <button type="button" id="#BasicInfoPopUp" @click="ShowBasicInfo= true" style="background-color: #00a9ff; color: white; position: absolute; left: 5%; width: 42.5%; top: 45%">
        基本信息
    </button>
    <button type="button" id="#SecurityCenterPopUp" @click="ShowSecurity= true" style="background-color: #cce5fa; color: black; position: absolute; left: 52.5%; width: 42.5%; top: 45%">
        安全中心
    </button>
    <transition name="fade">
        <div v-if="ShowBasicInfo" class="modal" id="BasicInfoPopUpMenu" style="position: absolute; top: 100px; left: 50px">
            <ul id="BasicInfo">
                    <li id="BasicInfoUsername">
                        <p style="color: black; width: auto; height: auto; position: relative; top: 15%; left: 7.5%; font-size: 12px"><strong>{{ username }}</strong></p>
                    </li>
                    <li id="BasicInfoUserTag">
                        <p style="color: lightgray; width: auto; height: auto; position: relative; top: 20%; left: 7.5%; font-size: 10px">{{ user_tag }}</p>
                    </li>
                </ul>
        </div>
        <div id="BasicInfoWrap" @click="ShowBasicInfo= true" style="display: none"></div>
    </transition>
</template>
<style scoped>
    #BasicInfo {
        list-style-type: none;
        display: flex;
        position: absolute;
        top: 20%;
        left: 15%;
        bottom: 20%;
        right: 15%;
        width: 70%;
        height: 60%;
        z-index: 100;
    }
    #BasicInfoWrap {
        display: none; 
        position: absolute;
        top: 0%;
        left: 0%;
        width: 100%;
        height: 100%;
        background-color: #f0f0f050;
        -webkit-backdrop-filter: blur(5px);
        backdrop-filter: blur(5px);
        z-index: 50;
    }
    #BasicInfoPopUp {
        display: none; 
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
    #BasicInfoPopUpMenu {
        display: none;
        background-color: lightgray;
        border-radius: 5%;
        border: none;
        text-align: center;
        text-decoration: none;
        font-size: 16px;
        margin: 4px 2px;
        cursor: pointer;
        position: absolute;
        top: 25%;
        left: 15%;
        bottom: 25%;
        right: 15%;
        width: 70%;
        height: 50%;
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
    button{
        border-radius: 8px;
        border: 1px solid transparent;
        padding: 0.6em 1.2em;
        font-size: 1em;
        font-weight: 500;
        font-family: inherit;
        cursor: pointer;
        transition: border-color 0.25s;
    }
        button:hover {
        border-color: #646cff;
    }
    button:focus,
    button:focus-visible {
        outline: 4px auto -webkit-focus-ring-color;
    }
</style>
