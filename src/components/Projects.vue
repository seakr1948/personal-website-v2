<template>
  <section id="projects">
    <h2>My Projects</h2>

    <div class="projects-container flex">
      <div v-for="(element, index) in PROJECTS" :key="index">
      <project-card v-bind="element" />
    </div>
    </div>
    
  </section>
</template>

<script>
import ProjectCard from "./ProjectCard.vue";

const projects = [
  {
    project: "MySpotifyInsights",
    image: 'MySpotifyInsights.png',
    description:
      "Senior project created with React that utilizes the spotify API to display the user data related to their music habits. Utilized React for the front end and Flask for the back end. My duties were to help develop the front end and implement some key functions like playing music samples",
    technologies: ["React", "CSS", "Flask"],
    site_url: "https://my-spotify-insights.herokuapp.com/",
    repo_url: "https://github.com/magacula/my-spotify-insights"
  },
  {
    project: "Calculator App",
    image: "Calculator-App.png",
    description:
      "This calculator app was created in React and is the first project I have that utilized SCSS. This was a great project to implement Sass since I utilized mixins in order to create different themes using mixins.",
    technologies: ["React", "SCSS"],
    site_url: "https://fn-calculator-app.netlify.app/",
    repo_url: "https://github.com/seakr1948/calculator-app"
  },
  {
    project: "The Auto Logger",
    image: "the-auto-logger.png",
    description:
      "Developed an app that allows a user to log the fuel efficiency of their vehicles and useful statistics over the tracked fuel logs.",
    technologies: ["React", "Express", "BootStrap"],
    site_url: "https://the-auto-logger.herokuapp.com/",
    repo_url: "https://github.com/seakr1948/the-auto-logger"
  },
  {
    project: "YelpCamp",
    image: "yelpcamp.png",
    description:
      "Designed an app that works similarly to Yelp, but utlilzes campgrounds instead of restaurants",
    technologies: ["Express", "EJS", "BootStrap"],
    site_url: "https://rocky-castle-04339.herokuapp.com/",
    repo_url: "https://github.com/seakr1948/YelpCamp"
  },
];
export default {
  components: { ProjectCard },
  name: "Projects",
  created() {
    this.PROJECTS = projects;
  },
};
</script>
