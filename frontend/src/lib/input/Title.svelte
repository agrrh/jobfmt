<script>
import { title } from '../../../scripts/stores.js';
</script>

<!-- Grade and Title -->
<div class="row">
  <div class="input-field col s12">
    <input placeholder="DevOps-инженер" id="title" type="text" class="validate" on:input={e => title.set(e.target.value)}>
    <label for="title">Позиция</label>
  </div>

  <!-- <div class="input-field col s12">
    <select multiple id="format_grade">
      <option value="0" selected>N/A</option>
      <option value="1">Intern</option>
      <option value="2">Junior</option>
      <option value="3">Middle</option>
      <option value="4">Senior</option>
      <option value="5">Lead / Head</option>
    </select>
    <label for="format_time">Уровень</label>
    <span class="helper-text" data-error="wrong" data-success="right">Helper text</span>
  </div> -->
</div>
