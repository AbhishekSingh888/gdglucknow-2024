<template>
  <div class="team-member text-center">
    <div class="profile-pic-wrapper">
      <img :src="image" :alt="name" class="profile-pic" />
    </div>
    <h3 class="name">{{ name }}</h3>
    <p class="role">{{ role }}</p>
  </div>
</template>

<script>
export default {
  props: {
    name: String,
    role: String,
    image: String
  }
};
</script>

<style scoped>
.team-member {
  width: 150px;
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 0 auto;
}
.profile-pic-wrapper {
  width: 120px;
  height: 120px;
  border-radius: 50%;
  overflow: hidden;
  border: 4px solid #000; /* Black border for image circle */
}
.profile-pic {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
.name {
  margin-top: 8px;
  font-weight: bold;
}
.role {
  color: #666;
}
</style>
