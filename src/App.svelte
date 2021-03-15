<script>

import TextEditor from './components/TextEditor.svelte';

</script>

<div class="page-root">
	<div class="page-content">
		<div class="page-content-center">
			<TextEditor />
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
	align-items: stretch;
	color: #515151;
}

</style>