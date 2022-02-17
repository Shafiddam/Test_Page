# Page_test
Testing Pages from Stepik_org (тестинг страниц, паттерны Page Object):

base_page.py
  """
  тут мы храним методы, которые применяются по всему проекту вообще, всё завернуто в класс, чтобы было удобно импортировать;
  """

locators.py
  """
  тут мы храним локаторы, в виде констант. Локаторы каждой отдельной страницы завёрнуты в класс, чтобы было удобно импортировать;
  """

main_page.py
  """
  тут мы храним методы по конкретной странице, завернутые в класс этой странице. 
  Класс этот - условный MainPage - наследник класса BasePage, чтобы можно было пользоваться методами, описанными в base_page.py
  """

test_main_page.py:
  """
  тест-кейсы для главной страницы (например тесты регистрации), которые будем запускать с помощью pytest. Мы будем создавать функции, которым:  
  1)выдаём нужный для проверки линк
  2)создаём в функции переменную page, которой передаём браузер из base_page.py(класс BasePage) и линк из шага 1)
  3)следом говорим "page, откройся", но методом из base_page.py(класс BasePage)
  4)добавляем проверки, которые создавали методами в main_page.py
  """

test_product_page.py:
  """
  тесты для товара(продукта), например добавление в корзину 
  """