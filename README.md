# \<s>ПИП\</s>

## _lab_ #1 - [here](http://p-n-p.herokuapp.com/l1/)
<table>
<tr><td></td><td>Разработать PHP-скрипт, определяющий попадание</td><td></td><tr>
<tr><td></td><td>точки на координатной плоскости в заданную область,</td><td></td><tr>
<tr><td></td><td>и создать HTML-страницу, которая формирует данные</td><td></td><tr>
<tr><td></td><td>для отправки их на обработку этому скрипту.</td><td></td><tr>
<tr><td></td><td>Параметр R и координаты точки должны передаваться</td><td></td><tr>
<tr><td></td><td>скрипту посредством HTTP-запроса. Скрипт должен</td><td></td><tr>
<tr><td></td><td>выполнять валидацию данных и возвращать HTML-страницу</td><td></td><tr>
<tr><td></td><td>с таблицей, содержащей полученные параметры и</td><td></td><tr>
<tr><td></td><td>результат вычислений - факт попадания или непопадания</td><td></td><tr>
<tr><td></td><td>точки в область. Кроме того, ответ должен</td><td></td><tr>
<tr><td></td><td>содержать данные о текущем времени и времени работы</td><td></td><tr>
<tr><td></td><td>скрипта.</td><td></td><tr>
<tr><td></td><td></td><td></td><tr>
<tr><td></td><td><img alt="lab1 areas.png" src="l1/static/images/areas.png"></td><td></td><tr>
<tr><td></td><td>Разработанная HTML-страница должна удовлетворять</td><td></td><tr>
<tr><td></td><td>следующим требованиям:</td><td></td><tr>
<tr><td></td><td>* Для расположения текстовых и графических элементов</td><td></td><tr>
<tr><td></td><td>необходимо использовать <strong><i><code>табличную верстку</code></i></strong>.</td><td></td><tr>
<tr><td></td><td>* Данные формы должны передаваться на обработку</td><td></td><tr> 
<tr><td></td><td>посредством GET-запроса.</td><td></td><tr>
<tr><td></td><td>* Таблицы стилей должны располагаться в отдельных</td><td></td><tr>
<tr><td></td><td>файлах.</td><td></td><tr>
<tr><td></td><td>* При работе с CSS должно быть продемонстрировано</td><td></td><tr>
<tr><td></td><td>использование селекторов атрибутов, селекторов</td><td></td><tr>
<tr><td></td><td>потомств, селекторов дочерних элементов, селекторов</td><td></td><tr>
<tr><td></td><td>элементов а также такие свойства стилей CSS, как</td><td></td><tr>
<tr><td></td><td>наследование и каскадирование.</td><td></td><tr>
<tr><td></td><td>* HTML-страница должна иметь "шапку", содержащую</td><td></td><tr>
<tr><td></td><td>ФИО студента, номер группы и новер варианта. При</td><td></td><tr>
<tr><td></td><td>оформлении шапки необходимо явным образом задать</td><td></td><tr>
<tr><td></td><td>шрифт (sans-serif), его цвет и размер в каскадной</td><td></td><tr>
<tr><td></td><td>таблице стилей.</td><td></td><tr>
<tr><td></td><td>* Отступы элементов ввода должны задаваться в процентах.</td><td></td><tr>
<tr><td></td><td>* Страница должна содержать сценарий на языке JavaScript,</td><td></td><tr>
<tr><td></td><td>осуществляющий валидацию значений, вводимых пользователем</td><td></td><tr>
<tr><td></td><td>в поля формы. Любые некорректные значения (например,</td><td></td><tr>
<tr><td></td><td>буквы в координатах точки или отрицательный радиус)</td><td></td><tr>
<tr><td></td><td>должны блокироваться.</td><td></td><tr>
</table>

---

## _lab_ #2
Разработать веб-приложение на базе сервлетов и JSP, определяющее попадание точки на координатной плоскости в заданную область.

**Приложение должно быть реализовано в соответствии с шаблоном MVC и состоять из следующих элементов**:
  * **ControllerServlet**, определяющий тип запроса, и, в зависимости от того, содержит ли запрос информацию о координатах точки и радиусе, делегирующий его обработку одному из перечисленных ниже компонентов. Все запросы внутри приложения должны передаваться этому сервлету (по методу GET или POST в зависимости от варианта задания), остальные сервлеты с веб-страниц напрямую вызываться не должны.
  * **AreaCheckServlet**, осуществляющий проверку попадания точки в область на координатной плоскости и формирующий HTML-страницу с результатами проверки. Должен обрабатывать все запросы, содержащие сведения о координатах точки и радиусе области.
  * **Страница JSP**, формирующая HTML-страницу с веб-формой. Должна обрабатывать все запросы, не содержащие сведений о координатах точки и радиусе области.
  
![lab2 areas.png](l2/web/img/areas.png)

**Разработанная страница JSP должна содержать**:
  1) "Шапку", содержащую ФИО студента, номер группы и номер варианта.
  2) Форму, отправляющую данные на сервер.
  3) Набор полей для задания координат точки и радиуса области в соответствии с вариантом задания.
  4) Сценарий на языке JavaScript, осуществляющий валидацию значений, вводимых пользователем в поля формы.
  5) Интерактивный элемент, содержащий изображение области на координатной плоскости (в соответствии с вариантом задания) и реализующий следующую функциональность:
    * Если радиус области установлен, клик курсором мыши по изображению должен обрабатываться JavaScript-функцией, определяющей координаты точки, по которой кликнул пользователь и отправляющей полученные координаты на сервер для проверки факта попадания.
    * В противном случае, после клика по картинке должно выводиться сообщение о невозможности определения координат точки.
    * После проверки факта попадания точки в область изображение должно быть обновлено с учётом результатов этой проверки (т.е., на нём должна появиться новая точка).
  6) Таблицу с результатами предыдущих проверок. Список результатов должен браться из контекста приложения, HTTP-сессии или Bean-компонента в зависимости от варианта.

**Страница, возвращаемая AreaCheckServlet, должна содержать**:
  * Таблицу, содержащую полученные параметры.
  * Результат вычислений - факт попадания или непопадания точки в область.
  * Ссылку на страницу с веб-формой для формирования нового запроса.
  
**Разработанное веб-приложение необходимо развернуть на сервере GlassFish**.
