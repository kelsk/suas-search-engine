<template>
  <div class="about">
    <p>
    The Shut Up & Sew search engine was created to quickly and easily search the websites of all the vendors from @pinkmimosabyjacinta's vendor list. These vendors have been vetted by Jacinta or by trusted followers as stores owned and operated by BIPOC and allies. 
    </p>
    <p>
      Note that Google returns targeted ads at the top of the search results. <em>Ignore the links labelled</em> <span class="ad-sample">Ad</span>.
    </p>
    <p>
    This site is maintained by kelsk. Please submit any bugs or feature requests through <a v-bind:href="urls.github" alt="github codebase">Github</a>. Feel free to contribute!
    </p>
  </div>
</template>

<script>
export default {
  name: 'About',
  data: ()=>{
    return {
      urls: {
        github: "https://github.com/kelsk/suas-search-engine"
      }
    }
  }
}
</script>