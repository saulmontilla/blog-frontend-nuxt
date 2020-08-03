<template>    
  <div>
    <main-header>
      Home
    </main-header>
    
    <b-row>
      <b-col>
        <h1>
          Título 1
        </h1>

        <p>
          Lorem ipsum dolor sit, amet consectetur adipisicing elit. Error, non neque rem quo ipsam unde? Accusantium, vitae. Dolorem autem quaerat asperiores sunt voluptas velit? Blanditiis aut quidem hic repudiandae iure?
        </p>

        <b-button variant="outline-danger">
          Learn more
        </b-button>
      </b-col>

      <b-col>
        <b-img fluid src="/pic01.jpg"/>
      </b-col>
    </b-row>

    <hr>

    <b-row>
      <b-col cols="6">
        <b-card
          title="Card Title"
          img-src="https://picsum.photos/600/300/?image=25"
          img-alt="Image"
          img-top
          tag="article"
          class="mb-2"
        >
          <b-card-text>
            Some quick example text to build on the card title and make up the bulk of the card's content.
          </b-card-text>

          <b-button href="#" variant="primary">Go somewhere</b-button>
        </b-card>
      </b-col>

      <b-col cols="6">
        <b-card
          title="Card Title"
          img-src="https://picsum.photos/600/300/?image=25"
          img-alt="Image"
          img-top
          tag="article"
          class="mb-2"
        >
          <b-card-text>
            Some quick example text to build on the card title and make up the bulk of the card's content.
          </b-card-text>

          <b-button href="#" variant="primary">Go somewhere</b-button>
        </b-card>
      </b-col>
    </b-row>
  </div>
</template>

<script>
import MainHeader from '../components/MainHeader'

export default {
  components: {
    MainHeader
  }
}
</script>

<style>
  
</style>