<template>
  <section class="organizing-team">
    <h2 class="title">Organizing Team</h2>
    <p class="description">
      Our mission is to equip our community members with practical skills, enabling them to communicate their insights and drive innovative solutions effectively.
    </p>
    <div class="team-members-grid">
      <TeamMember
        v-for="(member, index) in teamMembers"
        :key="index"
        :name="member.name"
        :role="member.role"
        :image="member.image"
      />
    </div>
  </section>
</template>

<script>
import TeamMember from '../components/team/temmember.vue';

export default {
  components: { TeamMember },
};
</script>

<style scoped>
.organizing-team {
  text-align: center;
  padding: 20px;
}
.title {
  font-size: 1.5em;
  font-weight: bold;
}
.description {
  margin-top: 8px;
  font-size: 1em;
  color: #555;
}
.team-members-grid {
  display: flex;
  justify-content: center;
  gap: 20px;
  flex-wrap: wrap;
  margin-top: 20px;
}
</style>
