# Настройки Sublime для работы с текстами

> Я пишу свои тексты в Sublime Text 3.
> https://www.sublimetext.com

## 1. Markdown
- https://www.sitepoint.com/sublime-text-perfect-blogging-6-ways/
- плагин: MarkdownEditing

## 2. Spell check
- https://www.sublimetext.com/docs/3/spell_checking.html
- https://github.com/titoBouzout/Dictionaries (Ru-Eng.*)

## 3. Text editor settings
- включить поддержку спеллера
- при авто-переносе строк не выравнивать абзацы по красной строке
    NB: в результате сломаются списки с длинными строками!

## 4. Color schemes and themes
- Theme: Ayu (нужно устанавливать)
- Color Scheme:
    - Ayu — светлая и тёмная (использую для кода)
    - MarkdownEditing — светлая (основная для текста)
        + можно сделать заголовки синими — см. `sublime-color-scheme` внизу.

## 5. Monospace Fonts
- https://www.creativebloq.com/features/the-best-monospace-fonts-for-coding
    + https://input.fontbureau.com/ — бесплатный для личного пользования
    + https://sourcefoundry.org/hack/ — тоже
- https://www.marksimonson.com/fonts/view/anonymous-pro
- https://fonts.google.com/specimen/PT+Mono — мой любимый

## 6. Полезные плагины
Все они устанавливаются через Package Control, с которого и нужно начать установку. Cmd+Shift+P (Ctrl+Shift+P) -> Install Package

- Sidebar Enchantments — больше возможностей боковой панели
- A File Icon (v.3) — иконки в левой панели
- WordCount - считать количество слов и символов
    + символы включаются в настройках
    + https://github.com/titoBouzout/WordCount (почему-то пропал из Install Package)
- Word​Highlight - подсветка всех таких же слов, как то, что под курсором
- PackageResourceViewer - чтобы править темы (менять цвет заголовков)
- Insert Unicode Character — вставлять красивые символы
- OpenURI — чтобы ссылки легче открывать

## Markdown.sublime-settings
```
{
    "spell_check": true,
    "translate_tabs_to_spaces": true,
    "dictionary": "Packages/User/Russian-English Bilingual.dic",
    "fallback_encoding": "Cyrillic (Windows 1251)",
    "draw_centered": true,
    "font_face": "PT Mono",
    "gutter": false,
    "indent_subsequent_lines": false,
    "draw_unicode_white_space": "none",
    "color_scheme": "MarkdownEditor.sublime-color-scheme",
    "indent_to_bracket": true,
    "line_padding_bottom": 4,
    "line_padding_top": 4,
    "scroll_past_end": true,
    "word_wrap": true,
    "wrap_width": 80,
    "font_size": 14,
    "file_exclude_patterns": [ ".DS_Store" ],
    "word_separators": "./\\()\"'-:,.;<>~!@#$%^&*|+=[]{}`~? ’‘「」",
}
```

## MarkdownEditor.sublime-color-scheme
```
{
    "rules":
    [
        {
            "name": "Markdown: Headings",
            "scope": "entity.name.section.markdown, punctuation.definition.heading.begin.markdown, punctuation.definition.heading.end.markdown",
            "foreground": "#0051F3",
            "font_style": "bold",
        },
    ]
}
```
      
## Прочие плагины
Они не имеют прямого отношения к тексту. Я использую их для других своих проектов.

- TypeScript
    - Completions
    - Syntax
    - Linter
- Python
    - Python 3 package
    - Linter
- Web development
    - LiveReload
    - ColorHighlighter
    - Emmet

## Неожиданности и вопросы

### Как сделать красивую красную строку?
Просто — никак. Но мы же русские витязи.
Нужно вставлять неразрывные пробелы.

На маке это `Alt-Space`.
Я думаю пять пробелов — самое то.

Ну и, конечно, в конфиг-файле (уже написано):
```
    "indent_subsequent_lines": false,
    "draw_unicode_white_space": "none",
```

Ещё можно сделать shortcut через `Preferences > Key Bindings`, вот так:
```
[
    { 
        "keys": ["shift+tab"], 
        "command": "insert", 
        "args": {"characters": "     "} 
     },
]
```

Только убедитесь, что пробелы неразрывные.
При копировании из веб-интерфейса Github они становятся обычными.
Вот отсюда можно взять:
https://unicode.flopp.net/c/00A0
