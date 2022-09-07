<script>
document.addEventListener('DOMContentLoaded', function() {
	var elems = document.querySelectorAll('.collapsible');
	var options = {
		accordion: false
	};
	var instances = M.Collapsible.init(elems, options);
});
</script>

<div class="row">
  <div class="input-field col s12">
    <input placeholder="Россия" id="title" type="text" class="validate">
    <label for="title">Локация</label>
  </div>
</div>

<!-- TODO Добавить выбор, требуется ли релокация для иногородних -->
<!-- TODO Добавить выбор, есть ли релокационный пакет -->
