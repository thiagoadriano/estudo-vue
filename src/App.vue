<template>
  <header class="phone-viewport">
    <md-toolbar>
      <md-button class="md-icon button" @click.native="toggleLeftSidenav">
        <md-icon>menu</md-icon>
      </md-button>

      <h1 class="md-title">{{title}}</h1>
    </md-toolbar>
    <md-sidenav class="md-left" ref="leftSidenav">
      <md-toolbar class="md-medium">
        <div class="md-toolbar-container">
          <h2 class="md-title">Navegação</h2>
        </div>
      </md-toolbar>
      <md-list>
        <md-list-item>Perfil</md-list-item>
        <md-list-item>
          <router-link to="/categories">Categorias</router-link>
        </md-list-item>
        <md-list-item>Produtos</md-list-item>
        <md-list-item>Sair</md-list-item>
      </md-list> 
    </md-sidenav>
  </header>
  <md-row>
    <router-view></router-view>
  </md-row>
</template> 	

<script>

export default {
  name: 'EstudoVue',
  data () {
    return {
      title: 'Ecommerce Estudo'
    }
  },
  methods: {
    toggleLeftSidenav () {
      this.$refs.leftSidenav.toggle()
    }
  }
}
</script>

<style>
</style>
