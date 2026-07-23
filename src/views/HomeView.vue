<template>
  <div class="portfolio">
    <!-- Scrolled Navbar -->
    <nav class="navbar-scrolled" :class="{ show: scrolled }">
      <div class="container-fluid px-4 h-100">
        <div class="d-flex align-items-center justify-content-end h-100 gap-1">
          <a href="#about" class="nav-link-custom">About me</a>
          <a href="#skills" class="nav-link-custom">Skills</a>
          <a href="#portfolio" class="nav-link-custom">Portfolio</a>
          <a href="#contact" class="btn-contact">CONTACT ME</a>
        </div>
      </div>
    </nav>

    <!-- Hero -->
    <section id="hero" class="hero-section">
      <div class="container position-relative">
        <img src="/assets/logo.svg" alt="Logo" class="hero-logo" />

        <nav class="hero-nav d-none d-lg-flex align-items-center">
          <a href="#about" class="nav-link-custom">About me</a>
          <a href="#skills" class="nav-link-custom">Skills</a>
          <a href="#portfolio" class="nav-link-custom">Portfolio</a>
          <a href="#contact" class="btn-contact">CONTACT ME</a>
        </nav>

        <div class="row hero-content align-items-center">
          <div class="col-lg-6">
            <p class="hero-greeting">Hi, I am</p>
            <h1 class="hero-name">Ed Rascoe Cagatan</h1>
            <p class="hero-title">Junior back-end Developer / UI Designer</p>
            <div class="social-links mt-4">
              <a
                href="mailto:edcagatan00@gmail.com"
                class="social-btn"
                aria-label="Email"
              >
                <img src="/assets/icon-mail.svg" alt="Email" />
              </a>
              <a
                href="https://github.com/Tunying21"
                class="social-btn"
                aria-label="GitHub"
              >
                <img src="/assets/icon-github.svg" alt="GitHub" />
              </a>
              <a
                href="https://www.linkedin.com/in/ed-rascoe-cagatan-317859192"
                class="social-btn"
                aria-label="LinkedIn"
              >
                <img src="/assets/icon-linkedin.svg" alt="LinkedIn" />
              </a>
            </div>
          </div>
          <div class="col-lg-6 hero-photo-wrap flex-column">
            <img
              src="/assets/hero-photo.png"
              alt="Portrait"
              class="hero-photo"
            />
          </div>
        </div>
      </div>
    </section>

    <!-- Summary -->
    <section id="summary" class="summary-section">
      <div class="summary-dark">
        <div class="container position-relative">
          <div class="it-logo d-none d-xl-flex">
            <span>IT</span>
          </div>
          <h2 class="summary-title">Summary</h2>
          <p class="summary-text">
            Detail-oriented and adaptable Information Technology student with
            hands-on internship experience in backend development. Possesses a
            strong foundation in database management, logic formulation, and
            technical problem-solving. Highly teachable and eager to transition
            academic foundations and technical expertise into a long-term role,
            whether in development or remote technical client support. Fully
            equipped for permanent work-from-home operations with a reliable
            internet setup and power backup.
          </p>
          <button type="button" class="btn-outline-custom mt-4 text-white">
            READ MORE
          </button>
        </div>
      </div>
    </section>

    <!-- About -->
    <section id="about" class="about-section text-center">
      <div class="container">
        <div class="section-title-box">
          <h2 class="section-title">About Me</h2>
        </div>
        <p class="about-text">
          My name is Ed Rascoe Cagatan, I'm a Fourth year Information Technology
          student at the Leyte Normal University in Tacloban City. I have been
          learning Front-End and backend technologies for a year and this time
          was just enough for me to make sure that this is my place in the
          industry.
        </p>
        <button type="button" class="btn-outline-custom">EXPLORE</button>
        <div class="separator"></div>

        <div class="row g-4 services-row">
          <div class="col-md-6">
            <div class="service-card text-start">
              <div class="service-icon-placeholder mb-2">✎</div>
              <h3 class="service-title">DESIGN</h3>
              <p class="service-text">
                I can design the site based on your needs and suggestions. I can
                also design the site from scratch and consult you during the
                job.
              </p>
            </div>
          </div>
          <div class="col-md-6">
            <div class="service-card text-start">
              <div class="service-icon-placeholder mb-2">&lt;/&gt;</div>
              <h3 class="service-title">DEVELOPMENT</h3>
              <p class="service-text">
                Based on a project created by me or another one, sent by you, I
                can program the website to be fully functional and responsive.
              </p>
            </div>
          </div>
          <div class="col-12">
            <div
              class="service-card text-center mx-auto"
              style="max-width: 500px"
            >
              <div class="service-icon-placeholder mb-2">⚙</div>
              <h3 class="service-title">MAINTENANCE</h3>
              <p class="service-text">
                In case of any problems or the need for changes, I can introduce
                new functionalities and solutions.
              </p>
            </div>
          </div>
        </div>

        <div class="separator"></div>

        <!-- Skills -->
        <div id="skills" class="skills-section">
          <div class="section-title-box">
            <h2 class="section-title">Skills</h2>
          </div>

          <h3 class="skills-subtitle text-start">USING NOW:</h3>
          <div class="row">
            <div
              v-for="skill in usingNow"
              :key="skill.name"
              class="col-6 col-md-3"
            >
              <div class="skill-item">
                <img :src="skill.icon" :alt="skill.name" class="skill-icon" />
                <p class="skill-label">{{ skill.name }}</p>
              </div>
            </div>
          </div>

          <h3 class="skills-subtitle text-start mt-5">LEARNING:</h3>
          <div class="row">
            <div
              v-for="skill in learning"
              :key="skill.name"
              class="col-6 col-md-3"
            >
              <div class="skill-item">
                <img :src="skill.icon" :alt="skill.name" class="skill-icon" />
                <p class="skill-label">{{ skill.name }}</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Portfolio -->
    <section id="portfolio" class="portfolio-section">
      <div class="portfolio-header">
        <img src="/assets/portfolio-header.jpg" alt="Portfolio header" />
        <div class="portfolio-header-overlay">
          <div class="section-title-box">
            <h2 class="section-title">Portfolio</h2>
          </div>
        </div>
      </div>

      <div class="container-fluid px-0">
        <div class="filter-bar position-relative">
          <button
            v-for="(tab, index) in filterTabs"
            :key="tab"
            type="button"
            class="filter-tab"
            :class="{ active: activeFilter === tab }"
            @click="setFilter(tab, index)"
          >
            {{ tab }}
          </button>
          <div class="filter-underline"></div>
          <div
            class="filter-underline-active"
            :style="filterUnderlineStyle"
          ></div>
        </div>

        <div class="row g-0 project-grid">
          <div
            v-for="(project, index) in filteredProjects"
            :key="index"
            class="col-12 col-md-4"
          >
            <div class="project-item" :class="{ featured: project.featured }">
              <img :src="project.image" :alt="project.name || 'Project'" />
              <div v-if="project.featured" class="project-overlay">
                <span class="project-tag">coded, designed</span>
                <h3 class="project-name">{{ project.name }}</h3>
                <p class="project-desc">{{ project.description }}</p>
                <div class="project-links">
                  <a href="#" class="project-link">DEMO</a>
                  <a href="#" class="project-link">MORE</a>
                </div>
              </div>
            </div>
          </div>
        </div>

        <p class="portfolio-footer-text">And many more to come!</p>
      </div>
    </section>
    <!-- Footer -->
    <footer class="footer-section">
      <a href="#hero" class="back-to-top"> ↑ BACK TO TOP </a>
      <div class="footer-social">
        <a href="mailto:edcagatan00@gmail.com" aria-label="Email">@</a>
        <a href="#" aria-label="GitHub">GH</a>
        <a href="#" aria-label="LinkedIn">in</a>
        <a href="#" aria-label="Twitter">X</a>
      </div>
      <p class="footer-copy">@2026 Ed Rascoe Cagatan All Rights Reserved.</p>
    </footer>
  </div>
</template>

<script>
export default {
  name: "HomeView",
  data() {
    return {
      scrolled: false,
      activeFilter: "ALL",
      activeFilterIndex: 0,
      form: {
        name: "",
        email: "",
        phone: "",
        message: "",
      },
      filterTabs: ["ALL", "CODED", "DESIGNED"],
      usingNow: [
        {
          name: "HTML5",
          icon: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg",
        },
        {
          name: "CSS3",
          icon: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg",
        },
        {
          name: "SASS",
          icon: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/sass/sass-original.svg",
        },
        {
          name: "JAVASCRIPT",
          icon: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg",
        },
        {
          name: "REACT",
          icon: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg",
        },
        {
          name: "BOOTSTRAP",
          icon: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/bootstrap/bootstrap-original.svg",
        },
        {
          name: "GIT",
          icon: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg",
        },
        {
          name: "FIGMA",
          icon: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/figma/figma-original.svg",
        },
      ],
      learning: [
        {
          name: "NODEJS",
          icon: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nodejs/nodejs-original.svg",
        },
        {
          name: "MySQL",
          icon: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original.svg",
        },
        {
          name: "MONGODB",
          icon: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mongodb/mongodb-original.svg",
        },
        {
          name: "TYPESCRIPT",
          icon: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/typescript/typescript-original.svg",
        },
      ],
      projects: [
        { image: "/assets/project-1.jpg", type: "DESIGNED" },
        {
          image: "/assets/project-3.jpg",
          type: "CODED",
          featured: true,
          name: "eatsome.",
          description: "Restaurant browsing in React.js (Using Yelp API)",
        },
        { image: "/assets/project-2.jpg", type: "DESIGNED" },
        { image: "/assets/project-1.jpg", type: "CODED" },
        { image: "/assets/project-2.jpg", type: "DESIGNED" },
        { image: "/assets/project-1.jpg", type: "CODED" },
      ],
    };
  },
  computed: {
    filteredProjects() {
      if (this.activeFilter === "ALL") return this.projects;
      return this.projects.filter((p) => p.type === this.activeFilter);
    },
    filterUnderlineStyle() {
      const tabWidth = 149;
      const startOffset = (587 - tabWidth * 3) / 2;
      return {
        width: `${tabWidth}px`,
        left: `calc(50% - 293px + ${
          startOffset + this.activeFilterIndex * tabWidth
        }px)`,
      };
    },
  },
  mounted() {
    window.addEventListener("scroll", this.handleScroll);
    this.setupSmoothScroll();
  },
  beforeUnmount() {
    window.removeEventListener("scroll", this.handleScroll);
  },
  methods: {
    handleScroll() {
      this.scrolled = window.scrollY > 400;
    },
    setFilter(tab, index) {
      this.activeFilter = tab;
      this.activeFilterIndex = index;
    },
    handleSubmit() {
      alert("Thank you for your message! I will get back to you soon.");
      this.form = { name: "", email: "", phone: "", message: "" };
    },
    setupSmoothScroll() {
      document.querySelectorAll('a[href^="#"]').forEach((anchor) => {
        anchor.addEventListener("click", (e) => {
          const href = anchor.getAttribute("href");
          if (href === "#") return;
          e.preventDefault();
          const target = document.querySelector(href);
          if (target) {
            target.scrollIntoView({ behavior: "smooth" });
          }
        });
      });
    },
  },
};
</script>

<style scoped>
.service-icon-placeholder {
  font-size: 2.5rem;
  opacity: 0.15;
  line-height: 1;
}
</style>
