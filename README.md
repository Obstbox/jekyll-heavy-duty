# jekyll-heavy-duty
a may be _24th_ or _37th_ try to manage it...

## прочие комментарии

### jekyll themes
победить темы красиво и с использованием инструкций _github pages_ так и не получилось. поэтому оставил тему по умолчанию
__minima__. также стащил стили у [tactile](https://github.com/pages-themes/tactile)


### про отладку
чтобы переключаться между _github pages_ и _локальной отладкой jekyll'а_, нужно в `Gemfile` раскомментировать
соответствующую строку (они взаимоисключающие):
- gem "jekyll"
- gem "github-pages"


### разделы
когда достаточно разберусь с html/css надо будет сделать в панели навигации
_главная_
_блог_
_обо мне_

а это в боковой панели. 
заметки
js demo
резюме
ЛФК
рыжий кот
разные фотки


### todo
- навести порядок в `title` и `description` на страницах
- `permalink` в _about.md_, как же это работает и нужно ли вообще.
- посмотреть официальные туториалы по _jekyll_ на _youtube_
- для чего в исходном __tactile__ был сделан _print.css_?
- навести порядок в стилях, разнести _tactile_ и собственные настройки, вообще прокачать __scss__
- добавить тень и вообще красоту к аватарке
- надо как-то покрасивее разместить футер (подсмотреть в _minima_)
- _вернуться обратно_ не работает с мобильного Brave
- pagination (какие-то там сложности html VS markdown)
- **next** / **prev** [post] (https://guypursey.com/blog/202104171135-next-previous-nav-links-jekyll-blog)

### плагины
[список 1](https://github.com/planetjekyll/awesome-jekyll-plugins)
[список 2](https://planetjekyll.github.io/plugins/top)

- [поиск](https://github.com/algolia/jekyll-algolia)  **deprecated**
- [tag cloud](https://github.com/pattex/jekyll-tagging)
- [paginate v2](https://github.com/sverrirs/jekyll-paginate-v2)

- admin
- pictures


`{{ site.baseurl }}{{ item.link }}` и `{{ item.link | relative_url }}` дают одинаковый результат
`{: style="float: left; margin-right: 1em;"}` стили в __kramdown__
`{: .no-indent}` после абзаца - добавляет к нему класс _no-indent_ в **kramdown**

