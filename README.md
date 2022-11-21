В репозитории лежат файлы:
conftest.py
test_selenium_petfriends_pytest.py
requirements.txt
В файл conftest.py добавлен обработчик, который считывает из командной строки параметр language, а так же browser_name В файле conftest.py реализована логика запуска браузера с указанным языком пользователя. Браузер объявлется в фикстуре browser и передается в тест как параметр. В файл test_items.py написаны тесты:
  -Присутствуют все питомцы.
  -Хотя бы у половины питомцев есть фото.
  -У всех питомцев есть имя, возраст и порода.
  -У всех питомцев разные имена.
  -В списке нет повторяющихся питомцев (у которых совпадают имя, порода и возраст одновременно).
Пример: тест запускается с параметром browser_name следующей командой:
  pytest -s -v --browser_name chrome test_selenium_petfriends_pytest.py
  pytest -s -v --browser_name firefox test_selenium_petfriends_pytest.py
