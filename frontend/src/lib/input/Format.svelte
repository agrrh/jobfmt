<script>
import { formatTime } from '../../../scripts/stores.js';
import { formatOffice } from '../../../scripts/stores.js';

function updateFormatTime(v) {
  const formatTimeV = {
    "1": "full-time",
    "2": "part-time",
  };

  var timeNotation = [];

  for (let item of v) {
    timeNotation.push(formatTimeV[item.value]);
  }

  formatTime.set(timeNotation);
}

function updateFormatOffice(v) {
  const formatOfficeV = {
    "1": "remote",
    "2": "hybrid",
    "3": "office",
  };

  var officeNotation = [];

  for (let item of v) {
    officeNotation.push(formatOfficeV[item.value]);
  }

  formatOffice.set(officeNotation);
}
</script>

<!-- Format -->
<div class="row">
  <div class="input-field col s12">
    <select multiple id="format_time" on:change={e => updateFormatTime(e.target.selectedOptions)}>
      <option value="1" selected>Полная</option>
      <option value="2">Частичная</option>
    </select>
    <label for="format_time">Занятость</label>
  </div>

  <div class="input-field col s12">
    <select multiple id="format_office" on:change={e => updateFormatOffice(e.target.selectedOptions)}>
      <option value="1" selected>Удаленка</option>
      <option value="2">Гибрид</option>
      <option value="3">Офис</option>
    </select>
    <label for="format_office">Формат</label>
  </div>
</div>
