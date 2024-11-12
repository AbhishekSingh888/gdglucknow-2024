<template>
  <h1 class="pb-2 title">The Trailblazers Behind the Magic ✨</h1>
  <p class="mb-4 subtitle">Our goal is to empower our community by providing them with valuable skills that help them
    articulate their ideas and foster innovative solutions. No matter the challenge, these leaders at the forefront of
    change, creativity, and discovery have worked alongside you to find the answers.</p>
  <div class="team-section">
    <div v-for="member in teamData" :key="member.name" class="team-card">
      <div class="border-overlay">
        <div class="image-wrapper" :style="{ backgroundImage: `url(${member.image})` }">
          <div class="bottom-content">
            <div src="" alt="Small image" class="small-image"></div>
          </div>
        </div>
      </div>
      <div class="info">
        <h3>{{ member.name }}</h3>
        <p>{{ member.role }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "TeamSection",
  setup() {
    const { teamData } = useJSONData();
    return { teamData };
  },
};
</script>

<style scoped>
.title {
  padding: 16px 0;
  text-align: center;
}

.subtitle {
  padding: 8px 16px;
  text-align: center;
  font-size: 1em;
}

.team-section {
  display: flex;
  flex-wrap: wrap;
  gap: 5rem;
  padding: 16px;
  justify-content: center;
}

.team-card {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 230px;
}

.border-overlay {
  position: relative;
  width: 14rem;
  height: 14rem;
  border-radius: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
  border: 8px solid #fff;
  box-shadow: rgba(50, 50, 93, 0.25) 0px 30px 60px -12px, rgba(0, 0, 0, 0.3) 0px 18px 36px -18px;
}

.border-overlay:hover::before {
  animation: rotateBorder 2s linear infinite;
}

.image-wrapper {
  width: 100%;
  height: 100%;
  border-radius: 50%;
  overflow: hidden;
  position: relative;
  background-size: cover;
  background-position: center;
  transition: transform 0.3s ease;
}

.image-wrapper img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 0.3s ease;
}

.bottom-content {
  position: absolute;
  bottom: 0px;
  text-align: center;
  left: 50%;
  width: 100%;
  background-color: #fff;
  transform: translateX(-50%);
  display: flex;
  flex-direction: column;
  align-items: center;
  z-index: 1;
}

.small-image {
  width: 130px;
  height: 45px;
  margin-top: 10px;
  background-image: url('/assets/img/logowithtext.png')
}

.info {
  flex: 1;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 11px;
}

.info h3 {
  font-size: 1em;
  margin: 8px 0;
  color: #333;
}

.info p {
  font-size: 0.8em;
  color: #777;
}

@keyframes rotateBorder {
  0% {
    transform: rotate(0deg);
  }

  100% {
    transform: rotate(360deg);
  }
}

/* Responsive Design */
@media (max-width: 768px) {
  .team-section {
    gap: 2rem;
  }

  .team-card {
    width: 48%;
  }

  .title {
    padding: 24px 16px;
    font-size: 1.5em;
  }

  .subtitle {
    padding: 8px 16px;
    font-size: 0.9em;
  }
}

@media (max-width: 480px) {
  .team-card {
    width: 100%;
  }

  .title {
    padding: 20px 8px;
    font-size: 1.2em;
  }

  .subtitle {
    padding: 4px 8px;
    font-size: 0.8em;
  }
}
</style>
