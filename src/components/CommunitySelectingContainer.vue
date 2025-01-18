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
    <div id="CommunityInfoSelectBar">
        <button type="button" id="Projects" class="SelectBar">
            作品({{count_projects}})
        </button>
    </div>
</template>
<style scoped>
    .SelectBar {
        background-color: white;
        border-radius: 0px;
        border: 1px solid transparent;
        padding: 0em;
        font-size: 1em;
        font-weight: 500;
        font-family: inherit;
        cursor: pointer;
        transition: border-color 0s;
    }
    .SelectBar button {
        color: #eee;
    }
    .SelectBar button:hover {
        border-color: white;
        color: white;
    }
    .SelectBar button:focus,
    .SelectBar button:focus-visible {
        outline: 0px auto -webkit-focus-ring-color;
    }
    #Projects {
        position: absolute;
        top: 55%;
    }
</style>