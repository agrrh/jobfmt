<script>
document.addEventListener('DOMContentLoaded', function() {
	var elems = document.querySelectorAll('.chips-autocomplete');
	var options = {
		autocompleteOptions: {
			data: {
				'Kubernetes': null,
				'Linux': null,
				'AWS': null
			},
			limit: Infinity,
			minLength: 1
		}
	}
	var instances = M.Chips.init(elems, options);
});

document.addEventListener('DOMContentLoaded', function() {
	var elems = document.querySelectorAll('select');
	var options = {
	};
	var instances = M.FormSelect.init(elems, options);
});
</script>

<div class="row">
	<form class="col s12">

	<!--

	Город и адрес офиса: ... (район или метро)
	Формат работы: офис или удаленка
	Занятость: полная, частичная, проектная
	Зарплатная вилка: от ... до ... или фикс, если сумма оплаты фиксирована (нужно отдельно указать, что фикс)
	(если у вас зарубежная вакансия сумма должна быть после налогов либо с ссылкой на калькулятор. «По договоренности» или «по результатам собеседования» не подходит, только конкретная вилка)
	Описание вакансии: ... (обязательно опишите текущий стек и задачи)
	Название компании: ...
	(с ссылкой; если у вас кадровое агентство — укажите название КА)
	Контакты: ...

	-->

		<!-- Title -->
		<div class="row">
			<div class="input-field col s12">
				<input placeholder="DevOps-инженер" id="title" type="text" class="validate">
				<label for="title">Позиция</label>
			</div>
		</div>

		<div class="row">
			<!-- Format -->
			<div class="input-field col s6">
				<select multiple id="format_time">
					<!-- <option value="" disabled selected>Choose your option</option> -->
					<option value="1" selected>Полная</option>
					<option value="2">Частичная</option>
				</select>
				<label for="format_time">Занятость</label>
			</div>

			<!-- Format -->
			<div class="input-field col s6">
				<select multiple id="format_office">
					<!-- <option value="" disabled selected>Choose your option</option> -->
					<option value="1" selected>Удаленка</option>
					<option value="2">Гибрид</option>
					<option value="3">Офис</option>
				</select>
				<label for="format_office">Формат</label>
			</div>
		</div>

		<!-- Location -->
		<div class="row">
			<div class="input-field col s12">
				<input placeholder="Россия" id="title" type="text" class="validate">
				<label for="title">Локация</label>
			</div>
		</div>

		<!-- TODO: Добавить раздел про релокацию -->
		<!-- TODO: Добавить галочку "релокация обязательна" -->

		<!-- Salary -->
		<div class="row">
			<div class="input-field col s2">
				<input placeholder="RUB" id="salary_currency" type="text">
				<label for="title">Валюта</label>
			</div>
			<div class="input-field col s5">
				<input placeholder="120 000" id="salary_min" type="text">
				<label for="title">Вилка от</label>
			</div>
			<div class="input-field col s5">
				<input placeholder="300 000" id="salary_max" type="text">
				<label for="title">Вилка до</label>
			</div>
		</div>

		<!-- Tech stack -->
		<div class="row">
			<div class="input-field col s12">
				<div class="chips chips-autocomplete" id="tech_stack"></div>
				<label for="tech_stack">Технологии</label>
			</div>
		</div>

		<!-- Description -->
		<div class="row">
			<div class="input-field col s12">
				<input placeholder="Описание деталей" id="title" type="text" class="validate">
				<label for="title">Description</label>
			</div>
		</div>

	</form>
</div>
