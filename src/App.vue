<template>
<div id="App">
  <MainNavbar />
			<router-view />

</div>
</template>

<script>
import MainNavbar from './components/MainNavbar';

export default {
  name: 'App',
	components: {
		MainNavbar,
	}
};
</script>
