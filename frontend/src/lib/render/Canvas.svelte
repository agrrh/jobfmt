<script>
import { title } from '../../../scripts/stores.js';
import { formatTime } from '../../../scripts/stores.js';
import { formatOffice } from '../../../scripts/stores.js';
import { location } from '../../../scripts/stores.js';
import { salary } from '../../../scripts/stores.js';
import { description } from '../../../scripts/stores.js';

// TODO Optimize this shit

var titleValue = "store not reachable";
const titleUnsubscribe = title.subscribe(value => {
	titleValue = value;
});

var formatTimeValue = "store not reachable";
const formatTimeUnsubscribe = formatTime.subscribe(value => {
	formatTimeValue = value;
});

var formatOfficeValue = "store not reachable";
const formatOfficeUnsubscribe = formatOffice.subscribe(value => {
	formatOfficeValue = value;
});

var locationValue = "store not reachable";
const locationUnsubscribe = location.subscribe(value => {
	locationValue = value;
});

var salaryValue = "store not reachable";
const salaryUnsubscribe = salary.subscribe(value => {
	salaryValue = value;
});

var descriptionValue = "store not reachable";
const descriptionUnsubscribe = description.subscribe(value => {
	descriptionValue = value;
});

</script>

<form class="row">
	<div class="input-field col s12">
		<textarea id="canvas" class="materialize-textarea">
		{titleValue}
		{formatTimeValue}
		{formatOfficeValue}
		{locationValue}
		{salaryValue}
		{descriptionValue}
		</textarea>
		<label for="canvas">Превью</label>
	</div>
</form>

<style>
	textarea.materialize-textarea {
		min-height: 60vh;
	}
</style>
