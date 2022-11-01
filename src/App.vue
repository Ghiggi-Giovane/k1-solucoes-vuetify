<template>
<div id="App">
  <MainNavbar />
	<Home />
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
