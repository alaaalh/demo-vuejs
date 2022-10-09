<template>
  <li>
    <div>
      <header>
        <h3>{{ title }}</h3>
        <base-button mode="deleteButton">Delete</base-button>
      </header>
      <p>{{ description }}</p>
      <nav>
        <a :href="link">view resource</a>
      </nav>
      <p @click="changeName">{{name}}</p>
    </div>
  </li>
</template>

<script>
export default {
  props: ["title", "description", "link"],
  data (){
    return {
        name: 'Alaa'
    }
  },
  methods: {
    changeName(){
        this.name = 'ibrahim'
    }
  }

};
</script>
