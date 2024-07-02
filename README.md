# CustomViews

Этот проект демонстрирует два Custom View для Android, написанных на Kotlin: **PieChart** и **LineChart**.

## Описание

- **PieChart**: круговая диаграмма, которая отображает пропорциональные данные в виде секторов.
- **LineChart**: линейный график, который показывает данные в виде точек, соединенных линиями.

## Используемые технологии

- **Kotlin**: язык программирования.
- **Canvas API**: для рисования пользовательских графиков.
- **Custom View**: создание настраиваемых компонентов UI.

## Установка

1. Клонируйте репозиторий:
    ```bash
    git clone https://github.com/firkatdavletov/CustomView.git
    ```

2. Перейдите в директорию проекта:
    ```bash
    cd CustomView
    ```

3. Откройте проект в Android Studio.

4. Постройте проект:
    ```bash
    ./gradlew build
    ```

## Использование

### PieChart

1. Добавьте `PieChart` в XML разметку вашего Activity или Fragment:
    ```xml
    <com.yourpackage.PieChartView
        android:id="@+id/pieChart"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"/>
    ```

2. В Kotlin коде настройте данные для `PieChart`:
    ```kotlin
    val pieChart: PieChart = findViewById(R.id.pieChart)
    val data = listOf(
        PieChart.PieSlice("Category 1", 25f, Color.RED),
        PieChart.PieSlice("Category 2", 35f, Color.BLUE),
        PieChart.PieSlice("Category 3", 40f, Color.GREEN)
    )
    pieChart.setData(data)
    ```

### LineChart

1. Добавьте `LineChart` в XML разметку вашего Activity или Fragment:
    ```xml
    <com.yourpackage.LineChartView
        android:id="@+id/lineChart"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"/>
    ```

2. В Kotlin коде настройте данные для `LineChart`:
    ```kotlin
    val lineChart: LineChart = findViewById(R.id.lineChart)
    val data = listOf(
        LineChart.DataPoint(0f, 1f),
        LineChart.DataPoint(1f, 3f),
        LineChart.DataPoint(2f, 2f),
        LineChart.DataPoint(3f, 5f)
    )
    lineChart.setData(data)
    ```

## Roadmap

- Добавить анимации при построении графиков.
- Поддержка пользовательских стилей для графиков.
- Добавить тесты для Custom View.

## Контрибуция

1. Форкните репозиторий.
2. Создайте новую ветку:
    ```bash
    git checkout -b feature-name
    ```
3. Внесите изменения и закоммитьте их:
    ```bash
    git commit -m "Add some feature"
    ```
4. Запушьте изменения в свою ветку:
    ```bash
    git push origin feature-name
    ```
5. Создайте Pull Request.


## Контакты

Если у вас есть вопросы или предложения, пожалуйста, создайте issue или свяжитесь со мной по email: [dr.firkat@ya.ru](mailto:dr.firkat@ya.ru).
