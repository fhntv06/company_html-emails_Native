# Инструкция верстки писем для рассылки

<blockquote>
  <h4>Примеры работ компаний:</h4>
  <ul>
    <li>Компания <a href="https://dom-a-dom.ru/" target="_blank">Домадом</a>: <a href="https://fhntv06.github.io/company_html-emails_Native/domadom-email/" target="_blank">работа</a></li>
    <li>Компания <a href="https://www.getbrand.ru/" target="_blank">Get Brand</a>: <a href="https://fhntv06.github.io/company_html-emails_Native/getbrand-email/" target="_blank">работа</a></li>
    <li>
      Компания
      <a href="https://optitech.ru/" target="_blank">Optitech</a>: <a href="https://fhntv06.github.io/company_html-emails_Native/optitech-email/email-optitech-new-year/" target="_blank">Новогоднее письмо</a>
      <a href="https://fhntv06.github.io/company_html-emails_Native/optitech-email/email-optitech/" target="_blank">Обычное письмо</a>
    </li>
  </ul>
</blockquote>

## Полезные ссылки с примерами
[Пример](https://fhntv06.github.io/company_html-emails_Native/example.html)
[Youtube](https://www.youtube.com/watch?v=u-jkI19omLo)
[Гит](https://github.com/maxdenaro/maxgraph-youtube-source/blob/master/%D0%92%D0%B5%D1%80%D1%81%D1%82%D0%BA%D0%B0%20HTML-%D0%BF%D0%B8%D1%81%D1%8C%D0%BC%D0%B0%20%D0%B2%202022/index.html)

## Требования к верстке писем
  <ol>
    <li>Письмо не должно превышать <b>102КБ</b>;</li>
    <li>Все стили для элементов пишутся инлайново на элементах;</li>
    <li>Дополнительные стили для классов адаптива или например, темной темы записываются в теге style;</li>
      <blockquote>
        <pre>
.class-adaptive-full {
  width: 100%;
  padding: 20px;
}
        </pre>
      </blockquote>
    <li>Медиа запросы записываются в теге style:
      <blockquote>
        <pre>
@media(max-width: 552px) {
  .class-adaptive-552px {
    width: 50%;
    padding: 10px;
  }
}
        </pre>
      </blockquote>
    </li>
    <li>Не должно быть подключения файлов: <b>js</b> или <b>css</b>;</li>
    <li>Все элементы находящиеся в строке должны оборачиваться в колонки <b>&lt;td&gt;</b>;</li>
    <li>Теги которые не имеют закрывающего тега должны закрываться. Например тег  <b>img</b>.</li>
    <li>
      Обязательно:
      <ul>
        <li>
          прописать для тега &lt;img&gt;
          <ul>
            <li>alt и title</li>
          </ul>
        </li>
      </ul>
      <ul>
        <li>
          прописать для тега &lt;a&gt;
          <ul>
            <li>role</li>
            <li>указывается target="_blank"</li>
          </ul>
        </li>
      </ul>
      <ul>
        <li>
          для каждой таблицы прописывается вид:
          &lt;table border='0' cellspacing='0' cellpadding='0' role='presentation'&gt;&lt;/table&gt;
          <ul>
            <li>role='presentation' - для корректной работы screen reader, чтобы screen reader программы могли корректно читать и поддерживать интерфейсы/li>
        </ul>
      </li>
  </ol>

  <hr>


## Основные теги:
  <ul>
    <li>table</li>
    <li>tr</li>
    <li>td</li>
    <li>thead</li>
    <li>tbody</li>
    <li>p</li>
    <li>span</li>
    <li>heading: h1 h2 h3 и тд</li>
    <li>img</li>
    <li>a</li>
  </ul>

  <hr>


## Адаптивная верстка письма
#### Инлайновость:
  <ul>
    <li>
      при верстке для адаптива можно использовать display inline, для него Обязательно нужно указывать font-size: 0; тк существуют "фантомные" отступы у инлайн элементов
    </li>
  </ul>

  <hr>

## Для OUTLOOK:
  <blockquote>
    обязательное использование конструкций фантомной таблицы:
  </blockquote>

  <blockquote>
    - "фантомная"
    <pre>
      &lt;!-- [if (gte mso 9)|(IE)] --&gt;
        &lt;table border='0' cellspacing='0' cellpadding='0' role='presentation'&gt;&lt;/table&gt;
          &lt;tr&gt;
            &lt;td&gt;
      &lt;![endif]--&gt;
    </pre>
  </blockquote>
  <blockquote>
    <контент>
  </blockquote>
  <blockquote>
    - "обычная"
    <pre>
      &lt;!-- [if (gte mso 9)|(IE)] --&gt;
          &lt;td&gt;
        &lt;tr&gt;
      &lt;/table&gt;
      &lt;![endif]--&gt
    </pre>
  </blockquote>
  <blockquote>
    фантомная таблица будет показана в Outlook, а обычная будет в других почтовиках
  </blockquote>

  <hr>

##### Правила поддерживают почтовики
  <ul>
    <li>
      Apple mail
    </li>
    <li>
      Gmail
    </li>
    <li>
      Outlook
    </li>
    <li>
      Yahoo
    </li>
    <li>
      Mail Почта
    </li>
    <li>
      Yandex Почта
    </li>
    <li>
      Sumsung mail
    </li>
  </ul>
