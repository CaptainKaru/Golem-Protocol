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
            <h3><a href="/caranez">Carlroy F. Arañez</a></h3>
            <p class="role">Project Manager</p>
          </div>
          <div class="member">
            <h3><a href="/kdelima">Kyla Gayle B. Delima</a></h3>
            <p class="role">Database Designer</p>
          </div>
          <div class="member">
            <h3><a href="/anocerale">Angel M. Nocerale</a></h3>
            <p class="role">Web Designer</p>
          </div>
          <div class="member">
            <h3><a href="/acastro">Azriel Kaye C. Castro</a></h3>
            <p class="role">Frontend Developer</p>
          </div>
          <div class="member">
            <h3><a href="/emagadan">Evan Kasimir Y. Magadan</a></h3>
            <p class="role">DevOps Engineer</p>
          </div>
          <div class="member">
            <h3><a href="/jdstaagata">Jerome Daniel S. Sta. Agata</a></h3>
            <p class="role">Backend Developer</p>
          </div>
          <div class="member">
            <h3><a href="/team/person-7">Monarch Asis</a></h3>
            <p class="role">Quality Assurance (QA) Tester</p>
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
  background: linear-gradient(135deg, #f8fafc 0%, #f1f5f9 100%);
}

.container {
  max-width: 1200px;
  margin: 0 auto;
}

h1 {
  font-size: 2.5rem;
  color: #1e293b;
  margin-bottom: 1.5rem;
}

h2 {
  font-size: 1.8rem;
  color: #334155;
  margin-top: 2rem;
  margin-bottom: 1rem;
}

.intro {
  font-size: 1.1rem;
  color: #475569;
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
  background: linear-gradient(145deg, #ffffff 0%, #f8fafc 100%);
  border-radius: 12px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.05), 0 1px 3px rgba(0, 0, 0, 0.1);
  text-align: center;
  transition: transform 0.2s ease, box-shadow 0.2s ease;
  border: 1px solid rgba(148, 163, 184, 0.1);
}

.member:hover {
  transform: translateY(-2px);
  box-shadow: 0 8px 25px rgba(0, 0, 0, 0.1), 0 4px 10px rgba(0, 0, 0, 0.05);
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

.values ul {
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
