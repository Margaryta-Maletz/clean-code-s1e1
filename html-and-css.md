<h1>Задача "Чистый код S1E1"</h1>
<p> Задача - навести порядок внутри файлов кода (рефакторинг) согласно следующим руководствам: начальный и продвинутый уровни. При этом функционал приложения должен остаться рабочим после изменений.</p>
<h2>Начальный уровень:</h2>
<h3>1. Общие правила для HTML + CSS</h3>
<h4>1.1 Отступы</h4>
<p>Всегда используйте для одного отступа два пробела. Не используйте табуляцию (tab-символ) для отступов и не смешивайте виды отступов (tab и пробелы одновременно).</p>

```
<ul>
  <li>Fantastic
  <li>Great
</ul>

.example {
  color: blue;
}
```

<h4>1.2 Нижний регистр написания</h4>
<p>Весь код должен быть в нижнем регистре. Это касается всех HTML-имен, включая названия атрибутов, значения атрибутов, CSS-селекторы, CSS-свойства и их значения.</p>

```
<!-- Not recommended -->
<A HREF="/">Home</A>

<!-- Recommended -->
<img src="google.png" alt="Google">

/* Not recommended */
color: #E5E5E5 ;

/* Recommended */
color: #e5e5e5 ;
```

<h4>1.3 Кавычки в HTML/CSS документе</h4>
<p>Используйте двойные кавычки вместо одинарных для задания значений атрибутов и CSS свойств.</p>

```
<!-- Not recommended -->
<a class='main-button main-button-secondary'>Sign in</a>

<!-- Recommended -->
<a class="main-button main-button-secondary">Sign in</a>
```

<h3>2. HTML</h3>
<h4>2.1 Форматирование</h4>
<p>Выделяйте новую строку для каждого блочного, табличного или списочного элемента, независимо от заданных для них стилей. И ставьте отступы для каждого вложенного элемента, соблюдая таким образом лестницу вложенности.</p>
<p>Примеры:</p>
<p>Элемент <code>&lt;em&gt;</code> - строчный, потому его можно не переносить. Он используется для выделения подстроки в параграфе. В то время как блочный <code>&lt;p&gt;</code> обязательно нужно перенести на новую строку.</p>

```
<blockquote>
  <p><em>Space</em>, the final frontier.</p>
</blockquote>
```

<p>Списочные элементы:</p>

```
<ul>
    <li>Маша</li>
    <li>Глаша</li>
    <li>Чебураша</li>
</ul>
```

<p>Табличные элементы:</p>

```
<table>
   <thead>
     <tr>
        <th scope="col">Прибыль</th>
        <th scope="col">Налоги</th>
     <tr>
   </thead>
   <tbody>
      <tr>
        <td>$ 5.00</td>
        <td>$ 4.50</td>
      <tr>
   </tbody>
</table>
```

<h4>2.2 Тип документа / Document Type</h4>
<p>Используйте HTML5.</p
<p>HTML5 рекомендуется для всех видов HTML-документов и обозначается первым тегом в HTML документе: <code>&lt;!DOCTYPE html&gt;</code></p>
<h4>2.3 Символы-мнемоники</h4>
<p>Не используйте символы-мнемоники.</p>

Нет смысла использовать мнемоники, такие как ```&mdash;(—)```, ```&rdquo;(”)``` или ```&#x263a;(☺)```, когда все команды в файлах, редакторах используют одну кодировку (UTF-8)

<p>Единственное исключение из этого правила — служебные символы HTML (например < и &), а так же вспомогательные и “невидимые” символы (например неразрывный пробел).</p>

```
<!-- Not recommended -->
<div>Валютный знак евро: &ldquo;&eur;&rdquo;.</div>
 
 <!--  Recommended -->
<div>Валютный знак евро: “€”. </div>
```

<h4>2.4 Атрибут 'type'</h4>
<p>Не используйте атрибут type при подключении стилей (кроме вариантов когда используется что-то кроме CSS) и скриптов (кроме вариантов когда это не JavaScript).</p>

```
<!--  Not recommended -->
<link rel="stylesheet" href="//www.google.com/css/main.css"
  type="text/css">

<!--  Recommended -->
<link rel="stylesheet" href="//www.google.com/css/main.css">

<!--  Not recommended -->
<script src="//www.google.com/js/gweb/analytics/autotrack.js"
  type="text/javascript"></script>

<!--  Recommended -->
<script src="//www.google.com/js/gweb/analytics/autotrack.js"></script>
```

<p>Опциональные рекомендации:</p>
<h4>2.5 HTML Line-Wrapping</h4>
<p>Разбивайте длинные строки на несколько.</p>
<p>Разбиение длинного текста на несколько строк может значительно улучшить читаемость кода.</p>
<p>При разбиении строк рекомендуется перед каждой перенесенной строкой от начальной поставить отступ хотя бы в 4 пробела.</p>
<p>Примеры:</p>

```
<md-progress-circular md-mode="indeterminate" class="md-accent"
    ng-show="ctrl.loading"md-diameter="35">
</md-progress-circular>
<md-progress-circular
    md-mode="indeterminate"
    class="md-accent"
    ng-show="ctrl.loading"
    md-diameter="35">
</md-progress-circular>
<md-progress-circular md-mode="indeterminate"
                      class="md-accent"
                      ng-show="ctrl.loading"
                      md-diameter="35">
</md-progress-circular>
```

<h3>3. CSS</h3>
<h4>3.1 Единый стиль именования селекторов (классов / id)</h4>
<p>Какой бы стиль написания имен вы не выбрали, соблюдайте его во всем проекте.</p>
<p>Если вы используете БЭМ, придерживайтесь этой нотации без исключения.</p>
<p>Иначе рекомендуется использовать дефис для разделения слов в селекторах и прописание их в нижнем регистре, при этом все слова в селекторе обязательно должны быть отделены.</p>
<p>Подробнее о БЭМ</p>

```
/* Не рекомендуется: слова “demo” и “image” не разделены */
.demoimage {}
  
/* Не рекомендуется: используется подчеркивание вместо дефиса */
.error_status {}

/* Рекомендуется */
#video-id {}
.ads-sample {}

/* Рекомендуется в случае использования БЭМ */
.search-form__button {}
```

<h4>3.2 Значимые названия идентификаторов и классов:</h4>
<p>Используйте шаблонные или осмысленные имена классов и идентификаторы.</p>
<p>Вместо использования шифров, или описания внешнего вида элемента, попробуйте в имени класса или идентификатора выразить смысл его создания, или дайте ему шаблонное имя…</p>
<p>рекомендуется выбирать имена, отражающие сущность класса, потому что их проще понять и, скорее всего, не понадобится менять в будущем.</p>
<p>Шаблонные имена — это просто вариант названия для элементов, у которых нет специального предназначения или которые не отличаются от своих братьев и сестер. Обычно они необходимы в качестве “Помощников”.</p>
<p>Использование функциональных или шаблонных имен уменьшает необходимость ненужных изменений в документа или шаблонах.</p>

```
/* Не рекомендуется: не имеет смысла */
  #yee-1901 {}
  
/* Не рекомендуется: описание внешнего вида */
  .button-green {}
  .clear {}
  
/* Рекомендуется: точно и по делу */
  #gallery {}
  #login {}
  .video {}
  
/* Рекомендуется: шаблонное имя */
  .clearfix {}
  .alt {}
```

<h4>3.3 Лаконичность названий идентификаторов и классов</h4>
<p>Для идентификаторов и классов используйте настолько длинные имена, насколько нужно, но настолько короткие, насколько возможно.</p>
<p>Попробуйте сформулировать, что именно должен делать данный элемент, при этом будьте кратки насколько возможно.</p>
<p>Такое использование классов и идентификаторов вносит свой вклад в облегчение понимания и увеличение эффективности кода.</p>

```
  /* Не рекомендуется */
  #navigation {}
  .atr {}
  /* Рекомендуется */
  #nav {}
  .author {}
```

<h4>3.4 Теговые селекторы</h4>
<p>Не используйте теговые селекторы (за исключением намеренного сброса дефолтных стилей).</p>
<p>Это повышает производительность при применении стилей браузером. Подробнее о этом</p>
<p>К тому же, возможно, в будущем вы захотите изменить используемый тег на какой-то другой, в таком случае вам придется отследить все места использования данного тега в стилях и поправить на новый, в то время как использование классов / id помогает абстрагировать ваши стили от деталей вашей html-верстки.</p>

```
  /* Не рекомендуется */
  body {}
  ul#example {}
  div.error {}

  /* Рекомендуется */
  .page {}
  #example {}
  .error {}
```

<h4>3.5 Отступы в блоках.</h4>
<p>Всегда ставьте отступы для содержимого блоков.</p>
<p>Всегда ставьте отступы для любого содержимого в блоке (блоки разделены фигурными скобками {}). Например для правил внутри правил или объявлений, чтобы отобразить иерархию и облегчить понимание кода.</p>

```
@media screen, projection {
  
  html {
    background: #fff;
    color: #444;
  }
    
}
```

<h4>3.6 Пробел после названий свойств</h4>
<p>Используйте пробелы после двоеточий в объявлениях.</p>
<p>Всегда используйте один пробел после двоеточия (но не до) в объявлениях, для порядка в коде.</p>

```
/* Not recommended */
  h3 {
    font-weight:bold;
  }

/* Recommended */
  h3 {
    font-weight: bold;
  }
```  

<h4>3.7 Точка с запятной после свойств</h4>
<p>Ставьте точку с запятой после каждого свойства.</p>
<p>После каждого объявления ставьте точку с запятой для согласованности кода и облегчения добавления новых свойств.</p>

```
/* Not recommended */
.test {
    display: block;
    height: 100px
}

/* Recommended */
.test {
    display: block;
    height: 100px;
}
``` 

<h4>3.8 Разделение селекторов и свойств</h4>
<p>Отделяйте селекторы и свойства переносом строки.</p>
<p>Начинайте каждый селектор или правило с новой строки.</p>

```
/* Not recommended */
  a:focus, a:active {
    position: relative; top: 1px;
  }

/* Recommended */
  h1,
  h2,
  h3 {
    font-weight: normal;
    line-height: 3.2;
  }
```  

<h2>Продвинутый уровень:</h2>
<h3>1. HTML</h3>
<h4>1.1 Семантика</h4>
<p>Используйте HTML так, как это было задумано.</p>
<p>Используйте теги по их прямому назначению: заголовки для заголовков, <p> для абзацев, <a> для ссылок и т.д. Помимо <div>-ов для блоков вам можно и нужно ознакомиться и применять такие элементы <code>&lt;aside>&gt;</code>, <code>&lt;section&gt;</code>, <code>&lt;article&gt;</code>.</p>
<p>Это облегчает чтение, редактирование и поддержку кода.</p>
<p>Также, если ваш сайт будет открываться на электронной книге, то семантические теги помогут парсеру разобрать элементы вашей страницы на компоненты согласно их назначению и правильно отобразить пользователю.</p>
<p>Так вы заботитесь о всех-всех пользователях: если страница открывается в браузере в режиме чтения для слабовидящих людей, специальный робот будет озвучивать читателю каждый элемент, чтобы помочь распознать контент страницы. Этот робот полагается на добросовестное использование семантических тегов. В противном случае, читатель не сможет сориентироваться на вашем сайте. (подробнее: Accessibility)</p>
<p>Поисковые системы google, yandex, bing, используют семантические теги как ключевые слова, с помощью которых они лучше распознают внутреннее содержимое страницы, и потому ранжируют такие страницы выше в результатах поиска. Чем выше ваша страница ранжируется в поисковом запросе - тем больше пользователей ее посетят. Еще о SEO</p>

```
<!-- Not recommended -->
<div onclick="goToRecommendations();">
    All recommendations
</div>

<!-- Recommended -->
<a href="recommendations/">
    All recommendations
</a>
```

<h4>1.2 Альтернатива для мультимедиа</h4>
<p>Всегда указывайте альтернативное содержимое для мультимедиа.</p>
<p>Постарайтесь указать альтернативное содержимое для мультимедиа: например для картинок, видео или анимаций, заданных с помощью canvas.</p>
<p>Для картинок - это осмысленный альтернативный текст (alt), а для видео и аудио - расшифровки текста и подписи, если это возможно.</p>
<p>Note! Если для картинки alt избыточен, или она используется только в декоративных целях в местах, где нельзя использовать CSS, используйте пустой альтернативный текст alt="".</p>
<p>Атрибут alt невероятно полезен для доступности: программы чтения с экрана читают это описание своим слабовидящим пользователям, чтобы дать им знать, что отображено на странице.</p>
<p>Это же описание используется поисковиками (Google, Yandex) для определения их содержания и отображения в результатах своего поиска. Таким образом, это еще один способ увеличить число пользователей вашей страницы.</p>
<p>К тому же описание из "alt" отображается на странице, если изображение не может быть загружено по какой-либо причине: плохое соединение, блокировка контента или ссылка на ресурс поломана.</p>

```
<!-- Not recommended -->
<img src="spreadsheet.png">

<!-- Recommended -->
<img src="spreadsheet.png" alt="Spreadsheet screenshot">

Файл субтитров добавляется с помощью <track> - элемента:
<video preload="auto" width="480" height="360" poster="cute-kitten-video.jpg">
  <source type="video/mp4" src="cute-kitten-video.mp4"/>
  <source type="video/webm" src="cute-kitten-video.webm"/>
  <track kind="captions" src="video-captions.vtt"/>
</video>
```

<h3>2. CSS</h3>
<h4>2.1 БЭМ</h4>
<p>Используйте БЭМ нотация для формирования имен классов.</p>
<p>БЭМ (Блок, Элемент, Модификатор) — компонентный подход к веб-разработке. В его основе лежит принцип разделения интерфейса на независимые блоки. Он позволяет легко и быстро разрабатывать интерфейсы любой сложности и повторно использовать существующий код, избегая «Copy-Paste».</p>
<p>БЭМ берет свое начало в компании Яндекс, однако распространился далеко за ее пределы.</p>
<p>В кратце в основе БЭМ лежит идея разделения любой интерфейс на блоки. Неотделимые части блоков — элементы. У тех и других есть модификаторы.</p>

```
<ul class="menu">
  <li class="
    menu__item">
  </li>
  <li class="
    menu__item
    menu__item_active">
  </li>
</ul>
```

<p>Например, блок меню сайта. Оно может быть в шапке и в боковой части сайта — значит, это блок. В нём есть обязательные части: элементы списка меню, заголовок — это его элементы. Если какой-то элемент меню является активным, то ему даётся модификатор.</p>
