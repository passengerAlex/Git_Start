# Итоговое задание по Проекту 3. Разведывательный анализ данных.
## Оглавление
1. Основные цели и задачи проекта
2. Краткая информация о данных
3. Этапы работы над проектом
4. Результат
# Основные цели и задачи проекта
Провести разведывательный анализ (EDA) датасета для дальнейшего построения модели, которая бы предсказывала результаты госэкзамена по математике для учеников школы.
## Краткая информация о данных
Датасет содержит информацию об 395 учениках (аббревиатура школы, пол, возраст,тип адреса, размер семьи, статус совместного жилья родителей, образование матери и отца, работа матери и отца, причина выбора школы, опекун, время в пути до школы, время на учёбу помимо школы в неделю, количество внеучебных неудач, дополнительная образовательная поддержка, семейная образовательная поддержка, дополнительные платные занятия по математике, дополнительные внеучебные занятия, посещал детский сад, хочет получить высшее образование, наличие интернета дома, в романтических отношениях, семейные отношения, свободное время после школы, проведение времени с друзьями, текущее состояние здоровья, количество пропущенных занятий, баллы по госэкзамену по математике)

## Этапы работы над проектом
* загрузка датасета и первичный отсмотр
* первичный анализ данных каждого критерия
* корреляционный анализ
* финальная подготовка датасета для построения модели
* выводы
## Результат
В результате EDA для анализа влияния критериев датасета на модель, которая предсказывала бы результаты госэкзамена по математике для каждого ученика школы были получены следующие выводы:

* в данных достаточно много пустых значений, только 3 столбца из 29 заполнены полностью. В некоторых процент пропусков доходит до 12%
* выбросы найдены:
  * в столбце возраст (значение 22 удалено)
  * в столбце score (значение 0.0 удалено, на его основе создан новый булевый критерий no_score)
* гипотезы:
  * отрицательная корреляция параметра age и score может говорить о том, что чем выше возраст тем ниже score
  * отрицательная корреляция параметра failures и score может говорить о том, что чем больше неудач по другим предметам тем ниже score
  * отрицательная корреляция параметра goout и score может говорить о том, что чем больше ученик проводит времени с друзьями тем ниже score
  * положительная корреляция по парамметру m_edu говорит о том, что чем выше лучше образование матери тем выше score
  *положительная корреляция по парамметру f_edu говорит о том, что чем выше лучше образование отца тем выше score
* cамых важных критериев, которые предлагается использовать в дальнейшем для построения модели 14, это: age, absences, address, schoolsup, m_edu, f_edu, m_job, f_job, studytime, failures, goout, paid, higher, romantic.
Результат работы включает полностью подготовленный числовой датасет **stud_for_model** и словарь соответствий между значениями датасета и описанием датасета **help_read_dict**
## Ответы на вопросы саморефлексии:
1. Какова была ваша роль в команде?
* one for all
2. Какой частью своей работы вы остались особенно довольны?
* доволен всеми частями
3. Что не получилось сделать так, как хотелось? Над чем ещё стоит поработать?
* Пока не ясно , на мой взгляд  все ок
4. Что интересного и полезного вы узнали в этом модуле?
* анализ графиков , вначале вообще не мог понять их
5. Что является вашим главным результатом при прохождении этого проекта?
* Чудо что я это не забросил , ведь на улице весна
6. Какие навыки вы уже можете применить в текущей деятельности?
* к моей текущей работы это не применимо
7. Планируете ли вы дополнительно изучать материалы по теме проекта?
* конечно 
