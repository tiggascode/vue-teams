<script setup>
import TeamMembers from "@/components/Teams/TeamMembers.vue";
import TeamHeader from "@/components/Teams/TeamHeader.vue";
import TeamFooter from "@/components/Teams/TeamFooter.vue";
import {useTeamStore} from "@/stores/TeamStore.js";


let team = useTeamStore();
team.fill();


</script>

<template>

    <TeamHeader/>
    
    <div class="place-self-center m-auto flex flex-col gap-y-3" style="width: 725px">
        <TeamMembers/>
    </div>
    
    <TeamFooter/>
    
    
</template>