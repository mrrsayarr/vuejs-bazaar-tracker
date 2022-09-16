
<template>
    <nav class="navbar navbar-light bg-light justify-content-between">
      <div class="in-navbar">
        <div class="start">
          <a class="navbar-brand">Bazaar Tracker | <small>Last update: -</small></a>
        </div>
        
        <div class="end">
          <b-button variant="success"  @click="refreshPage">Refresh</b-button>
        </div>
      </div>
        <!-- <form class="form-inline">
          <button class="getBtn btn btn-outline-success mr-2 my-2 my-sm-0" >GET</button>
        </form> -->
        <div>
        </div>
    </nav>
</template>

<script>
export default {
  name: 'NavbarPage',
  data:() => ({

  }),

  created() {
    // this.refreshPage()
  },

  methods: {
    refreshPage() {
      window.location.reload();
    }
  }
}
</script>

<style scoped>

.in-navbar  {
  width: 150vh;
  display: flex;
  justify-content: space-between;
}
.end {
  display: flex;
  justify-content: end;
}
</style>
