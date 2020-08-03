<template>
  <div class="sidenav" v-bind:class="{hidden : hidden}">
    <section class="search">
        <input type="text" class="form-control" placeholder="search">
    </section>

    <nav class="menu">
      <header>
        <h2 class="title">
            Laravel Sanctum
        </h2>
      </header>

      <ul>
          <li>
              <a href="#">
                  Home
              </a>
          </li>
          <li>
              <a href="#">
                  Categoria 1
              </a>
          </li>
          <li>
              <a href="#">
                  Categoria 2
              </a>
          </li>
          <li>
              <a href="#">
                  Categoria 3
              </a>
          </li>
          <li>
              <a href="#">
                  Categoria 4
              </a>
          </li>
      </ul>
    </nav>

    <div class="footer">
        <nuxt-link to="/register">
            Register
        </nuxt-link>
        <nuxt-link to="/login">
            Login
        </nuxt-link>
    </div>

     <a href="#" class="toggler" @click.prevent="toggleSideNav()">
         <b-icon-list class="toggler-icon" />
     </a>
  </div>
</template>

<script>
import { BIcon, BIconList } from 'bootstrap-vue'

export default {
    components: {
        BIcon,
        BIconList
    },
    data () {
        return {
            hidden: false
        }
    },
    methods: {
        toggleSideNav () {
            this.hidden = !this.hidden
        }
    }
}
</script>

<style scoped>
.sidenav {
  width: 272px;
  height: 100vh;
  display: flex;
  flex-direction: column;
  background: #f5f6f7;
  position: sticky;
  top: 0;
  z-index: 1;
  transition: all 0.3s linear;
  white-space: nowrap;
}

.sidenav .search {
    padding: 1rem;
    background: #eff1f2;
}
.sidenav .title {
  border-bottom: 3px solid var(--orange);
  font-size: 1.38889em;
  display: inline-block;
  line-height: 3rem;
  margin-bottom: 2rem;
}

.sidenav .menu {
    padding-left: 1.5rem;
    padding-right: 1.5rem;
    flex-grow: 1;
}
.sidenav .menu ul {
    display: flex;
    flex-direction: column;
    list-style: none;
    margin: 0;
    padding: 0;
}

.sidenav .menu li {
    text-transform: uppercase;
}

.sidenav .menu a {
    text-decoration: none;
    color: #3d4449;
    display: block;
    padding: 0.625rem 0;
    line-height: 2rem;
    border-bottom: 2px solid #dadfe1;
}

.sidenav .menu a:hover {
    color: var(--orange);
    border-color: var(--orange);
}

.sidenav .toggler {
    position: absolute;
    top: 1rem;
    left:  calc(272px + 1rem);
    z-index: 1;
}

.sidenav .toggler-icon {
    width: 2rem;
    height: 2rem;
    color: var(--orange);
}

.sidenav.hidden {
    margin-left: -272px;
}

.sidenav .footer {
    display: flex;
    justify-content: space-around;
    background: var(--orange);
}

.sidenav .footer a {
    text-decoration: none;
    color: #fff;
    padding: 0.6rem;
    flex-grow: 1;
    text-align: center;
}

.sidenav .footer a:hover {
    background: var(--dark-orange);
}

</style>