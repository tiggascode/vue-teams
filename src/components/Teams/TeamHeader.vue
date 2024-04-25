<script setup>
import {useTeamStore} from "@/stores/TeamStore.js";
import AddMemberModal from "@/components/Teams/AddMemberModal.vue";

let team = useTeamStore();
team.fill();
</script>

<template>
    <header class="flex mt-6  px-9 py-5 justify-between">
        <div>
            <AddMemberModal/>
        </div>
        
        <div>
            <h3 class="inline-flex items-center text-3xl relative">
                <!--<img src="/smiley.png" class="mr-2">-->
                {{team.name}} Team
                <div class="bg-green-400 w-5 h-5 text-xs text-white rounded-full flex justify-center items-center absolute -right-4 -top-2">{{team.spots}}</div>
            </h3>
        </div>
    </header>
</template>