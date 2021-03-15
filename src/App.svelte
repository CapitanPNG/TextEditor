<script>

import { link, Router, Route } from 'svelte-routing';

export let version;

</script>

<div class="page-root">
	<div class="page-header">
		<a use:link href="/Home">	
			SVELTE APP (v {version})
		</a>
	</div>
	<div class="page-content">
		<div class="page-content-center">
			<Router>
				<Route path="/">Default Page</Route>
				<Route path="/Home">Home Page</Route>
				<Route path="/**">Page Not Found</Route>
			</Router>
		</div>
	</div>
</div>

<style>

* {
	font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
}

.page-root {
	width: 100%;
	height: 100%;
	display: flex;
	flex-direction: column;
	justify-content: center;
	align-items: center;
	position: absolute;
	left: 0;
	right: 0;
	top: 0;
	bottom: 0;
}

.page-header {
	width: 100%;
	display: block;
	color: #ffffff;
	background-color: #00bd9c;
	font-size: 32px;
	font-weight: bolder;
	text-align: center;
}

a {
	width: 100%;
	height: 100%;
	display: block;
	padding: 40px;
	color: #ffffff;
	text-decoration: none;
}

.page-content {
	width: 100%;
	display: block;
	flex-grow: 1;
	font-size: 32px;
	text-align: center;
	overflow-y: auto;
}

.page-content-center {
	width: 100%;
	height: 100%;
	display: flex;
	flex-direction: row;
	justify-content: center;
	align-items: center;
	color: #515151;
}

</style>