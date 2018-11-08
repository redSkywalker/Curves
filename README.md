# Curves
v 1.4 Оптимизация кода. 
- Внесены изменения в класс Shape: добавлен статический метод для factory method
- внесены изменения в метод main(Program.cpp):
  - изменено наполнение первого контейнера через factory method
  - убраны лишние временные переменные при выводе точек и при наполнении второго контейнера
  - оптимизирован функтор сравнения для сортировки (заменен лямбдой)
 (код из предыдущей версии не убран, а закомментирован для наглядности)

v 1.3 Все вычисления, в тч наполнение контейнеров, происходят в функции main(Program.cpp).
По сравнению с предыдущей версией: 
- исправлена формула вычисления точки на спирали (Helix)
- использована передача аргументов в функции-члены классов по ссылке, в тч константной, что оптимизировало код и сократило время выполнения
- использованы умные указатели shared_ptr в решении задачи
- у функции сравнения идентичности адресов указателей в первом и втором контейнерах изменена реализация на использующую std::owner_before
- упрощена реализация подсчета суммы радиусов и предиката сравнения для сортировки
