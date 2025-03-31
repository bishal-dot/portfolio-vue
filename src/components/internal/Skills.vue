<script setup>
import { ref } from 'vue';


    const skills = ref([
        {
            name: 'HTML',
            percentage: 90
        },
        {
            name: 'CSS',
            percentage: 90
        },
        {
            name: 'Javascript',
            percentage: 85
        },
        {
            name: 'Vue.js',
            percentage: 80
        },
        {
            name: 'Git & GitHub',
            percentage: 75
        }
    ]);

</script>

<template>
    <div class="skills-container">
        <h2>My Skills</h2>
        <div v-for="skill in skills" :key="skill.name" class="skill">
            <div class="skill-label">
                <p>{{ skill.name }}</p>
                <p>{{ skill.percentage }}</p>
            </div>
            <div class="skill-bar">
                <div class="fill" :style="{ width: skill.percentage + '%'}"></div>
            </div>
        </div>
    </div>
    
</template>