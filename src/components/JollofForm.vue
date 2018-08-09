<template>
  <div>
    <h2>What jollofin at? Pick the best Jollof in the land.</h2>
    <form method="post" netlify-honeypot="bot-field" netlify>
      <input type="hidden" name="form-name" value="jollof-wars" />
      <ul>
        <li v-for="jollof in jollofTypes">
          <label>
            <input 
              type="radio"
              name="jollofTypes"
              :checked="jollof === defaultJollof"
            >
            <span>{{ jollof }}</span>
          </label>
        </li>
      </ul>
      <button type="submit">Select your fighter</button>
    </form>
  </div>
</template>

<script>
  export default {
    name: 'JollofForm',
    data () {
      return {
        jollofTypes: ['Ghanaian Jollof', 'Nigerian Jollof', 'Senegal Jollof'],
        defaultJollof: 'Senegal Jollof'
      }
    }
  }
</script>

<style scoped>
li {
  list-style: none;
}
span {
  font-size: 1.35em;
  font-weight: 300;
}
</style>