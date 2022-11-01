<template>
  <v-app>
		<v-navigation-drawer
		v-model="drawer"
      app
			dark
      temporary
			>
      <v-list-item>
        <v-list-item-content>
					<v-avatar class="mb-3 mt-3" size="80"><img :src="navlogo"/></v-avatar>
					<h4 class="H4" id="sidebar-no-header-title">Menu Soluções</h4>
        </v-list-item-content>
      </v-list-item>

      <v-divider style="border: 1px solid #fff"></v-divider>

      <v-list
        dense
        nav

      >
        <v-list-item
          v-for="item in items"
          :key="item.title"
          link
        >
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar app
		color="rgb(140, 32, 30)"
		>
      <v-app-bar-nav-icon @click="drawer = !drawer" ></v-app-bar-nav-icon>

			<img class="mx-3" href="#" src="../assets/K1_Logo_BRANCO.png" style="width: 30px;" />

				<v-btn
					fab
					dark
					small
					color="rgb(140, 32, 30)"
					elevation
				>
      <v-icon dark>
        mdi-home
      </v-icon>
    </v-btn>

    </v-app-bar>

    <v-main>
      <!--  -->
    </v-main>
  </v-app>
</template>


<script>
  export default {
		name: 'MainNavbarComponent',
    data: () => ({
			drawer: false,
			navlogo: require("../assets/K1_Logo_BRANCO_sm.png"),
			items: [
				{ title: 'Home', icon: 'mdi-home' },
				{ title: 'Clientes', icon: 'mdi-account-multiple'},
				{ title: 'Transportadoras', icon: 'mdi-truck'},
				{ title: 'Colaboradores', icon: 'mdi-account'},
			],
			}
		),
  }
</script>

<style scoped>
	.H4 {
		text-align: center;
	}
</style>

