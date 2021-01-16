# Настройки Sublime для работы с текстами

> Я пишу свои тексты в Sublime Text 3.
> https://www.sublimetext.com

## 1. Markdown
- https://www.sitepoint.com/sublime-text-perfect-blogging-6-ways/
- плагин: MarkdownEditing

## 2. Spell check
- https://www.sublimetext.com/docs/3/spell_checking.html
- https://devmag.ru/sublime-text-3-spellcheck/

## 3. Text editor settings
- включить поддержку спеллера
- при авто-переносе строк не выравнивать абзацы по красной строке
    NB: в результате сломаются списки с длинными строками!

## 4. Color schemes and themes
- Theme: Ayu (нужно устанавливать)
- Color Scheme:
    - Ayu — светлая и тёмная (использую для кода)
    - MarkdownEditing — светлая (основная для текста)
        + можно сделать заголовки синими (#0051F3)

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
- Word​Highlight - подсветка всех таких же слов, как то, что под курсором
- Plain Tasks — список задач с чекбоксами
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
    "color_scheme": "Packages/MarkdownEditing/MarkdownEditor.tmTheme",
    "draw_centered": true,
    "font_face": "PT Mono",
    "gutter": false,
    "ignored_packages":
    [
        "Markdown",
        "Vintage"
    ],
    "indent_subsequent_lines": false,
    "indent_to_bracket": true,
    "line_padding_bottom": 4,
    "line_padding_top": 4,
    "scroll_past_end": true,
    "theme": "ayu-light.sublime-theme",
    "word_wrap": true,
    "wrap_width": 80
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
