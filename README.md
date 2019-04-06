# Полезные сокращения bash / zsh

*Выбрать язык: [English](README.en.md) :us:*

Пользователи MacOS iTerm 2 должны включить мета-ключ — https://coderwall.com/p/_lmivq

## Схематичное представление: 

![visual cheetsheet](https://github.com/JackPot777/BASH/blob/master/moving_cli.png?raw=true)
____

### Перемещение курсора
| Комбинация клавиш | Значение |
|:----:|:----|
| <kbd>Ctrl</kbd> + <kbd>a</kbd>, <kbd>Home</kbd> | Переместить курсор в начало командной строки |
| <kbd>Ctrl</kbd> + <kbd>e</kbd>, <kbd>End</kbd> | Переместить курсор в конец командной строки |
| <kbd>Ctrl</kbd> + <kbd>f</kbd>, <kbd>→</kbd> | Переход на один символ вперёд (вправо) от курсора |
| <kbd>Ctrl</kbd> + <kbd>b</kbd>, <kbd>←</kbd> | Переход на один символ назад (влево) от курсора |
| <kbd>Alt</kbd> + <kbd>b</kbd>, <kbd>Esc</kbd> + <kbd>b</kbd> | Переместить курсор назад (влево) на одно слово |
| <kbd>Alt</kbd> + <kbd>f</kbd>, <kbd>Esc</kbd> + <kbd>f</kbd> | Переместить курсор вперёд (вправо) на одно слово |
| <kbd>Ctrl</kbd> + <kbd>xx</kbd> | Переход от курсора в начало строки и обратно |

____
### Редактирование строки
| Комбинация клавиш | Значение |
|:----:|:----|
| <kbd>Alt</kbd> + <kbd>?</kbd>, <kbd>Tab</kbd> + <kbd>Tab</kbd> | Автодополнение команды или имени файла |
| <kbd>Ctrl</kbd> + <kbd>u</kbd> | Удалить все символы от курсора до начала командной строки |
| <kbd>Ctrl</kbd> + <kbd>k</kbd> | Удалить все символы от курсора до конца командной строки |
| <kbd>Ctrl</kbd> + <kbd>w</kbd> | Удалить символы от курсора до пробела слева |
| <kbd>Alt</kbd> + <kbd>Backspace</kbd> | Удалить символы от курсора до начала слова |
| <kbd>Alt</kbd> + <kbd>d</kbd>, <kbd>Esc</kbd> + <kbd>d</kbd> | Удалить от курсора до конца слова |
| <kbd>Ctrl</kbd> + <kbd>y</kbd> | Вставить символ, слово или текст, удаленные приведенными выше сочетаниями клавиш |
| <kbd>Alt</kbd> + <kbd>y</kbd> | Смотреть в буфере удаленные слова для вставки. Работает после нажатия <kbd>Ctrl</kbd> + <kbd>y</kbd> |
| <kbd>Ctrl</kbd> + <kbd>h</kbd> | Удалить перед курсором один символ |
| <kbd>Ctrl</kbd> + <kbd>d</kbd> | Удалить под курсором один символ |
| <kbd>Alt</kbd> + <kbd>\\</kbd> | Удалить любое количество пробелов вокруг курсора |
| <kbd>Ctrl</kbd> + <kbd>_</kbd> | Откатить редактирование |
| <kbd>Alt</kbd> + <kbd>r</kbd>, <kbd>Esc</kbd> + <kbd>r</kbd> | Отменить все изменения содержимого строки |
| <kbd>Alt</kbd> + <kbd>c</kbd> | Превращает под курсором букву в заглавную и переводит курсор в конец слова |
| <kbd>Alt</kbd> + <kbd>u</kbd> | Переводит все буквы от курсора и до конца слова в заглавные |
| <kbd>Alt</kbd> + <kbd>l</kbd> | Переводит все буквы от курсора и до конца слова в нижний регистр |
| <kbd>Alt</kbd> + <kbd>t</kbd>, <kbd>Esc</kbd> + <kbd>t</kbd> | Замена текущего слова под курсором на предыдущие слово|
| <kbd>Ctrl</kbd> + <kbd>t</kbd> | Замена символа перед курсором на предыдущий символ |

____
### История команд
| Комбинация клавиш | Значение |
|:----:|:----|
| <kbd>Ctrl</kbd> + <kbd>r</kbd> | Искать команду в истории (эквивалентно: vim ~/.bash_history) |
| <kbd>Ctrl</kbd> + <kbd>g</kbd> | Выйти из режима поиска в истории |
| <kbd>Ctrl</kbd> + <kbd>p</kbd>, <kbd>↑</kbd> | Предыдущая команда в истории |
| <kbd>Ctrl</kbd> + <kbd>n</kbd>, <kbd>↓</kbd> | Следующая команда в истории |
| <kbd>Alt</kbd> + <kbd><</kbd> | Переход к первой команде в буфере истории |
| <kbd>Alt</kbd> + <kbd>.</kbd>, <kbd>Esc</kbd> + <kbd>.</kbd> | Вставить последний аргумент предыдущей команды |
| <kbd>Ctrl</kbd> + <kbd>o</kbd> | Выполняет введённую команду и оставляет её же в командной строке |

____
### Выполнение и вывод на экран
| Комбинация клавиш | Значение |
|:----:|:----|
| <kbd>Ctrl</kbd> + <kbd>l</kbd> | Очистка экрана |
| <kbd>Ctrl</kbd> + <kbd>s</kbd> | Остановить вывод на экран |
| <kbd>Ctrl</kbd> + <kbd>q</kbd> | Возобновить вывод на экран, если он был приостановлен комбинацией <kbd>Ctrl</kbd> + <kbd>s</kbd> |
| <kbd>Ctrl</kbd> + <kbd>c</kbd> | Прервать выполнение текущей команды |
| <kbd>Ctrl</kbd> + <kbd>z</kbd> | Приостановить выполнение текущей команды (для возобновления выполните fg) |
| <kbd>Shift</kbd> + <kbd>Ctrl</kbd> + <kbd>c</kbd> | Копировать в буфер |
| <kbd>Shift</kbd> + <kbd>Ctrl</kbd> + <kbd>v</kbd> | Вставить из буфера |
| <kbd>Ctrl</kbd> + <kbd>d</kbd> | Выйти из командной оболочки Bash |

____
### Управление процессом

### (!)- Расширенная История.

Bash имеет некоторые удобные функции, которые используют `'!'` с командами bash.  
Общая запись `'![event][:word[:modifier[:modifier]...]]'`.  
Вы можете опустить разделитель слов `':'`, если обозначение слова начинается с `'^'`, `'$'`, `'*'`, `'-'`, или `'%'`.  
Если обозначение слова предоставляется без спецификации события, в качестве события используется предыдущая команда.  
После необязательного обозначения слова можно добавить последовательность из одного или нескольких модификаторов, каждому из которых предшествует ':'.

### Выполнение и вывод на экран
<table>
  <tr>
    <th>События</th><th>Значение</th><th>Пример</th>
  </tr>
  <tr>
    <td>!</td>
    <td>Начните подстановку истории, за исключением случаев, когда за ней следует пробел, вкладка, конец строки, ' = ' или ' (’ (когда опция оболочки extglob включена с помощью shopt builtin).</td>
    <td>
      <pre>
      </pre>
    </td>
  </tr>
  <tr>
    <td>!<i>n</i></td>
    <td>Выполнить команду <i><b>n</b></i> с начала истории.</td>
    <td>
      <pre>
      $ history
      1 echo foo bar baz
      2 history
      $ !1
      #Выведет команду сохраненную в истории
      #+ и выполнит ее
      echo foo bar baz
      #Результат выполнения
      foo bar baz
      </pre>
    </td>
  </tr>
  <tr>
    <td>!-<i>n</i></td>
    <td>Выполнить команду <i><b>n</b></i> с конца истории.</td>
    <td>
      <pre>
      $ history
      1 echo foo
      2 echo bar
      3 echo baz
      4 history
      $ !-3
      echo bar
      bar
      </pre>
    </td>
  </tr>
  <tr>
    <td>!!</td>
    <td>Выполнить последнюю команду. Синоним ‘!-1’.</td>
    <td>
      <pre>
      $ echo foo bar baz
      foo bar baz
      $ !!
      echo foo bar baz
      foo bar baz
      </pre>
    </td>
  </tr>
  <tr>
    <td>!<i>string</i></td>
    <td>Выполнить последнюю команду, содержащую в себе <i><b>string</b></i>.</td>
    <td>
      <pre>
      $printf '%s\n' foo
      foo
      $ echo bar
      bar
      $ !pri
      printf '%s\n' foo
      foo
      </pre>
    </td>
  </tr>
  <tr>
    <td>!?<i>string</i>[?]</td>
    <td>Смотрите самые последние команды, содержащие в себе <i><b>string</b></i>. <i><b>?</b></i> в конце может быть опущен, если за <i><b>string</b></i> немедленно следует новая строка.</td>
    <td>
      <pre>
      $printf '%s\n' foo
      foo
      $ echo bar
      bar
      $ !?ntf
      printf '%s\n' foo
      foo
      $ !?bar
      echo bar
      bar
      </pre>
    </td>
  </tr>
  <tr>
    <td>^<i>string1</i>^<i>tring2</i>^</td>
    <td>Быстрая Замена. Повторите последнюю команду, заменив <i><b>string1</b></i> на <i><b>string2</b></i>. Эквивалент `!!:s/string1/string2`.</td>
    <td>
    Дополнительные сведения см. `s/old/new/` в разделе <b>Модификаторы</b>.
      <pre>
      $ echo foo
      foo
      $ ^echo^printf '%s\n'^
      printf '%s\n' foo
      foo
      </pre>
    </td>
  </tr>
  <tr>
    <td>!#</td>
    <td>Повторите всю командную строку перед этим событием.</td>
    <td>
      <pre>
      $ echo foo; echo bar; !#echo baz
      echo foo; echo bar; echo foo; echo bar; echo baz
      foo
      bar
      foo
      bar
      baz
      </pre>
    </td>
  </tr>
  <tr>
    <th>Слово</th><th>Значение</th><th>Пример</th>
  </tr>
  <tr>
    <td>!:0 (zero)</td>
    <td>0-е слово. Для многих приложений, это командное слово.</td>
    <td>
      <pre>
      $ echo foo
      foo
      $ !:0
      echo
      </pre>
    </td>
  </tr>
  <tr>
    <td>!:<i>n</i></td>
    <td><i><b>n</b></i>-е слово.</td>
    <td>
      <pre>
      $ echo foo bar baz
      foo bar baz
      $ echo !:2
      echo bar
      bar
      </pre>
    </td>
  </tr>
  <tr>
    <td>!^</td>
    <td>Первый аргумент; то есть, слово 1.</td>
    <td>
      <pre>
      $ echo foo bar baz
      foo bar baz
      $ echo !^
      echo foo
      foo
      </pre>
    </td>
  </tr>
  <tr>
    <td>!$</td>
    <td>Последний аргумент.</td>
    <td>
      <pre>
      $ echo foo bar baz
      foo bar baz
      $ echo !$
      echo baz
      baz
      </pre>
    </td>
  </tr>
  <tr>
    <td>!%</td>
    <td>Слово совпадает с последним поиском `?string?`</td>
    <td>
      <pre>
      $ echo foo
      foo
      $ printf '%s\n' bar
      bar
      $ !?ch
      echo foo
      foo
      $ !% baz
      echo baz
      baz
      $ !?bar
      printf '%s\n' bar
      bar
      $ echo !%
      echo bar
      bar
      </pre>
    </td>
  </tr>
  <tr>
    <td>!:x-y</td>
    <td>Диапазон слов; `-y` сокращает `0-y`.</td>
    <td>
      <pre>
      $ echo foo bar baz
      foo bar baz
      $ echo !:2-3
      echo bar baz
      bar baz
      $ !:-1
      echo bar
      bar
      </pre>
    </td>
  </tr>
  <tr>
    <td>!*</td>
    <td>Все слова, кроме 0-го. Это синоним `1-$`. Это не ошибка использовать `*`, если в событии есть только одно слово - в этом случае возвращается пустая строка.</td>
    <td>
      <pre>
      $ echo foo bar baz
      foo bar baz
      $ printf '%s\n' !*
      printf '%s\n' foo bar baz
      foo
      bar
      baz
      </pre>
    </td>
  </tr>
  <tr>
    <td>!:x*</td>
    <td>Сокращает `x-$`</td>
    <td>
      <pre>
      $ echo foo bar baz
      foo bar baz
      $ printf '%s\n' !:2*
      printf '%s\n' bar baz
      bar
      baz
      </pre>
    </td>
  </tr>
  <tr>
    <td>!:x-</td>
    <td>Сокращает `x -$`, как `x*`, но опускает последнее слово.</td>
    <td>
      <pre>
      $ echo foo bar baz
      foo bar baz
      $ printf '%s\n' !:0-
      printf '%s\n' echo foo bar
      echo
      foo
      bar
      </pre>
    </td>
  </tr>
  <tr>
    <th>Модификаторы</th><th>Значение</th><th>Пример</th>
  </tr>
  <tr>
    <td>!:p</td>
    <td>Распечатать новую команду, но не выполнять ее.
Распечатанная команда сохраняется в истории, поэтому вы можете использовать <kbd>Ctrl</kbd> + <kbd>p</kbd> для повторного ввода ее в текущем приглашении.</td>
    <td>
      <pre>
      $ echo foo bar baz
      foo bar baz
      $ !:p
      #Printed, but not executed
      echo foo bar baz
      $ !:*:p
      foo bar baz
      </pre>
    </td>
  </tr>
  <tr>
    <td>!:h</td>
    <td>Удалите все в конце пути после последнего `/`, включая последний `/`</td>
    <td>
      <pre>
      $ echo foo /example/path/bar.txt baz
      foo /example/path/bar.txt baz
      $ !:p:h
      echo foo /example/path
      </pre>
    </td>
  </tr>
  <tr>
    <td>!:t</td>
    <td>Удалите все в начале пути до последнего `/`, включая последний `/`</td>
    <td>
      <pre>
      $ echo foo /example/path/bar.txt baz
      foo /example/path/bar.txt baz
      $ !:p:t
      bar.txt baz
      </pre>
    </td>
  </tr>
  <tr>
    <td>!:r</td>
    <td>Удалите все в конце после `.suffix`, включая `.suffix`, оставив только имя.</td>
    <td>
      <pre>
      $ echo foo /example/path/bar.txt baz
      foo /example/path/bar.txt baz
      $ !:p:r
      echo foo /example/path/bar
      </pre>
    </td>
  </tr>
  <tr>
    <td>!:e</td>
    <td>Удалите все в начале до `.suffix`, включая `.`.</td>
    <td>
      <pre>
      $ echo foo /example/path/bar.txt baz
      foo /example/path/bar.txt baz
      $ !:p:e
      txt baz
      </pre>
    </td>
  </tr>
  <tr>
    <td>!:q</td>
    <td>Процитируйте подставленные слова, избегая дальнейших подстановок.</td>
    <td>
      <pre>
      $ echo foo 'bar baz'
      foo bar baz
      $ !:p:q
      'echo foo '\'bar baz'\'''
      </pre>
    </td>
  </tr>
  <tr>
    <td>!:x</td>
    <td>Процитируйте подставленные слова как ‘!:q’, разделив пробелами, табами и новыми строками.</td>
    <td>
      <pre>
      $ echo foo 'bar baz'
      foo bar baz
      $ !:p:x
      'echo' 'foo' ''\'bar' 'baz'\'''
      </pre>
    </td>
  </tr>
  <tr>
    <td><i>s/<i>old</i>/<i>new</i>/</i></td>
    <td>Заменить <i><b>old</b></i> на <i><b>new</b></i> в строке события. Вместо `/` может использоваться любой разделитель. Разделитель может быть экранирован в <i><b>old</b></i> и <i><b>new</b></i> обратным слэшем "\". Если `&` появляется в <i><b>new</b></i>, то заменяет <i><b>old</b></i>. Обратный слэш "\" будет экранироватьь `&`. Конечный разделитель является необязательным, если он является последним символом в строке ввода.</td>
    <td>
      <pre>
      $ echo foo bar
      foo bar
      $ !:p:s/foo/baz
      echo baz bar
      </pre>
    </td>
  </tr>
  <tr>
    <td>!:&</td>
    <td>Повторите предыдущую замену.</td>
    <td>
      <pre>
      $ echo foo bar
      foo bar
      $ !:p:s/foo/baz
      echo baz bar
      $ printf '%s\n' foo
      foo
      $ !:p:&
      printf '%s\n' baz
      </pre>
    </td>
  </tr>
  <tr>
    <td>!:g<br>!:a</td>
    <td>Вызовите изменения, которые будут применяться ко всей строке события. Используется в сочетании с `s`, как в `gs/old/new/`, или с `&`.</td>
    <td>
      <pre>
      $ echo foo bar foo
      foo bar foo
      $ !:p:gs/foo/baz
      echo baz bar baz
      </pre>
    </td>
  </tr>
  <tr>
    <td>G</td>
    <td>Примените модификатор `s` один раз к каждому слову в событии.</td>
    <td>Результат такой же, как в модификаторе `g`</td>
  </tr>
</table>

## Ссылки
* [Bash Shortcuts For Maximum Productivity](http://www.skorks.com/2009/09/bash-shortcuts-for-maximum-productivity/)
* [Syntax Bashkeyboard](http://ss64.com/osx/syntax-bashkeyboard.html)
* [Moving efficiently in the CLI](https://clementc.github.io/blog/2018/01/25/moving_cli/)
* [Bash History Expansion](https://www.gnu.org/software/bash/manual/html_node/History-Interaction.html)
