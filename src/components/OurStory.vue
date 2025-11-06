<!-- ============================================ -->
<!-- COMPONENT 2: OurStory.vue -->
<!-- ============================================ -->

<script setup></script>

<template>
  <section class="our-story">
    <div class="container">
      <div class="story-image">
        <div class="image-placeholder">
          <svg viewBox="0 0 300 300" xmlns="http://www.w3.org/2000/svg">
            <defs>
              <linearGradient id="ice1" x1="0%" y1="0%" x2="0%" y2="100%">
                <stop offset="0%" style="stop-color: #ffb7c5; stop-opacity: 1" />
                <stop offset="100%" style="stop-color: #ff8fa3; stop-opacity: 1" />
              </linearGradient>
              <linearGradient id="ice2" x1="0%" y1="0%" x2="0%" y2="100%">
                <stop offset="0%" style="stop-color: #b4f8c8; stop-opacity: 1" />
                <stop offset="100%" style="stop-color: #a0e7b8; stop-opacity: 1" />
              </linearGradient>
            </defs>

            <circle cx="100" cy="100" r="60" fill="url(#ice1)" />
            <circle cx="200" cy="100" r="60" fill="url(#ice2)" />

            <path d="M 60 140 L 100 240 L 140 140 Z" fill="#E8A87C" />
            <path d="M 160 140 L 200 240 L 240 140 Z" fill="#E8A87C" />

            <line x1="75" y1="155" x2="85" y2="190" stroke="#D4956A" stroke-width="3" />
            <line x1="100" y1="155" x2="100" y2="215" stroke="#D4956A" stroke-width="3" />
            <line x1="125" y1="155" x2="115" y2="190" stroke="#D4956A" stroke-width="3" />

            <line x1="175" y1="155" x2="185" y2="190" stroke="#D4956A" stroke-width="3" />
            <line x1="200" y1="155" x2="200" y2="215" stroke="#D4956A" stroke-width="3" />
            <line x1="225" y1="155" x2="215" y2="190" stroke="#D4956A" stroke-width="3" />

            <circle cx="85" cy="90" r="4" fill="white" opacity="0.6" />
            <circle cx="115" cy="95" r="4" fill="white" opacity="0.6" />
            <circle cx="185" cy="95" r="4" fill="white" opacity="0.6" />
            <circle cx="215" cy="90" r="4" fill="white" opacity="0.6" />
          </svg>
        </div>
      </div>
      <div class="story-content">
        <h2>Sweet Beginnings</h2>
        <p>
          CoolVue was born from a simple dream: to bring joy to our community through exceptional
          frozen treats. What started as a small shop with just three flavors has grown into a
          beloved local destination.
        </p>

        <p>
          Today, we're proud to serve over 20 unique flavors of ice cream and a rotating selection
          of seasonal ice pops, all made in-house with locally sourced ingredients whenever
          possible.
        </p>

        <div class="stats">
          <div class="stat">
            <span class="stat-number">20+</span>
            <span class="stat-label">Flavors</span>
          </div>
          <div class="stat">
            <span class="stat-number">5000+</span>
            <span class="stat-label">Happy Customers</span>
          </div>
          <div class="stat">
            <span class="stat-number">100%</span>
            <span class="stat-label">Handcrafted</span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.our-story {
  padding: 5rem 2rem;
  background: white;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  align-items: center;
  gap: 4rem;
}

.story-image {
  flex: 1;
}

.image-placeholder {
  width: 100%;
  max-width: 400px;
  aspect-ratio: 1;
  background: linear-gradient(135deg, #fff5f7 0%, #e0f7fa 100%);
  border-radius: 20px;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 2rem;
  box-shadow: 0 8px 25px rgba(0, 0, 0, 0.1);
}

.image-placeholder svg {
  width: 100%;
  height: 100%;
}

.story-content {
  flex: 1;
}

.story-content h2 {
  font-size: 3rem;
  color: #2c3e50;
  margin-bottom: 1.5rem;
  font-weight: 700;
}

.story-content p {
  font-size: 1.15rem;
  color: #546e7a;
  line-height: 1.8;
  margin-bottom: 1.5rem;
}

.stats {
  display: flex;
  gap: 3rem;
  margin-top: 3rem;
  padding-top: 2rem;
  border-top: 2px solid #f0f0f0;
}

.stat {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.stat-number {
  font-size: 2.5rem;
  font-weight: 700;
  color: #6ec1e4;
  margin-bottom: 0.5rem;
}

.stat-label {
  font-size: 1rem;
  color: #546e7a;
  font-weight: 500;
}

@media (max-width: 768px) {
  .our-story {
    padding: 3rem 1.5rem;
  }

  .container {
    flex-direction: column;
    gap: 2rem;
  }

  .story-content h2 {
    font-size: 2.2rem;
  }

  .story-content p {
    font-size: 1.05rem;
  }

  .stats {
    gap: 1.5rem;
  }

  .stat-number {
    font-size: 2rem;
  }
}
</style>
