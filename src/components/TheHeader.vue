<script setup>
import { RouterLink } from 'vue-router'
</script>

<template>
  <header>
    <div class="header-container">
      <div class="logo-section">
        <div class="logo">
          <svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
            <!-- Ice cream scoop -->
            <circle cx="50" cy="35" r="25" fill="#FFB7C5" />
            <circle cx="50" cy="30" r="20" fill="#FFC8DD" />
            <!-- Cone -->
            <path d="M 35 45 L 50 85 L 65 45 Z" fill="#E8A87C" />
            <!-- Cone pattern -->
            <line x1="40" y1="50" x2="45" y2="65" stroke="#D4956A" stroke-width="2" />
            <line x1="50" y1="50" x2="50" y2="75" stroke="#D4956A" stroke-width="2" />
            <line x1="60" y1="50" x2="55" y2="65" stroke="#D4956A" stroke-width="2" />
            <line x1="42" y1="55" x2="58" y2="55" stroke="#D4956A" stroke-width="1.5" />
            <line x1="44" y1="63" x2="56" y2="63" stroke="#D4956A" stroke-width="1.5" />
            <line x1="46" y1="71" x2="54" y2="71" stroke="#D4956A" stroke-width="1.5" />
          </svg>
        </div>
        <h1>CoolVue</h1>
      </div>

      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/menu">Menu</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </nav>
    </div>
  </header>
</template>

<style scoped>
header {
  margin: 0;
  padding: 0;
  background: linear-gradient(135deg, #6ec1e4 0%, #89d4f5 100%);
  width: 100vw;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

.header-container {
  max-width: 1200px;
  margin: 0 auto;
  min-height: 7rem;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 0 2rem;
}

.logo-section {
  display: flex;
  align-items: center;
  gap: 1rem;
}

.logo {
  width: 5rem;
  height: 5rem;
  background-color: #ffffff;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 0.5rem;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.15);
  transition: transform 0.3s ease;
}

.logo:hover {
  transform: rotate(10deg) scale(1.05);
}

.logo svg {
  width: 100%;
  height: 100%;
}

h1 {
  font-weight: 600;
  font-size: 2.6rem;
  color: white;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.1);
  margin: 0;
}

nav {
  display: flex;
  gap: 2rem;
}

nav a {
  color: white;
  text-decoration: none;
  font-size: 1.1rem;
  font-weight: 500;
  padding: 0.5rem 1rem;
  border-radius: 20px;
  transition: all 0.3s ease;
  position: relative;
}

nav a:hover {
  background-color: rgba(255, 255, 255, 0.2);
  transform: translateY(-2px);
}

nav a.router-link-active {
  background-color: rgba(255, 255, 255, 0.3);
  font-weight: 600;
}

/* Mobile responsiveness */
@media (max-width: 768px) {
  .header-container {
    flex-direction: column;
    gap: 1rem;
    padding: 1.5rem 1rem;
  }

  nav {
    gap: 1rem;
  }

  nav a {
    font-size: 1rem;
    padding: 0.4rem 0.8rem;
  }

  h1 {
    font-size: 2rem;
  }

  .logo {
    width: 4rem;
    height: 4rem;
  }
}
</style>
