<template>
  <div class="match-widget">
    <div class="league-name">{{ league }}</div>
    <div class="teams">
      <div class="team">
        <span class="name">{{ homeTeam }}</span>
        <span class="score">{{ homeScore }}</span>
      </div>
      <div class="divider">-</div>
      <div class="team">
        <span class="score">{{ awayScore }}</span>
        <span class="name">{{ awayTeam }}</span>
      </div>
    </div>
    <div class="status">{{ status }}</div>
  </div>
</template>

<script setup>
defineProps({
  league: { type: String, default: 'Premier League' },
  homeTeam: { type: String, default: 'Arsenal' },
  awayTeam: { type: String, default: 'Chelsea' },
  homeScore: { type: Number, default: 2 },
  awayScore: { type: Number, default: 1 },
  status: { type: String, default: 'Live - 75\'' }
})
</script>

<style scoped>
/* Add your own styling or Tailwind classes here */
.match-widget {
  background: #1a1a1a;
  color: #fff;
  padding: 1rem;
  border-radius: 8px;
  text-align: center;
  font-family: sans-serif;
}
.teams { display: flex; justify-content: center; gap: 1rem; margin: 10px 0; font-weight: bold; }
.status { color: #ff4757; font-size: 0.9rem; animation: blink 2s infinite; }
@keyframes blink { 50% { opacity: 0.5; } }
</style>
