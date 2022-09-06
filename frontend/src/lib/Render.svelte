<script>
export let render = "Placeholder";
</script>

<div class="row">
	<form class="col s12">
		<div class="row">
			<div class="input-field col s12">
				<textarea id="sketch" class="materialize-textarea">{render}</textarea>
				<label for="sketch">Превью</label>
			</div>
		</div>
	</form>
</div>

<style>
	textarea.materialize-textarea {
		min-height: 60vh;
	}
</style>
