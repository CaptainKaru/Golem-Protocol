<template>
  <section class="about-us">
    <div class="container">
      <h1>About Us</h1>
      <p class="intro">
        Welcome to our platform. We are dedicated to providing innovative solutions
        and exceptional service to our users.
      </p>
      
      <div class="mission">
        <h2>Our Mission</h2>
        <p>
          To empower users with cutting-edge technology and deliver value through
          continuous innovation and customer-focused development.
        </p>
      </div>

      <div class="values">
        <h2>Our Values</h2>
        <ul>
          <li>Innovation - Pushing boundaries and exploring new possibilities</li>
          <li>Integrity - Operating with honesty and transparency</li>
          <li>Excellence - Striving for the highest quality in everything we do</li>
          <li>Community - Building strong relationships with our users</li>
        </ul>
      </div>

      <div class="team">
        <h2>Our Team</h2>
        <div class="team-members">
          <div class="member">
            <h3><a href="/team/person-1">John Smith</a></h3>
            <p class="role">Project Manager</p>
          </div>
          <div class="member">
            <h3><a href="/team/person-2">Sarah Johnson</a></h3>
            <p class="role">Database Designer</p>
          </div>
          <div class="member">
            <h3><a href="/team/person-3">Michael Chen</a></h3>
            <p class="role">Web Designer</p>
          </div>
          <div class="member">
            <h3><a href="/team/person-4">Emma Davis</a></h3>
            <p class="role">Frontend Developer</p>
          </div>
          <div class="member">
            <h3><a href="/team/person-5">Alex Rodriguez</a></h3>
            <p class="role">DevOps Engineer</p>
          </div>
          <div class="member">
            <h3><a href="/team/person-6">Lisa Anderson</a></h3>
            <p class="role">Backend Developer</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
// About Us component
</script>

<style scoped>
.about-us {
  padding: 2rem;
  background-color: #f9f9f9;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
}

h1 {
  font-size: 2.5rem;
  color: #333;
  margin-bottom: 1.5rem;
}

h2 {
  font-size: 1.8rem;
  color: #444;
  margin-top: 2rem;
  margin-bottom: 1rem;
}

.intro {
  font-size: 1.1rem;
  color: #666;
  line-height: 1.6;
  margin-bottom: 2rem;
}

.team {
  margin-bottom: 2rem;
}

.team-members {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 2rem;
  margin-top: 1.5rem;
}

.member {
  padding: 1.5rem;
  background-color: #fff;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  text-align: center;
}

.member h3 {
  margin: 0 0 0.5rem 0;
  font-size: 1.3rem;
}

.member a {
  color: #1976d2;
  text-decoration: none;
  font-weight: 500;
  transition: color 0.3s ease;
}

.member a:hover {
  color: #1565c0;
  text-decoration: underline;
}

.role {
  color: #666;
  font-size: 0.95rem;
  margin: 0.5rem 0 0 0;
}
  list-style-type: none;
  padding-left: 0;
}

.values li {
  padding: 0.5rem 0;
  color: #555;
  line-height: 1.6;
}

.values li::before {
  content: "✓ ";
  color: #4caf50;
  font-weight: bold;
  margin-right: 0.5rem;
}

p {
  color: #666;
  line-height: 1.8;
}
</style>
