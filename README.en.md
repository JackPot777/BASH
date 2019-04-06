# Useful bash / zsh shortcuts

*Select a language: [Russian](README.md) :ru:*

MacOS iTerm 2 users must turn on meta key — https://coderwall.com/p/_lmivq

## Visual cheatsheet: 

![visual cheetsheet](https://github.com/JackPot777/BASH/blob/master/moving_cli.png?raw=true)
____

### Move cursor
| Key combination | Meaning |
|:----:|:----|
| <kbd>Ctrl</kbd> + <kbd>a</kbd>, <kbd>Home</kbd> | Go to the beginning of the line |
| <kbd>Ctrl</kbd> + <kbd>e</kbd>, <kbd>End</kbd> | Go to the End of the line |
| <kbd>Ctrl</kbd> + <kbd>f</kbd>, <kbd>→</kbd> | Forward one character |
| <kbd>Ctrl</kbd> + <kbd>b</kbd>, <kbd>←</kbd> | Backward one character |
| <kbd>Alt</kbd> + <kbd>b</kbd>, <kbd>Esc</kbd> + <kbd>b</kbd> | Forward (right) one word |
| <kbd>Alt</kbd> + <kbd>f</kbd>, <kbd>Esc</kbd> + <kbd>f</kbd> | Back (left) one word |
| <kbd>Ctrl</kbd> + <kbd>xx</kbd> | Toggle between the start of line and current cursor position |

____
### Edit
| Key combination | Meaning |
|:----:|:----|
| <kbd>Alt</kbd> + <kbd>?</kbd>, <kbd>Tab</kbd> + <kbd>Tab</kbd> | Auto-complete command or file name |
| <kbd>Ctrl</kbd> + <kbd>u</kbd> | Cut the line before the cursor position |
| <kbd>Ctrl</kbd> + <kbd>k</kbd> | Cut the Line after the cursor to the clipboard |
| <kbd>Ctrl</kbd> + <kbd>w</kbd> | Cut the Word before the cursor to the clipboard |
| <kbd>Alt</kbd> + <kbd>Backspace</kbd> | Remove characters from cursor to beginning of word |
| <kbd>Alt</kbd> + <kbd>d</kbd>, <kbd>Esc</kbd> + <kbd>d</kbd> | Remove from cursor to end of word |
| <kbd>Ctrl</kbd> + <kbd>y</kbd> | Insert a character, word, or text that has been removed by the above keyboard shortcuts |
| <kbd>Alt</kbd> + <kbd>y</kbd> | Look in the buffer for deleted words to paste. Works after pressing <kbd>Ctrl</kbd> + <kbd>y</kbd> |
| <kbd>Ctrl</kbd> + <kbd>h</kbd> | Delete one character before the cursor |
| <kbd>Ctrl</kbd> + <kbd>d</kbd> | Delete character under the cursor |
| <kbd>Alt</kbd> + <kbd>\\</kbd> | Remove any number of spaces around the cursor |
| <kbd>Ctrl</kbd> + <kbd>_</kbd> | Undo |
| <kbd>Alt</kbd> + <kbd>r</kbd>, <kbd>Esc</kbd> + <kbd>r</kbd> | Cancel the changes and put back the line as it was in the history |
| <kbd>Alt</kbd> + <kbd>c</kbd> | Capitalize the character under the cursor and move to the end of the word |
| <kbd>Alt</kbd> + <kbd>u</kbd> | UPPER capitalize every character from the cursor to the end of the current word |
| <kbd>Alt</kbd> + <kbd>l</kbd> | Lower the case of every character from the cursor to the end of the current word |
| <kbd>Alt</kbd> + <kbd>t</kbd>, <kbd>Esc</kbd> + <kbd>t</kbd> | Swap current word with previous|
| <kbd>Ctrl</kbd> + <kbd>t</kbd> | Swap the last two characters before the cursor |

____
### History
| Key combination | Meaning |
|:----:|:----|
| <kbd>Ctrl</kbd> + <kbd>r</kbd> | Recall the last command including the specified character(s)(equivalent to : vim ~/.bash_history) |
| <kbd>Ctrl</kbd> + <kbd>g</kbd> | Escape from history searching mode |
| <kbd>Ctrl</kbd> + <kbd>p</kbd>, <kbd>↑</kbd> | Previous command in history (i.e. walk back through the command history) |
| <kbd>Ctrl</kbd> + <kbd>n</kbd>, <kbd>↓</kbd> | Next command in history (i.e. walk forward through the command history) |
| <kbd>Alt</kbd> + <kbd><</kbd> | Go to the first command in the history buffer |
| <kbd>Alt</kbd> + <kbd>.</kbd>, <kbd>Esc</kbd> + <kbd>.</kbd> | Use the last word of the previous command |
| <kbd>Ctrl</kbd> + <kbd>o</kbd> | Executes the entered command and leaves it in the command line |

____
### Execution and display
| Key combination | Meaning |
|:----:|:----|
| <kbd>Ctrl</kbd> + <kbd>l</kbd> | Clear the screen |
| <kbd>Ctrl</kbd> + <kbd>s</kbd> | To stop output to the screen |
| <kbd>Ctrl</kbd> + <kbd>q</kbd> | To resume output to the screen if it were suspended by a combination of <kbd>Ctrl</kbd> + <kbd>s</kbd> |
| <kbd>Ctrl</kbd> + <kbd>c</kbd> | Abort the current command |
| <kbd>Ctrl</kbd> + <kbd>z</kbd> | To suspend the execution of the current command (resume, run fg) |
| <kbd>Shift</kbd> + <kbd>Ctrl</kbd> + <kbd>c</kbd> | Copy to clipboard |
| <kbd>Shift</kbd> + <kbd>Ctrl</kbd> + <kbd>v</kbd> | Paste from clipboard |
| <kbd>Ctrl</kbd> + <kbd>d</kbd> | Exit the command shell Bash |

____
### Process control

### Bang(!) - The History Expansion
Bash also has some handy features that use the ! (bang) to allow you to do some funky stuff with bash commands.<br>
General notation is `'![event][:word[:modifier[:modifier]...]]'`.<br>
You may ommit word separator `':'`, if the word designator begins with a `'^'`, `'$'`, `'*'`, `'-'`, or `'%'`.<br>
If a word designator is supplied without an event specification, the previous command is used as the event.<br>
After the optional word designator, you can add a sequence of one or more modifiers, each preceded by a `':'`.<br>

<table>
  <tr>
    <th>Events</th><th>Meaning</th><th>Example</th>
  </tr>
  <tr>
    <td>!</td>
    <td>Start a history substitution, except when followed by a space, tab, the end of the line, ‘=’ or ‘(’ (when the extglob shell option is enabled using the shopt builtin).</td>
    <td>
      <pre>
      </pre>
    </td>
  </tr>
  <tr>
    <td>!<i>n</i></td>
    <td>Refer to command line <i><b>n</b></i>.</td>
    <td>
      <pre>
      $ history
      1 echo foo bar baz
      2 history
      $ !1
      #Print command that will be saved in history
      #+and executed
      echo foo bar baz
      #Actual execution
      foo bar baz
      </pre>
    </td>
  </tr>
  <tr>
    <td>!-<i>n</i></td>
    <td>Refer to the command <i><b>n</b></i> lines back.</td>
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
    <td>Refer to the previous command. This is a synonym for ‘!-1’.</td>
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
    <td>Refer to the most recent command preceding the current position in the history list starting with <i><b>string</b></i>.</td>
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
    <td>Refer to the most recent command preceding the current position in the history list containing <i><b>string</b></i>. The trailing ‘?’ may be omitted if the <i><b>string</b></i> is followed immediately by a newline.</td>
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
    <td>Quick Substitution. Repeat the last command, replacing <i><b>string1</b></i> with <i><b>string2</b></i>. Equivalent to `!!:s/string1/string2`.</td>
    <td>
    For more info, refer to `s/old/new/` in <b>Modifiers</b> section.
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
    <td>Repeat entire command line before this event.</td>
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
    <th>Words</th><th>Meaning</th><th>Example</th>
  </tr>
  <tr>
    <td>!:0 (zero)</td>
    <td>The 0th word. For many applications, this is the command word.</td>
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
    <td>The <i><b>n</b></i>th word.</td>
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
    <td>!:^</td>
    <td>The first argument; that is, word 1.</td>
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
    <td>!:$</td>
    <td>The last argument.</td>
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
    <td>!:%</td>
    <td>The word matched by the most recent `?string?` search</td>
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
    <td>A range of words; `-y` abbreviates `0-y`.</td>
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
    <td>!:*</td>
    <td>All of the words, except the 0th. This is a synonym for `1-$`. It is not an error to use `*` if there is just one word in the event - the empty string is returned in that case.</td>
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
    <td>Abbreviates `x-$`</td>
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
    <td>Abbreviates `x-$` like `x*`, but omits the last word.</td>
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
    <th>Modifiers</th><th>Meaning</th><th>Example</th>
  </tr>
  <tr>
    <td>!:p</td>
    <td>Print the new command but do not execute it.<br>Printed command is saved in history, so you can use <kbd>Ctrl</kbd> + <kbd>p</kbd> to re-enter it in current prompt.</td>
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
    <td>Remove a trailing pathname component, leaving only the head (Actually, remove all after last `/`, including).</td>
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
    <td>Remove all leading pathname components, leaving the tail (Actually, remove all before last `/`, including).</td>
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
    <td>Remove a trailing suffix of the form `.suffix`, leaving the basename (Actually, remove all after last `.`, including).</td>
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
    <td>Remove all but the trailing suffix (Actually, remove all before last `.`, including).</td>
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
    <td>Quote the substituted words, escaping further substitutions.</td>
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
    <td>Quote the substituted words as with ‘q’, but break into words at spaces, tabs, and newlines.</td>
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
    <td>Substitute <i><b>new</b></i> for the first occurrence of <i><b>old</b></i> in the event line. Any delimiter may be used in place of `/`. The delimiter may be quoted in <i><b>old</b></i> and <i><b>new</b></i> with a single backslash. If `&` appears in <i><b>new</b></i>, it is replaced by <i><b>old</b></i>. A single backslash will quote the `&`. The final delimiter is optional if it is the last character on the input line.</td>
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
    <td>Repeat the previous substitution.</td>
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
    <td>Cause changes to be applied over the entire event line. Used in conjunction with `s`, as in gs/old/new/, or with `&`.</td>
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
    <td>Apply the following ‘s’ modifier once to each word in the event.</td>
    <td>Result is same as in `g` modifier
<pre>
</pre>
    </td>
  </tr>
</table>

## Recent links
* [Bash Shortcuts For Maximum Productivity](http://www.skorks.com/2009/09/bash-shortcuts-for-maximum-productivity/)
* [Syntax Bashkeyboard](http://ss64.com/osx/syntax-bashkeyboard.html)
* [Moving efficiently in the CLI](https://clementc.github.io/blog/2018/01/25/moving_cli/)
* [Bash History Expansion](https://www.gnu.org/software/bash/manual/html_node/History-Interaction.html)
