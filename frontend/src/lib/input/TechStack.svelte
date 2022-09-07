<script>
document.addEventListener('DOMContentLoaded', function() {
	var elems = document.querySelectorAll('.chips-stack');
	var options = {
		data: [{
			tag: 'Kubernetes',
		}, {
			tag: 'Linux',
		}],
		autocompleteOptions: {
			data: {
				'Kubernetes': null,
				'Linux': null,
				'AWS': null
			},
			limit: Infinity,
			minLength: 1
		},

	}
	var instances = M.Chips.init(elems, options);
});
</script>

<!-- Tech stack -->
<div class="row">
  <div class="input-field col s12">
    <span class="color-grey color-lighten-4">Технологии</span>
    <div class="chips chips-stack" id="tech_stack"></div>
  </div>
</div>
