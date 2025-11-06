<!-- ============================================ -->
<!-- COMPONENT 5: LocationSection.vue -->
<!-- ============================================ -->

<script setup></script>

<template>
  <section class="location-section">
    <div class="container">
      <h2>Visit Us</h2>
      <div class="location-content">
        <div class="location-info">
          <div class="info-block">
            <h3>📍 Location</h3>
            <p>123 Sweet Street<br />City, XX 12345</p>
          </div>

          <div class="info-block">
            <h3>🕐 Hours</h3>
            <p>
              <strong>Monday - Thursday:</strong> 11am - 9pm<br />
              <strong>Friday - Saturday:</strong> 11am - 11pm<br />
              <strong>Sunday:</strong> 12pm - 8pm
            </p>
          </div>

          <div class="info-block">
            <h3>📞 Contact</h3>
            <p>
              Phone: (000) 000-0123<br />
              Email: hello@coolvue.com
            </p>
          </div>
        </div>

        <div class="map-placeholder">
          <div class="map-content">
            <svg viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg">
              <circle cx="100" cy="100" r="80" fill="#6ec1e4" opacity="0.2" />
              <circle cx="100" cy="100" r="60" fill="#6ec1e4" opacity="0.3" />
              <circle cx="100" cy="100" r="40" fill="#6ec1e4" opacity="0.4" />
              <path d="M 100 60 Q 80 80 100 120 Q 120 80 100 60" fill="#FF6B9D" />
              <circle cx="100" cy="75" r="15" fill="white" opacity="0.9" />
              <text
                x="100"
                y="82"
                text-anchor="middle"
                font-size="20"
                fill="#FF6B9D"
                font-weight="bold"
              >
                📍
              </text>
            </svg>
            <p>Map Location</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.location-section {
  padding: 5rem 2rem;
  background: white;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
}

.location-section h2 {
  font-size: 3rem;
  color: #2c3e50;
  text-align: center;
  margin-bottom: 3rem;
  font-weight: 700;
}

.location-content {
  display: flex;
  gap: 4rem;
  align-items: flex-start;
}

.location-info {
  flex: 1;
  display: flex;
  flex-direction: column;
  gap: 2.5rem;
}

.info-block h3 {
  font-size: 1.5rem;
  color: #2c3e50;
  margin-bottom: 1rem;
  font-weight: 600;
}

.info-block p {
  font-size: 1.1rem;
  color: #546e7a;
  line-height: 1.8;
}

.info-block strong {
  color: #2c3e50;
}

.map-placeholder {
  flex: 1;
  background: linear-gradient(135deg, #e0f7fa 0%, #fff5f7 100%);
  border-radius: 20px;
  min-height: 400px;
  display: flex;
  align-items: center;
  justify-content: center;
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
}

.map-content {
  text-align: center;
}

.map-content svg {
  width: 200px;
  height: 200px;
  margin-bottom: 1rem;
}

.map-content p {
  font-size: 1.2rem;
  color: #546e7a;
  font-weight: 600;
}

@media (max-width: 768px) {
  .location-section {
    padding: 3rem 1.5rem;
  }

  .location-section h2 {
    font-size: 2.2rem;
  }

  .location-content {
    flex-direction: column;
    gap: 2rem;
  }

  .map-placeholder {
    min-height: 300px;
  }

  .map-content svg {
    width: 150px;
    height: 150px;
  }
}
</style>
