<script>
	import Input from './lib/Input.svelte'
	import Render from './lib/Render.svelte'
</script>


<div class="container">
	<div class="row">
		<div class="col s8">
			<h1>jobs&nbsp;fmt</h1>
		</div>

		<div class="col s4">
			<a class="waves-effect waves-light btn-large right" href="#!"><i class="material-icons left">send</i>foo</a>
		</div>

		<div class="col s12">
			<hr>
		</div>
	</div>

	<div class="row">
		<div class="col s5">
			<Input />
		</div>
		<div class="col s6 push-s1">
			<Render />
		</div>
	</div>
</div>

<style>
	.btn-large {
		margin-top: 52px;
	}
</style>
