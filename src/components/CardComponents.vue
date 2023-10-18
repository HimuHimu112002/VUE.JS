<script>
export default {
  props: {
    title: String,
    discription: String,
  },
};
</script>

<template>
    <div class="container">
      <div class="row gx-5">

        <div class="col-6 mb-4 mt-4">
          <div class="card">
            <img src="../assets/dark2.jpg" class="card-img-top" alt="...">
            <div class="card-body">
              <h5 class="card-title">{{ title }}</h5>
              <p class="card-text">{{ discription }}</p>
              <router-link to="/">
                <a href="#" class="btn btn-primary">Go Home</a>
              </router-link>
            </div>
          </div>
        </div>

        <div class="col-6 mt-4">
          <div class="card">
            <img src="../assets/dark3.jpg" class="card-img-top" alt="...">
            <div class="card-body">
              <h5 class="card-title">{{ title }}</h5>
              <p class="card-text">{{ discription }}</p>
              <router-link to="/">
                <a href="#" class="btn btn-primary">Go Home</a>
              </router-link>
            </div>
          </div>
        </div>

      </div>
    </div>
</template>