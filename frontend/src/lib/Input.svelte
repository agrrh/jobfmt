<script>
import GradeAndTitle from './input/GradeAndTitle.svelte';
import Format from './input/Format.svelte';
import Location from './input/Location.svelte';
import Salary from './input/Salary.svelte';
import TechStack from './input/TechStack.svelte';
import Description from './input/Description.svelte';

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

	<!-- TODO Добавить название компании / КА -->

		<GradeAndTitle />
		<Format />
		<Salary />

		<Location />

		<TechStack />

		<Description />

	</form>
</div>
