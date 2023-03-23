<template>
  <div>
    <h1>Projects</h1>
    <div id="project-list">
      <div
        class="project"
        v-for="project in this.projects"
        v-bind:key="project.projectName"
      >
        <div id="project-name-links">
          <h3>{{ project.projectName }}</h3>
          <div>
            <a
              v-for="link in project.links"
              v-bind:key="link.index"
              :href="link.url"
            >
              <img
                id="link-icon"
                :src="require(`@/assets/tech/${link.icon}`)"
                :alt="link.linkName"
              />
            </a>
          </div>
        </div>
        <div id="project-detail">
          <p>{{ project.description }}</p>
          <ul>
            <li>Tech Stack: {{ project.techStack }}</li>
            <li>Images</li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      projects: [
        {
          projectName: "Unit Conversion Application",
          description:
            "A CLI based Unit Conversion application that converts values individually through the command line interface or automatic bulk conversion through CSV input. Provides several unit conversion options in one single app.",
          skills: "C#, OOP, User IO, File IO, Unit Testing",
          techStack: "C#",
          images: [],
          links: [
            {
              linkName: "Code Repo",
              icon: "github.png",
              url: "https://github.com/a-ahrens/CSharpPlayground",
            },
            {
              linkName: "Youtube application showcase",
              icon: "youtube.png",
              url: "https://youtu.be/G6hqoFIx0Tk",
            },
          ],
        },
        {
          projectName: "Paddler App",
          description:
            "An application designed to help paddlers check the conditions of their trips.",
          skills: "",
          techStack:
            "Java, PostgreSQL, Spring-Boot, HTML, CSS, Javascript, Vuejs",
          images: ["", "", ""],
          links: [
            {
              linkName: "Paddler App Project Repo",
              icon: "github.png",
              url: "https://github.com/a-ahrens/Kudo_Kademy"
            },
            {
              linkName: "Youtube App Overview",
              icon: "youtube.png",
              url: "https://youtu.be/PkBsPErYmSc",
            },
          ],
        },
        {
          projectName: "Kudo Kademy",
          description:
            "Teachers are able to award a student's good behavior by giving them kudos. Kids earn points with each kudo and compete with other students.",
          skills: "",
          techStack:
            "Java, PostgreSQL, Spring-Boot, HTML, CSS, Javascript, Vuejs",
          images: [],
          links: [
            {
              linkName: "Kudo Kademy Project Repo",
              icon: "github.png",
              url: "https://github.com/a-ahrens/Kudo_Kademy"
            }
          ],
        },
        {
          projectName: "Tenmo Cash App",
          description:
            "Designed and built a backend application that simulates payment requests and transfers between users.",
          skills: "",
          techStack: "Java, PostgreSQL, Spring-Boot",
          images: [],
          links: [
            {
              linkName: "Tenmo Cash App Project Repo",
              icon: "github.png",
              url: "https://github.com/a-ahrens/Tenmo_Cash_App"
            }
          ],
        },
        {
          projectName: "Vending Machine App",
          description:
            "A CLI based application that simulates the functionality of a standard snack vending machine.",
          skills: "",
          techStack: "Java",
          images: [],
          links: [
            {
              linkName: "Vending Machine Project Repo",
              icon: "github.png",
              url: "https://github.com/a-ahrens/TEVendingMachine"
            }
          ],
        },
      ],
    };
  },
};
</script>

<style scoped>
#link-icon {
  width: 50px;
  height: 50px;
}

.project {
  text-align: left;
  padding: 20px;
}

#project-detail {
  max-width: 400px;
  border: 2px solid;
  padding: 20px;
}

#project-list {
  display: flex;
  justify-content: space-evenly;
  flex-wrap: wrap;
}

#project-name-links {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: aliceblue;
  padding: 0 10px 0 10px;
  color: black;
}
</style>