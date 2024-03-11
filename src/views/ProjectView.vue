<template>
    <p class="text-center mb-3 dark:text-blue-300">Here's some stuff I've worked on...</p>
    <div class="max-h-[50vh] overflow-auto sm:w-4/12 mx-auto">
        <!-- Static projects list -->
        <div class="bg-blue-300 mb-4 p-2 rounded-md shadow-md" v-for="(project, index) in projects" :key="index">
            <a :href="project.html_url" target="_blank">
                <h2 class="font-bold text-xl">{{ project.name }}</h2>
                <p>{{ project.description }}</p>
            </a>
        </div>
    </div>
</template>

<script setup>
// Removed the dynamic loading logic
const projects = [
    {
        id: 1,
        name: 'Intelligent Digit Interpreter',
        description: 'An interactive ML application designed to recognize handwritten digits in real-time.',
        html_url: 'https://github.com/yourusername/project-1'
    },
    {
        id: 2,
        name: 'Note to Self',
        description: 'A React Native application designed to act as a proactive tool during emotional crises.',
        html_url: 'https://github.com/yourusername/project-2'
    },
];
</script>

<style scoped>
/* Add any additional styling here */
</style>
