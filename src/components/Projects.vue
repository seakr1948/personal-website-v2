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
    project: "NFT Card Component",
    image: "NFT-Card-Component.png",
    description:
      "This project is a simple component that displays an NFT card. Used simple HTML and CSS",
    technologies: ["HTML", "CSS"],
    site_url: "https://fn-nft-card-component.netlify.app/",
    repo_url: "https://github.com/seakr1948/NFT-preview-card"
  },
  {
    project: "Ecommerce Page",
    image: "Ecommerce-Page.png",
    description:
      "In this project, I utilized React create the different components necessary for the website. I also utilized Bootstrap to style the site to familiarize myself with the CSS framework",
    technologies: ["React", "CSS"],
    site_url: "https://fn-ecommerce-site.netlify.app/",
    repo_url: "https://github.com/seakr1948/ecommerce-product-page"
  },
  {
    project: "Tip Calculator App",
    image: "Tip-Calculator-App.png",
    description: "The tip calculator was created in React and ",
    technologies: ["React", "CSS", "Flask"],
    site_url: "https://fn-tip-calculator.netlify.app/",
    repo_url: "https://github.com/seakr1948/tip-calculator-app"
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
    project: "Time Tracking Dashboard",
    image: "Time-Tracking-Dashboard.png",
    description:
      "This simple React app let me familiarize myself with importing information using the included JSON file. It also familiarized me with media queries for different screen sizes.",
    technologies: ["HTML", "CSS", "React"],
    site_url: "https://fn-time-tracking-dashboard.netlify.app/",
    repo_url: "https://github.com/seakr1948/time-tracking-dashboard"
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