# Структурные сущности — интерфейсы

## Интерфейс (Interface)
Интерфейсы очерчивают границу между выражением того, что делает абстракция, и реализацией того, как она это делает. **Интерфейс** – это набор операций, применяемый для описания сервиса класса или компонента.

Интерфейсы используются для визуализации, специфицирования, конструирования и документирования соединений внутри системы. Типы и роли представляют механизм моделирования статического и динамического согласования абстракции с интерфейсом в определенном контексте.

Хорошо структурированный интерфейс представляет четкое разделение внешнего и внутреннего представлений абстракции, обеспечивая понятность и доступность без необходимости погружаться в детали его реализации.

Интерфейс используется для описания услуг,предоставляемых классом. Интерфейсграфически изображается окружностью или в виде класса со стереотипом "interface". Интерфейс не может содержать атрибутов. Принято к началу имени интерфейса добавлять букву "I". Если интерфейс изображен окружностью, то для обозначения отношения реализации используется сплошная линия, а если в виде класса, то используется стандартная форма отношения реализации.

Многие языки программирования, включая Java и Python, поддерживают концепцию интерфейса. Интерфейсы – это важное средство не только разделения спецификации и реализации класса или компонента, но и определения внешнего представления пакета или подсистемы.

Интерфейсы в UML изображаются так, как показано на рис. такая нотация позволяет раздельно визуализировать описание абстракции и ее реализацию.

![](/assets/diagram-class/realesationInterface.png)

Интерфейс (**interface**) – это набор операций, используемый для описания сервиса класса или компонента. Тип (type) – это стереотип класса, используемый для спецификации домена объектов вместе с разрешенными для них операциями (но не методами). Роль (**role**) – это поведение сущности в определенном контексте.

Графически интерфейс может быть представлен как класс со стереотипом – это позволяет раскрыть его операции и прочие свойства. Для отображения связи между классом и интерфейсом используется специальная нотация. Предоставляемый интерфейс – тот, который описывает сервисы, обеспечиваемые классом, – показан в виде маленького кружка, присоединенного к прямоугольнику (классу). Требуемый интерфейс – тот, который один класс требует от другого, – выглядит как маленький полукруг, соединенный с прямоугольником (классом).

Помимо прочего интерфейсы могут использоваться в целях описания контракта для варианта использования или подсистемы.

## Имя интерфейса (Interface name)

У каждого интерфейса должно быть имя, отличное от имен других интерфейсов. **Имя** – это текстовая строка. Само по себе оно рассматривается как простое имя; квалифицированное имя – это имя интерфейса, предваренное именем пакета, в котором он содержится. Интерфейс может быть нарисован с указанием только имени.

![](/assets/diagram-class/namingInterface.png)

В имени интерфейса могут в любом количестве использоваться буквы латинского алфавита, цифры и некоторые знаки пунктуации (за исключением таких, как двоеточие, которое применяется для отделения имени интерфейса от имени содержащего его пакета). Имя может располагаться в несколько строк. Фактически имена интерфейсов – это краткие существительные или фразы-существительные, взятые из словаря моделируемой системы.

## Операции интерфейса (Methods interface)

Интерфейс – это именованный набор операций, применяемый для описания сервиса класса или компонента. В отличие от классов или типов, интерфейсы не описывают никакой реализации (то есть не могут включать в себя никаких методов, представляющих реализации операций). Подобно классу, интерфейс может содержать любое количество операций. Они могут быть дополнены свойствами видимости, параллельности, стереотипами, помеченными значениями и ограничениями.

Когда вы декларируете интерфейс, то изображаете его как класс со стереотипом, перечисляя операции в соответствующем разделе. Операции могут быть представлены только именем либо полной сигнатурой и прочими свойствами (см. рис.). С интерфейсами также можно ассоциировать сигналы.

![](/assets/diagram-class/interface.png)

## Связи между интерфейсами (relationships between interface)

Подобно классу, интерфейс может участвовать в связях обобщения, ассоциации и зависимости, а кроме того, в связи реализации. **Реализация** – это семантическая связь между двумя классификаторами, один из которых описывает контракт, а другой обязуется его исполнять.

Интерфейс специфицирует контракт для класса или компонента, не навязывая его реализации. Класс или компонент может реализовывать множество интерфейсов – в таком случае он обязуется исполнять все контракты точно и в полной мере, то есть предоставлять набор методов, которые правильно реализуют операции, определенные во всех этих интерфейсах. Набор предлагаемых сервисов называется **предоставляемым интерфейсом**.

Аналогичным образом класс или компонент может зависеть от множества интерфейсов. При этом он ожидает, что контракты будут предоставлены некоторым набором компонентов, реализующих интерфейсы. Набор сервисов, которые данный класс требует от других классов, называется **требуемым интерфейсом**. Интерфейс представляет собой соединительный элемент, связывающий компоненты системы. Интерфейс специфицирует контракт, две стороны которого – клиент и поставщик – могут изменяться независимо до тех пор, пока каждый из них соблюдает свои договорные обязанности.

Как явствует из рис., вы можете двумя способами показать, что элемент реализует интерфейс.

![](/assets/diagram-class/interfaceForExample.png)

Во-первых, существует простая форма: интерфейс и его связь реализации изображаются в виде линии, соединяющей прямоугольник (класс) и маленький кружок (в случае использования предоставляемого интерфейса) или маленький полукруг (в случае использования требуемого интерфейса). Эта форма удобна и даже предпочтительна, когда вы просто хотите показать соединения в вашей системе. Однако ограничения данной нотации в том, что вы не можете визуализировать операции или сигналы, представленные интерфейсом.

Во-вторых, можно использовать расширенную форму: интерфейс изображается в виде класса со стереотипом, что позволяет визуализировать операции и другие свойства, а также нарисовать связь реализации (для предоставляемого интерфейса) или зависимости (для требуемого интерфейса) от классификатора или компонента к интерфейсу. В UML связь реализации изображается пунктирной линией с большой треугольной стрелкой на конце, указывающей на интерфейс. Эта нотация – нечто среднее между обобщением и зависимостью.

Интерфейсы похожи на абстрактные классы. В частности, ни те, ни другие не могут иметь непосредственных экземпляров. Абстрактный класс, однако, может реализовывать свои конкретные операции. Интерфейс больше напоминает абстрактный класс, у которого абстрактны и все операции.

Первое, что вы видите при работе с интерфейсом, – это набор операций, специфицирующих сервис класса или компонента. Если посмотреть немного глубже, можно выявить полные сигнатуры этих операций наряду с их особыми свойствами, такими как видимость, контекст и семантика параллелизма.

Эти свойства важны, но для сложных интерфейсов их недостаточно, чтобы прояснить семантику предоставляемого ими сервиса и дать понять, как правильно использовать операции. При отсутствии любых других сведений вы должны погрузиться в некую абстракцию, которая реализует интерфейс, чтобы понять, что именно делает каждая операция и как все они должны работать вместе. Однако это лишает смысла использование интерфейса, назначение которого состоит в том, чтобы представлять четкое разделение аспектов в системе.

В модели UML можно указать значительно больше информации, чтобы сделать интерфейс понимаемым и доступным. Во-первых, вы можете сопроводить каждую операцию пред- и постусловиями, а класс или компонент в целом – инвариантами. В результате клиент, желающий использовать интерфейс, сможет понять, что он делает и как его применять, не погружаясь в детали реализации. Если важны формальности, стоит прибегнуть к OCL для спецификации семантики. Во-вторых, можно сопроводить интерфейс конечным автоматом для описания допустимой частичной упорядоченности его операций. В-третьих, сопроводив интерфейс кооперациями, вы определяете его ожидаемое поведение с помощью ряда диаграмм взаимодействия.

[<<Предыдущая страница](/diagram-class/class.md)
[Содержание](/diagram-class/README.md)
[Следующая страница>>](/diagram-class/template.md)