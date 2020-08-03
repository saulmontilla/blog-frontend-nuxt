<template>
  <b-container fluid>
    <b-row class="header-nav mb-5">
      <b-col class="p-0">
        <strong>
          <slot></slot>
        </strong>
      </b-col>
    </b-row>
  </b-container>
</template>

<style scoped>
.header-nav {
  padding-bottom: 1rem;
  border-bottom: 3px solid var(--orange);
}
</style>