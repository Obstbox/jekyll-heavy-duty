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

### todo
- вычистить `seo\_tag`,  etc из default.html
- навести порядок в `title` и `description` на страницах
- `permalink` в _about.md_, как же это работает и нужно ли вообще.
- посмотреть официальные туториалы по _jekyll_ на _youtube_
- ~~при 404 верхний заголовок съезжает ниже~~
- для чего в исходном __tactile__ был сделан _print.css_?
- добавить тень и вообще красоту к аватарке
- ~~_h2_ и _a_ слишком похожи друг на друга по стилям~~
- надо как-то покрасивее разместить футер
- может добавить пикчи в сслыках на контакты?



`{{ site.baseurl }}{{ item.link }}` и `{{ item.link | relative_url }}` дают одинаковый результат
`{: style="float: left; margin-right: 1em;"}` стили в __kramdown__
`{: .no-indent}` после абзаца - добавляет к нему класс _no-indent_ в **kramdown**

