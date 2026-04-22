<template>
  <div class="profile-container">

    <!-- Header: Photo + Name + Email -->
    <div class="profile-header">
      <img src="/anocerale.PNG" alt="Profile Photo" class="profile-photo" />
      <div class="profile-info">
        <h1>Nocerale Angel Merino</h1>
        <p class="email">22-1-01120@vsu.edu.ph</p>
      </div>
    </div>

    <!-- Bio -->
    <div class="section">
      <p class="bio">I’m motivated by the challenge of learning complex concepts and continuously expanding my knowledge and skills.
</p>
    </div>

    <!-- Collaborative Project Experience -->
    <div class="section">
      <h2>Collaborative Project Experience</h2>

      <div class="entry">
        <p><strong>Frontend Developer</strong> | <span class="date">April 2026</span></p>
        <p class="description">Developed one of the components of a user interface for an agriculture tracker hub.</p>
      </div>
      <div class="entry">
        <p><strong>Web Designer</strong> | <span class="date">April 2026</span></p>
        <p class="description">Currently contributing to the web design for project Golem-Protocol.</p>
      </div>

      <!-- Add more work experience entries by copying the div.entry block above -->

    </div>

    <!-- Educational Background -->
    <div class="section">
      <h2>Educational Background</h2>

      <div class="entry">
        <p><strong>Visayas State University</strong></p>
        <p>Bachelor of Science in Computer Science</p>
        <p class="date">Undergraduate</p>
      </div>

      <!-- Add more education entries by copying the div.entry block above -->

    </div>

    <!-- Projects -->
    <div class="section">
      <h2>Projects</h2>

      <div class="entry">
        <p><strong>Red Lead</strong> | <span class="date">February 2026 – On Going</span></p>
        <p class="description">A fun and interactive educational web platform for learning basic/highschool math.</p>
      </div>

      <!-- Add more project entries by copying the div.entry block above -->

    </div>


    <!-- Skills -->
    <div class="section">
      <h2>Skills</h2>
      <ul class="skills-list">
        <li>C</li>
        <li>C++</li>
        <li>Java</li>
        <li>MySQL</li>
        <li>JavaScript</li>
        <li>React</li>
        <li>Git/Github</li>
        <!-- Add more skills as needed -->
      </ul>
    </div>

  </div>
</template>

<script>
export default {
  name: 'NoceraleAngelPage', // Change this to your name e.g. 'JuanDelaCruzPage'
  head() {
    return {
      title: 'Nocerale Angel Merino', // Change to your full name
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'The personal page of Nocerale Angel Merino.' // Change to your full name
        }
      ]
    }
  }
}
</script>

<style scoped>
.profile-container {
  max-width: 800px;
  margin: 40px auto;
  padding: 24px;
  font-family: Arial, sans-serif;
  color: #222;
}

.profile-header {
  display: flex;
  align-items: center;
  gap: 20px;
  margin-bottom: 24px;
}

.profile-photo {
  width: 90px;
  height: 90px;
  border-radius: 50%;
  object-fit: cover;
  border: 2px solid #ccc;
}

.profile-info h1 {
  margin: 0;
  font-size: 1.5rem;
}

.email {
  color: #555;
  margin: 4px 0 0;
}

.bio {
  font-style: italic;
  color: #444;
}

.section {
  margin-bottom: 28px;
}

.section h2 {
  font-size: 1.1rem;
  border-bottom: 1px solid #ddd;
  padding-bottom: 4px;
  margin-bottom: 12px;
}

.entry {
  margin-bottom: 14px;
}

.entry p {
  margin: 2px 0;
}

.date {
  color: #888;
  font-size: 0.9rem;
}

.description {
  color: #555;
  font-style: italic;
}

.skills-list {
  list-style: disc;
  padding-left: 20px;
  line-height: 1.8;
}
</style>