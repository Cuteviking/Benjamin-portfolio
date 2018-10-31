<template>
  <section class="container h-100 position-relative">
    <div class="row h-100 z-index-10">
      <div class="col-8 offset-2 my-auto">
        <div class="content-wrapper align-self-center">
          <h1 class="mb-5">Art director <br/> UX + UI designer</h1>
          <div class="content">
            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
            tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
            quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
            consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse
            cillum dolore eu fugiat nulla pariatur.</p>
              
          </div>
          <nav>
            <ul class="list-inline">
              <li class="list-inline-item">
                <nuxt-link to="/work">My Work</nuxt-link>
              </li>
              <li class="list-inline-item">
                <nuxt-link to="/contact">Contact me</nuxt-link>
              </li>
            </ul>
          </nav>
        </div>   
      </div>
      <div class="background">
          <div class="huge-wrapper">
            &
          </div>
      </div> 
    </div>
  </section>
</template>
<style lang="scss">
  .background {
    position:absolute;
    color: rgba(243,37,80,1);
    top: 40%;
    right: 12%;
    transform: translateY(-50%);
    z-index: -1;

    .huge-wrapper {
      font-weight: 700;
      font-size: 42em;
      
    }
  }

  .z-index-10 {
    z-index: 10;
  }

  .content {
    max-width: 500px;
  }

  .list-inline {
    .list-inline-item:not(:last-child) {
      margin-right: 2.5rem;
    }
  }

</style>

<script>

export default {
  components: {
    
  }
}
</script>

