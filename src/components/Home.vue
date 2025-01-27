<script setup>
import lost_world_img from '@/assets/portfolio/the-lost-world.png'

const languages = ["Rust", "Go", "C#", "Dart", "Python", "Javascript", "Typescript"]
const frameworks = ["Vue.js", "Flutter", "Unity", "Godot", "Raylib", "Avalonia UI", "Blender"]
const projects = [
    {
        image: lost_world_img,
        title: "The Lost World",
        description: "A 3D platformer made using Unity and C#",
        link: "https://t-more1010.itch.io/lost-world"
    }
]

const experience = [
    {
        title: "Freelance Desktop App Developer",
        description: "Creating a desktop app called MedRec for storing medical records electronically using Flutter, Go, and SQLite ",
        color: "blue"
    }, 
    {
        title: "Freelance Desktop App Developer",
        description: "Creating a desktop app called Malalearn that runs on Windows, and Raspberry Pi 4+ for distributing educational videos to remote areas",
        color: "green"
    },

]
</script>

<template>
    <!-- Navigation Bar -->
    <v-app-bar app>
        <v-toolbar-title>Timothy Kandiado</v-toolbar-title>
        <v-spacer></v-spacer>

        <v-btn text href="#about">About</v-btn>
        <v-btn text href="#portfolio">Portfolio</v-btn>
        <v-btn text href="#experience">Experience</v-btn>
        <v-btn text href="#contact">Contact</v-btn>
    </v-app-bar>

    <!-- Hero -->
    <v-container id="hero" class="d-flex align-center justify-center h-50">
        <div>
            <h1>Timothy Kandiado</h1>
            <p class="py-6"> Chemical Engineer | Game Developer | Fullstack Web Developer | Desktop & Mobile App Developer</p>
            <v-btn large href="#portfolio"> View My Work</v-btn>
        </div>
    </v-container>

    <!-- About -->
    <v-container id="about" class="py-12">
        <v-row>
            <v-col cols="12" md="6">
                <h2>About Me</h2>
                <p>
                    A BEng. in Chemical Engineering Graduate with First Class Honours.
                </p>
            </v-col>
        </v-row>
        <v-row>
            <v-col cols="12" md="6">
                <h3>Languages</h3>
                <v-chip-group column>
                    <v-chip v-for="item in languages">{{ item }}</v-chip>
                </v-chip-group>
            </v-col>
            <v-col cols="12" md="6">
                <h3>Frameworks</h3>
                <v-chip-group column>
                    <v-chip v-for="item in frameworks">{{ item }}</v-chip>
                </v-chip-group>
            </v-col>
        </v-row>
    </v-container>

    <!-- Portfolio -->
    <v-container id="portfolio" class="py-12">
        <h2>Portfolio</h2>
        <v-row>
            <v-col cols="12" md="4" v-for="(project, index) in projects" :key="index">
                <v-card>
                    <v-img :src="project.image" height="200px" cover></v-img>
                    <v-card-title> {{ project.title }}</v-card-title>
                    <v-card-text> {{ project.description }}</v-card-text>
                    <v-card-actions>
                        <v-btn text :href="project.link" target="_blank">View</v-btn>
                    </v-card-actions>
                </v-card>
            </v-col>
        </v-row>
    </v-container>

    <!-- Experience -->
    <v-container id="experience" class="py-12">
        <h2>Experience</h2>
        <v-timeline side="end">
            <v-timeline-item v-for="(item, index) in experience" :key="index" :dot-color="item.color">
                <v-card>
                    <v-card-title> {{ item.title }}</v-card-title>
                    <v-card-text> {{ item.description }}</v-card-text>
                </v-card>
            </v-timeline-item>
        </v-timeline>
    </v-container>

    <!-- Contact -->
    <v-container id="contact" class="py-12">
        <h2>Contact</h2>
        
        <a>
            <v-icon icon="mdi: mdi-email"></v-icon>
            kandiadotimothy@gmail.com
        </a>
        <!--
        <div class="social-links mt-4">
            <v-icon v-for="link in links" :href="link.link" :color="link.color">{{ link.icon }}</v-icon>
        </div>
    -->
    </v-container>
</template>