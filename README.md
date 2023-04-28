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
