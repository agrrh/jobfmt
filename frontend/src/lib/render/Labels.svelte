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

<!-- Labels -->
<div class="row">
  <div class="col s12">
    <span class="color-red color-lighten-4">labels</span>
    <div class="chips chips-stack" id="labels"></div>
  </div>
</div>
