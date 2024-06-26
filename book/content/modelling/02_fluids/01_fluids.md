# Жидкости и газы

## Обзор
Гидродинамика описывает движение жидкостей или газов. Возможно, потребуется принять во внимание следующие аспекты:

* сжимаемость
* граничные условия, например, стены
* турбулентность
* теплопроводность
* химические реакции
* различные виды и состояния вещества
* и т.д.

**Наука о пожарной безопасности**

В науке о пожарной безопасности гидродинамика играет важную роль в понимании динамических явлений пожара. Гидродинамику необходимо учитывать, например, во время процессов смешивания, горения, конвективного теплообмена или распространения дыма в сложных зданиях.

<iframe width="60%" src="https://www.youtube-nocookie.com/embed/sKgP1Us-SF0" title="YouTube video player" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe><br>


**Технические применение**

Классическим примером применения является оптимизация транспортных средств для уменьшения лобового сопротивления.

<iframe width="60%" src="https://www.youtube-nocookie.com/embed/E9ZSAX56m0E" title="YouTube video player" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Основы 

В гидродинамике наиболее фундаментальными являются следующие процессы:

* **Поток** описывает движение среды. Это векторное поле описывает скорость жидкости в каждой точке пространства и времени: $\mf \vv = \vv(x,t)$. Компоненты скорости обозначаются как $\mf \vv = (v_x,v_y,v_z) = (u,v,w)$.
* **Конвекция** это внутреннее движение жидкости, то есть обусловленное плавучестью.
* **Адвекция** описывает перенос вещества или свойств (плотность, температура, дым) под действием потока. Конвекция - это адвекция скорости.
* **Диффузия** это процесс, который управляет процессом балансировки для уравновешивания различий в свойствах потока (скорость, температура, плотность дыма).


### Количественные показатели потока

 ```{list-table} Количественные показатели потока.
:header-rows: 1
:name: tab-flow-quantities
:widths: auto

* - Имя
   - Символ
   - Блок
   - Тип
* - плотность 
   - $\mf \rho$
   - $\mf kg/m^3$
   - скалярное поле
* - скорость 
   - $\mf \vv$
   - $\mf m/s$
   - векторное поле
* - вихреобразование
   - $\mf \vec{\omega} = \nabla \times \vv$
   - $\mf 1/s$
   - векторное поле
* - плотность импульса 
   - $\mf \vu = \rho\vv$
   - $\mf kg/(m^2~s)$
   - векторное поле 
* - давление
   - $\mf p$
   - $\mf Pa = kg/(m^2~s)$
   - скалярное поле 
* - температура
   - $\mf T$
   - $\mf K$
   - скалярное поле
* - удельная энтальпия
   - $\mf h = \int_{T_0}^T c_p(T')\ dT' + \Delta h_f^0$
   - $\mf J/kg = m^2/s^2$
   - скалярное поле
```

Где  $\mf c_p(T)$ это теплоемкость при температуре $\mf T$ и $\mf \Delta h_f^0$ это теплота образования.

### Скорость звука

В жидкостях и твердых телах информация (изменения потока, возмущения) распространяется с конечной скоростью: скоростью звука. Звуковые волны представляют собой волны продольного сжатия. Типичные скорости распространения следующие $\mf 343~m/s$ в воздухе, $\mf 1484~m/s$ в воде и $\mf 5120~m/s$ в стали. В целом скорость звука $\mf c_s$ в идеальном газе опредлеляется:

$$
\mf c_s = \sqrt{\frac{\gamma k_B T}{m}}
$$(eq-speed-of-sound)

где  $\mf \gamma$ коэффициент теплоемкости $\mf \gamma=c_P/c_V$, $\mf k_B$ постоянная Больцмана ($\mf \sim\!1.381\cdot 10^{−23}~J/K$), T температура газа и $\mf m$ масса одной молекулы газа. В общем случае для данного вида газа скорость звука зависит только от температуры. Для сухого воздуха ее можно приблизительно определить как:

$$
\mf c_{s, air} =(331.3+0.606\cdot \Theta) m/s 
$$(eq-c-in-air)

где  $\mf \Theta$ температура воздуха при  $\mf ^\circ C$.

### Уравнение состояния

Для идеального газа состояние обычно можно описать в терминах двух термодинамических переменных ($\mf n$, $\mf\rho$, $\mf p$, $\mf e$, $\mf T$, $\mf V$, $\mf m$, $\mf h$). Следуя комбинации законов Бойля и Чарльза в термодинамическом равновесии, уравнение состояния имеет вид:

$$
\mf pV = nRT
$$(eq-equation-of-state)

где $\mf R = 8.314~J/(mol~K)$ универсальная газовая постоянная и $\mf n$ количество частиц. Реактивные потоки в основном представляют собой соединения нескольких различных видов. Таким образом, уравнение состояния для системы, находящейся в равновесии с  $\mf N$  виды становятся

$$
\mf p = f(V, T, n_1 , \dots , n_N)\quad .
$$

Закон парциальных давлений Дальтона $\mf p_i$ позволяет сформулировать общее давление

$$
\mf p = \sum_{i=1}^N p_i = \frac{1}{V} \sum_{i=1}^N n_i R T\quad .
$$

## Описание потоков
Потоки текучих сред (жидкостей и газов) имеют одни и те же основные характеристики. Далее не будет различий в потоках жидкости или газа. Они будут отличаться только свойствами материала. Примеры для потока текучей среды:


:::{figure-md} fig-fluid-vortex-island

<img src="https://upload.wikimedia.org/wikipedia/commons/2/2c/Vortex-street-1.jpg" width="40%" class="rotate90">

Вихревая дорожка Фон Кармана, наблюдаемая в природе. Источник: [Wikkimedia Commons](https://commons.wikimedia.org/wiki/File:Vortex-street-1.jpg).
:::


:::{figure-md} fig-fluid-vortex-lab

<img src="https://upload.wikimedia.org/wikipedia/commons/f/fe/VortexStreet01.jpg" width="80%">

Вихревая дорожка Фон Кармана в лаборатории. Источник: [Wikkimedia Commons](https://commons.wikimedia.org/wiki/File:VortexStreet01.jpg).
:::

### Сжимаемые потоки

Потоки со скоростями, значительно меньшими ($\mf \ll c_s$) ниже скорости звука являются несжимаемыми, т.е. звуковые волны бесконечно быстры в масштабе задействованных процессов. Таким образом, все изменения плотности быстро уравновешиваются. Объекты, движущиеся со скоростью не менее $\mf 0.3c_s$ начнут вносить флуктуации в плотность. Схемы течения сверхзвуковых явлений (взрыв, сверхзвуковые самолеты) и соответствующие инженерные подходы полностью отличаются от таковых в случае субзвуковых течений.

Примечание: Изменения температуры, как и при пожаре, приводят к изменению плотности и, следовательно, к так называемым слабо сжимаемым потокам.

:::{figure-md} fig-fluid-laminar

<img src="https://upload.wikimedia.org/wikipedia/commons/b/b9/Aerodynamics_of_model_car.jpg" width="60%">

Несжимаемое течение вокруг модели автомобиля. Источник: [Wikkimedia Commons](https://commons.wikimedia.org/wiki/File:Aerodynamics_of_model_car.jpg).
:::


:::{figure-md} fig-fluid-supersonic

<img src="https://upload.wikimedia.org/wikipedia/commons/0/06/X-15_Model_in_Supersonic_Tunnel_-_GPN-2000-001272.jpg" width="60%">

Модель сверхзвукового самолета в туннеле со скоростью около $\mf 3.5 c$. Источник: [Wikkimedia Commons](https://en.wikipedia.org/wiki/Compressible_flow#/media/File:X-15_Model_in_Supersonic_Tunnel_-_GPN-2000-001272.jpg).
:::

### Турбулентные течения

В зависимости от того, насколько гладким (непрерывным) является поток, можно различать ламинарные и турбулентные потоки. Потоки, связанные с пожарами, обычно являются турбулентными.


:::{figure-md} fig-fluid-turbulence-separation

<img src="https://upload.wikimedia.org/wikipedia/commons/2/2f/1915ca_abger_fluegel.jpg" width="60%">

Обтекание профиля с отрывом потока. Материал: [Wikkimedia Commons](https://commons.wikimedia.org/wiki/File:1915ca_abger_fluegel.jpg).
:::

<iframe width="60%" src="https://www.youtube.com/embed/QzuzbwJWlYs" title="YouTube video player" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


### Свойства веществ

Фундаментальный интерес представляют следующие свойства веществ:

* **плотность** $\mf\rho$ это масса на объем
  * воздух при $\mf 20~^\circ C$ : $\mf\rho = 1.205~kg/m^3$
  * воздух при $\mf 200~^\circ C$: $\mf\rho = 0.746~kg/m^3$
* **динамическая вязкость** $\mf\mu$ характеризует способность потока уравновешивать различия в скорости
  * воздух при $\mf 20~^\circ C$ : $\mf\mu = 1.836\cdot 10^{-5}~kg\,m / s$
  * воздух при $\mf 200~^\circ C$: $\mf\mu = 2.623\cdot 10^{-5}~kg\,m / s$
* **теплопроводность** $\mf k$ эквивалентно  $\mf\mu$, но для температуры жидкости
  * воздух при $\mf 20~^\circ C$ : $\mf k = 0.0257~W\,m / K$
  * воздух при $\mf 200~^\circ C$: $\mf k = 0.0386~W\,m / K$
* **теплоемкость** $c_p$ описывает изменение температуры вследствие добавления или отвода тепла при постоянном давлении
  * воздух при $\mf 20~^\circ C$ : $\mf c_p = 1.005~kJ\,kg / K$
  * воздух при $\mf 200~^\circ C$: $\mf c_p = 1.026~kJ\,kg / K$


Дополнительные данные по многим свойствам воздуха (и другим веществам) можно найти в [Engineering ToolBox (свойства воздуха)](https://www.engineeringtoolbox.com/air-properties-d_156.html).

**Примерное величины: вязкость**

Проще говоря, вязкость описывает, как движущиеся элементы жидкости, например слои, влияют на соседние элементы. Она описывает силы трения между относительно движущимися элементами жидкости.

Например, мед обладает высокой вязкостью: он очень медленно стекает по ложке. Внешние "элементы меда” прочно связаны с внутренними – несвободными – элементами.

:::{figure-md} fig-fluid-honey

<img src="https://upload.wikimedia.org/wikipedia/commons/c/cc/Runny_hunny.jpg" width="40%">

Мед, стекающий по ложке. Источник: [Wikkimedia Commons](https://commons.wikimedia.org/wiki/File:Runny_hunny.jpg).
:::

В простой двумерной установке с неподвижной и движущейся стенками, см. {numref}`fig-fluid-viscosity`, динамическая вязкость описывает соотношение сил, действующих на стенки, и градиента скорости. Если градиент скорости $\mf u/y$ является постоянным, это приводит к следующей силе трения на площадь:

$$
\mf \frac{F}{A} = \mu \cdot \frac{u}{y} 
$$ (eq-dyn-vis)


:::{figure-md} fig-fluid-viscosity

<img src="https://upload.wikimedia.org/wikipedia/commons/9/93/Laminar_shear.svg" width="60%">

Визуализация концепции вязкости. Материал: [Wikkimedia Commons](https://commons.wikimedia.org/wiki/File:Laminar_shear.svg).
:::

Соотношение  {eq}`eq-dyn-vis` является определением *динамической вязкости* $\mf \mu$. Тем не менее, в некоторых случаях *кинематическая вязкость* $\mf \nu$  (или коэффициент диффузии по импульсу) является более удобной величиной. Он определяется как отношение динамической вязкости к плотности

$$
\mf \nu = \frac{\mu}{\rho} \quad .
$$ (eq-kin-vis)


Жидкости, вязкость которых не зависит от напряженного состояния, называются ньютоновскими жидкостями, все газы являются ньютоновскими жидкостями. Однако существуют также [неньютоновские жидкости](https://en.wikipedia.org/wiki/Non-Newtonian_fluid), такие как кровь, томатный кетчуп и вода, смешанная с кукурузным крахмалом.

<iframe width="60%" src="https://www.youtube-nocookie.com/embed/B6h5pVETbd8" title="YouTube video player" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

### Безразмерные числа

Многие явления и типы потоков могут характеризоваться безразмерными числами. Предполагается, что потоки с аналогичными характеристиками сопоставимы, хотя, например, пространственные масштабы различны. Некоторые из обычно используемых безразмерных чисел являются:
* [Число Маха](https://en.wikipedia.org/wiki/Mach_number) $\mf Ma$
* [Число Рейнольдса](https://en.wikipedia.org/wiki/Reynolds_number) $\mf Re$
* Число Грасхофа $\mf Gr$
* Число Прандтля $\mf Pr$
* Число Архимеда $\mf Ar$
* Число Ричардсона $\mf Ri$
* Число Нусселя $\mf Nu$


**Число Маха**

Число Маха определяется как отношение скорости к скорости звука:

$$
\mf Ma = \frac{v}{c_s}
$$ (eq-mach-number)

Это число характеризует сжимаемость потока: 
* $\mf Ma \rightarrow 0$: полностью несжимаемые
* $\mf Ma \lesssim 0.3$: несжимаемые
* $\mf Ma \gtrsim 0.3$: сжимаемые

Предел  $\mf Ma \rightarrow 0$ также могут быть истолкованы как $\mf c \rightarrow \infty$.

**Число Рейнольдса**

Число Рейнольдса связывает конвекцию с диффузией: 

$$
\mf Re = \frac{\rho v L}{\mu}
$$

Здесь, $\mf L$ обозначает характерную длину, в случае течения в трубе это будет диаметр трубы. Число Рейнольдса может использоваться для отличия ламинарных течений от турбулентных, т.е. очень высокое $\mf Re$ представляет собой турбулентные потоки. В потоке по трубе характерным числом для перехода примерно $\mf Re \approx 4000$. Это число является классическим примером масштабирования. Явления текущие при одинаковом числе Рейнольдса будут вести себя одинаково; это может быть показано нормализацией уравнений течения.



:::{figure-md} fig-fluid-re-table

<img src="https://upload.wikimedia.org/wikipedia/commons/9/99/Reynoldsflugrpd.png" width="60%">

Скорость и числа Рейнольдса для некоторых летающих объектов (на немецком языке). (Staub: Пыль, Insekt: Насекомое, Modellflugzeug/Vogel: Модель самолета/Птица, Windrad: Ветряная мельница, Drachenflieger: Дельтаплан, Flugzeug: Самолет, Luftschiff: Дирижабль) Источник: [Wikkimedia Commons](https://de.wikipedia.org/wiki/Reynolds-Zahl#/media/Datei:Reynoldsflugrpd.png).
:::



## Уравнения движения жидкости

### Законы сохранения

Динамика жидкости основана на следующих трех физических законах сохранения: 

* сохранение массы
* сохранение импульса
* сохранение энергии

Из этих законов могут быть выведены основные уравнения течения жидкости: 

* уравнение непрерывности
* уравнение движения
* уравнение энергии

В общем случае, помимо этих уравнений требуется замыкание, например, с помощью уравнения состояния. Во многих случаях можно использовать закон идеального газа.

**Сохранение массы**

Сохранение массы предсказывает, что общая масса контрольного объема изменяется только при наличии чистого расхода (неравновесного входного и выходного потоков) через границы. Несжимаемые потоки всегда имеют нулевой чистый расход.

При моделировании пожара необходимо учитывать несколько компонентов (например, кислород, топливо и углекислый газ). Их масса сохраняется индивидуально. Однако они тесно связаны друг с другом через термины "источник". Например, во время горения кислород и топливо расходуются для получения углекислого газа.

**Сохранение импульса**

Импульс элемента жидкости изменяется только из-за: 

* адвекция импульса
* градиент давления
* диффузия и напряжения, т.е. из-за конечной вязкости
* внешние силы, например, гравитация, капли воды

При моделировании турбулентности особый интерес представляет диффузия. Это явление должно быть охвачено моделями турбулентности.

**Сохранение энергии**

Изменения энергии контрольного объема обусловлены:

* адвекция энергии
* теплопроводность
* процессы нагрева и охлаждения, например излучение, трение, горение

В сочетании с принципом сохранения энергии для определения температуры газа необходимо уравнение состояния.

### Дифференциальные уравнения в частных производных

Дифференциальные уравнения в частных производных (PDE) являются одним из самых мощных инструментов в науке и технике. Большинство технических, математических, физических, химических и даже биологических моделей основаны на дифференциальных уравнениях. Решения дифференциальных уравнений могут описывать:

* потоки газа и процессы горения
* распределение тепла в твердых телах
* колебания маятника
* распространение волн света или воды
* взаимодействие двух видов (хищника и жертвы)

**Типы PDE**

Общая структура PDE для $\mf\phi = \phi(x,y)$ дается:

$$
\mf a\partial_{xx}\phi + b\partial_{xy}\phi + c\partial_{yy}\phi + d\partial_x\phi + e\partial_y\phi + f\phi = 0
$$

где все коэффициенты ($\mf a,\dots,f$) зависят от $\mf x$ и $\mf y$, например  $\mf a = a(x,y)$.

Коэффициенты определяют характер PDE:

$$
\mf D(x,y) = a(x,y)\cdot c(x,y) - \left(\frac{b(x,y)}{2}\right)^2
$$

* $\mf D \gt 0$: эллиптическое, например, уравнение Лапласа
* $\mf D = 0$: параболическое, например, уравнение теплопроводности
* $\mf D \lt 0$: гиперболическое, например, волновое уравнение

Примечание: Тип может зависеть от различных параметров материала и/или положения, здесь $\mf (x,y)$.

**Полевые операторы**

Двумя наиболее распространенными математическими операторами, используемыми в гидродинамике, являются частная производная и оператор Набла.

**Частная производная** описывает изменение поля в заданном направлении пространства или времени. Изменение поля скоростей $\mf \vv(x,y,z,t)$ что касается времени, то:

$$
\mf \frac{\partial \vec{v}(x,y,z,t)}{\partial t} \quad \mbox{или короткий}\quad \partial_t \vec{v}(x,y,z,t)
$$

**Оператор Nabla** $\mf \nabla$ используется для представления операций Лапласа, градиента, расхождения и вращения.


$$
\mf \nabla = \left( \partial_x,  \partial_y,  \partial_z \right)
$$

$$
\mf \Delta(\rho) = \nabla^2\rho \\
\mf grad(\rho) = \nabla\rho \\
\mf div(\vv) = \nabla\cdot\vv \\
\mf rot(\vv) = \nabla\times\vv
$$

**Конвективная производная** объединяет оба оператора. Она представляет полное изменение значения из-за локальных внутренних изменений и из-за адвекции. Изменение скалярного значения $\mf \phi(x,y,z,t)$ поэтому могут быть записаны следующим образом


$$
\mf \frac{d\phi}{dt} = \partial_t \phi + \vv\cdot(\nabla\phi)
$$

Первый член ($\mf \partial_t \phi$) представляет собой внутренние изменения, а второй ($\mf\vv\cdot(\nabla\phi)$) описывает изменения, вызванные адвекцией в поле скоростей $\mf\vv$.

### Уравнение непрерывности

Уравнение непрерывности для потока одного вида имеет вид:

$$
\mf \frac{d\rho}{dt} = \underbrace{-\rho\nabla\cdot\vec{v}}_{A}
$$ (eq-fluid-cont)

* $\mf A$: чистый расход массы

Принимая во внимание конвективную производную, обычно используемая формулировка может быть получена следующим образом:

$$
\mf \partial_t \rho = -\nabla\cdot(\rho\vec{v})\quad .
$$ (eq-fluid-cont-conservative)

### Уравнение движения

Принимая во внимание сохранение импульса, можно сформулировать следующую простую форму уравнения движения

$$
\mf \partial_t \rho\vec{v} + \nabla\cdot(\rho\vec{v}\vec{v}) = \underbrace{-\nabla p}_{A} + \underbrace{\mu\nabla^2\vec{v}}_{B} + \underbrace{\vec{f}}_{C}
$$ (eq-fluid-momentum)

* $\mf A$: усилие, обусловленное перепадами давления
* $\mf B$: молекулярная диффузия
* $\mf C$: внешние силы, например, гравитация

Это уравнение широко известно как уравнение Навье-Стокса.


### Уравнение энергии

Уравнение для энергии $E = e + \frac{1}{2}\vv^2$ дается

$$
\mf \partial_t (\rho E) + \nabla\cdot(\vec{v}\rho E) = \underbrace{-\nabla\cdot(\vec{v}p)}_{A} + \underbrace{\nabla\cdot(\mu\vec{v}\nabla\vec{v})}_{B} + \underbrace{\nabla\cdot(k\nabla T)}_{C}+ \underbrace{\vec{v}\cdot\vec{f}}_{D}+\underbrace{\dot{Q_s}}_{E}
$$ (eq-fluid-energy)

* $\mf A$: работа, выполняемая с жидкостью из-за перепадов давления
* $\mf B$: работа, выполняемая с помощью вязкости
* $\mf C$: теплопроводность
* $\mf D$: работа, выполняемая внешними силами
* $\mf E$: источники и поглотители тепла


Примечание: Иногда предпочтительнее формулировка в терминах энтальпии. Это относится к уравнениям, решаемым с помощью FDS.

### Уравнения несжимаемости

Если поток несжимаемый и предполагается, что он изотермический, то остальные уравнения, которые необходимо решить, следующие:



$$
\mf \partial_t \rho\vec{v} + \nabla\cdot(\rho\vec{v}\vec{v}) = -\nabla p + \mu\nabla^2\vec{v} + \vec{f} \\
\mf \nabla^2 p = - \nabla\cdot\left(\nabla\cdot(\rho\vec{v}\vec{v})\right) + \nabla \cdot \vec{f}
$$

### Режим слабого сжатия

В полностью *несжимаемых* потоках давление мгновенно уравновешивает все расхождения и, следовательно, поддерживает плотность постоянной.

В режиме *сжимаемости* закон идеального газа обеспечивает связь между сохранением энергии и массы и импульса.

Для потоков с низкой скоростью, как при пожарах, но при значительных колебаниях температуры плотность может изменяться. Это не связано с колебаниями давления, поскольку давление остается относительно неизменным. Это так называемый *слабо сжимаемый* режим.

Здесь используется уравнение состояния при фиксированном давлении окружающей среды $\mf p_0$ для определения плотности:

$$
\mf \rho = \frac{p_0 M}{R T}
$$

с $\mf M$ представляет собой молекулярную массу интересующего объема.

## Граничные условия

Помимо уравнений жидкости, другим важным аспектом являются граничные условия. Во многих приложениях влияние граничных условий имеет решающее значение, и их надлежащая обработка необходима.

В общем случае существует несколько типов граничных условий:

* Дирихле: заданы явные значения

  $$
  \mf u=u_0\quad v=w=0
  $$

* Нейман: предписывается нормальная производная

  $$
  \mf \partial_n u = n_0\quad \partial_n v = \partial_n w = 0
  $$

* симметричные: производные используются для сохранения предписанной симметрии
* периодические: значения на границах облицовки поддерживаются равными


Некоторые явные примеры граничных условий, обычно используемых в гидродинамике: 

* отсутствие скольжения по сплошной стене
  
  $$
  \mf u = v = w = 0 \quad \mbox{у стены}
  $$
* вход для газа
  
  $$
  \mf u = u_0\quad v=w=0 \quad \mbox{в притоке}
  $$
* утечка газа

  $$
  \mf \partial_n u = \partial_n v = \partial_n w = 0\quad \mbox{на выходе}
  $$
* постоянная температура стенок

  $$
  \mf T = T_w
  $$
* стена с изменяющейся температурой, но фиксированным тепловым потоком

  $$
  \mf q_w = k \partial_n T\quad \mbox{у стены}
  $$
* адиабатический

  $$
  \mf k\partial_n T = 0 \quad \mbox{у стены}
  $$

:::{figure-md} fig-fluid-bnd-open

<img src="./figs/boundaries_open_plume.svg" width="60%">

Пример установки границы для открытого горения.
:::



:::{figure-md} fig-fluid-bnd-compartment

<img src="./figs/boundaries_compartment.svg" width="60%">

Пример установки границ для простого отсека.
:::


**Перевод и адаптацию произвел Мироненко Роман Владимирович.**  
**Открыт для предложений по переводу и сотрудничеству.**  
**При использовании данного материала прошу давать ссылку на этот материал.**