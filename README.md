## Проект “Англо-русский словарь”

***Задачи:***
- Написать программу для создания англо-русского словаря по книге на английском языке.

***Используемые технологии:***
- Java JDK 11, Collections, Git, Github, IntelliJ IDEA, Maven, API Яндекс.Словарь, библиотеки Jackson, Lombok, Apache HttpComponents, itextpdf, Evo Inflector

***Результаты:***
- Для работы с json использовал библиотеку Jackson, для pdf - itextpdf
- Для поиска английских слов во множественном числе использовал библиотеку Evo Inflector
- Также использовал Lombok - для сокращения количества кода и Apache HttpComponents для работы с HTTP
- Работа программы заключается в следующем:
    - В папку проекта в /pdf необходимо положить OCR-распознанный файл книги на английском языке
    - При помощи itextpdf из файла вычитываю слова в коллекцию TreeSet
    - Затем удаляю все английские слова во множественном числе через библиотеку Evo Inflector
    - Для каждого слова из коллекции отправляю запрос на Яндекс.Словарь, полученный перевод слова записываю в txt-файл
    - В итоге в корне папки проекта получаем англо-русский словарь Dictionary.txt, который затем можно распечатать