<template>
  <div class="about-section">
    <div id="bio-section">
      <img
        id="personal-photo"
        :src="require(`@/assets/Me/${myPhoto}`)"
        alt=""
      />
      <div id="bio">
        <h1>About Me</h1>
        <p>
          Greeting/Backstory <br />
          "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
          eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad
          minim veniam, quis nostrud exercitation ullamco laboris nisi ut
          aliquip ex ea commodo consequat. Duis aute irure dolor in
          reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla
          pariatur. Excepteur sint occaecat cupidatat non proident, sunt in
          culpa qui officia deserunt mollit anim id est laborum."
        </p>

        <p>
          Goals/Passions <br />
          "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
          eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad
          minim veniam, quis nostrud exercitation ullamco laboris nisi ut
          aliquip ex ea commodo consequat. Duis aute irure dolor in
          reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla
          pariatur. Excepteur sint occaecat cupidatat non proident, sunt in
          culpa qui officia deserunt mollit anim id est laborum."
        </p>
      </div>
    </div>
    <div>
      <h2>Technologies</h2>
      <p>
        These are some of the many languages and frameworks I have worked with.
      </p>
      <div id="technologies-wrapper">
        <div id="technologies">
          <div
            class="tech-logo-container"
            v-for="tech in this.technologies"
            v-bind:key="tech.language"
          >
            <img
              class="tech-logo"
              :title="tech.language"
              :src="require(`@/assets/tech/${tech.image}`)"
              alt="technology type"
            />
          </div>
        </div>
      </div>
    </div>
    <h3>Interests</h3>
    <div>Projects</div>
  </div>
</template>

<script>
//import { defineComponent } from '@vue/composition-api'

export default {
  data() {
    return {
      bio: "Hi, my name is Anthony and I am an aspiring software dev. \n Want to hear more?",
      myPhoto: "driscalSuit.jpg",

      technologies: [
        {
          language: "Java",
          image: "Java.png",
          desciption: "Fundamentals of OOP design and programming.",
        },
        {
          language: "SpringBoot",
          image: "Spring_Boot.png",
          desciption: "Fundamentals of OOP design and programming",
        },
        {
          language: "C#",
          image: "CSharp.png",
          desciption: "Fundamentals of OOP design and programming",
        },
        {
          language: "asp.net",
          image: "asp.net_.png",
          desciption:
            "Knowledge of building out RESTful services through asp,net framework.",
        },
        {
          language: "HTML5",
          image: "HTML5.png",
          desciption: "",
        },
        {
          language: "CSS3",
          image: "CSS3.png",
          desciption: "",
        },
        {
          language: "Javascript",
          image: "Javascript.png",
          desciption: "",
        },
        {
          language: "Vue.JS",
          image: "Vue.png",
          desciption: "",
        },
        {
          language: "MySQL",
          image: "MySQL.png",
          desciption: "",
        },
        {
          language: "PostgreSQL",
          image: "postgresql.png",
          desciption: "",
        },
      ],
    };
  },
};
</script>

<style scoped>
.about-section {
  padding: 0px 25px 25px 25px;
  display: flex;
  flex-direction: column;
}

#bio-section {
  display: flex;
  justify-content: space-evenly;
  flex-wrap: wrap;
  align-items: flex-start;
}

#bio {
  display: flex;
  flex-direction: column;
  text-align: left;
  padding: 25px;
  max-width: 700px;
}

#personal-photo {
  width: 40%;
  max-width: 500px;
  min-width: 250px;
  margin-top: 50px;
  border: 6px solid ;
}

.tech-logo-container {
  margin: 6px 3px 0px 3px;
  background-color: aliceblue;
  display: flex;
  justify-content: center;
  align-items: center;
  width: 65px;
  height: 65px;
  border-radius: 10%;
  border: 3px black solid;
}

.tech-logo {
  max-height: 50px;
}

#technologies {
  position: relative;
  border: none;
  text-align: center;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  padding: 10px;
  margin: -4px -6px -4px -5px;
}

#technologies-wrapper {
  margin: 10px;
  border: 3px dashed greenyellow;
  border-radius: 6px;
}

#technologies::before,
#technologies::after {
  position: absolute;
  width: 60%;
  height: 40%;
  content: "";
}

#technologies::before {
  left: 0;
  top: 0;
  border-left: 10px outset;
  border-top: 6px outset;
  border-radius: 6px;
}

#technologies::after {
  right: 0;
  bottom: 0;
  border-right: 10px inset;
  border-bottom: 6px inset;
  border-radius: 6px;
}
</style>
