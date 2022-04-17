# Gradient-descent-vs-simulated-annealing

**Задача:** нарисовать траекторию пошагового спуска к минимуму градиентного метода и имитации отжига. Сравнить их работу при поиске мимимума тестовой функции, где тестовая функция: 

![](https://latex.codecogs.com/svg.image?min(418.9829N&plus;\sum\limits_{i=1}^{N}(-x_i\cdot&space;sin(\sqrt{|x_i|}))),)

где ![](https://latex.codecogs.com/svg.image?-500\leq&space;x_i\leq&space;500).

В работе рассматривается случай N = 2, график: 

![Image alt](https://github.com/valerizabby/Gradient-descent-vs-simulated-annealing/raw/main/picture/3D-graphic.png)

При решении задачи:
- реализован алгоритм градиентного спуска
- реализован алгоритм имитации отжига Коши
- подобраны оптимальные параметры для обоих алгоритмов, на которых те сходятся к глобальному минимуму тестовой функции

___
### Выводы:
Получилось найти глобальный минимум функции обоими алгоритмами с некоторыми нюансами.

**Градиентный спуск** спускается к глобальному минимуму только если точка, из которой начинается спуск, изначально лежит в такой окрестности глобального минимума, что антиградиент в точке направлен в него, что сильно снижает шанс нахождения глобального минимума с помощью одного запуска алгоритма.

Алгоритм **имитации отжига** оказался более эффективен, так как является вероятностным алгоритмом и даже если по ходу алгоритма мы оказывались в локальных минимумах, если длина шага подобрана оптимальна, из них удавалось выйти и продожить поиск глобального.
