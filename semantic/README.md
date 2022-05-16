[![Donate](https://img.shields.io/badge/donate-dyaka.com-red?style=plastic)](https://css_notes.dyaka.com/startpack)

# Easy-webdev-startpack

![CodeFactor Grade](https://img.shields.io/codefactor/grade/github/budfy/easy-webdev-startpack?style=plastic) ![GitHub release (latest by date)](https://img.shields.io/github/v/release/budfy/Easy-webdev-startpack?style=plastic) ![GitHub last commit](https://img.shields.io/github/last-commit/budfy/easy-webdev-startpack?style=plastic) ![GitHub Repo stars](https://img.shields.io/github/stars/budfy/Easy-webdev-startpack?style=plastic) ![GitHub forks](https://img.shields.io/github/forks/budfy/Easy-webdev-startpack?style=plastic)

## Сборка Gulp4 с плагинами для разработки вебпроектов.

Вы можете поддержать разработку проекта, перейдя [по ссылке](https://css_notes.diaka.ua/startpack) и оставив мне что-то на кофе.

[![Мануал по работе со сборкой Easy-webdev-startpack](http://joxi.ru/GrqlnQoCRGvenA.png)](http://www.youtube.com/watch?v=_j38UEpskPU "Мануал по работе со сборкой Easy-webdev-startpack")

Смотрите [вики](https://github.com/budfy/Easy-webdev-startpack/wiki) сборки, чтобы узнать, как ею пользоваться правильно. В вики справа есть разделы и они по мере наличия времени и возникновения вопросов дополняются.
![Разделы вики](http://dl3.joxi.net/drive/2020/05/30/0024/1564/1599004/04/b9d9794244.png)

## Что есть в сборке:

- компилятор для препроцессора scss/sass;
- минификация готового css;
- автопрефиксер;
- импорт одних файлов в другие, который позволяет собирать html из модулей;
- babel;
- конвертация шрифтов из ttf вwoff и woff2;
- полуавтоматическое формирование и подключение @font-face;
- для живого обновления страниц - browsersync;
- карта исходников для отображения в браузере, из какого scss взят кусок css;
- сжатие изображений;
- адекватное сжатие png через pngquant;
- сжатие svg;
- создание svg-спрайтов и конвертация svg в background-image;
- конвертация растровых изображений в webp;
- живая перезагрузка при работе с PHP (совместно с openserver);

## Об ошибках, пожалуйста, сообщайте в [ишьюс](https://github.com/budfy/Easy-webdev-startpack/issues). Там же можно оставить свои предложения по функционалу сборки.

index.html - наша главная страничка проекта.
*Данная сборка способна работать с многостраничниками . Чтоб создать новую страничку , достаточно в папке src создать новый html файл ( *пример : portfolio.html) и следом подключить к нему основные компоненты ( такие как _head.html , _scripts.html , _header.html , _footert.html ) .

Все созданные html в папке src копируются в папку build конкатенируясь с компонентами.

Все файлы из папки scss конкатенируются в один и выходят в папке build/src ( style.min.css ) .

Та же история и в папке src/js .

Скинутые изображения в src/images автоматически сжимаются ( если svg и png ) и выходят в папке build/images

2(Дерево файлов)
build - итоговая папка всего вашего проекта.

src - папка , в которой вы работаете.

| components - в сборке присутствует компонентная сборка(импорт html из components в index.html).
*Чтоб импортировать html из components, следует в index.html в нужной вам области (куда вы хотите вставить компонент) написать - @@include('components/имя вашего компонента').

| _header.html - header вашего проекта .
| _head.html - head вашего проекта.
| _footer.html - footer вашего проекта.
| _scripts.html - скрипты вашего проекта.
| fonts - папка с шрифтами вашего проекта ( которые автоматически конвертирются в ttf,woff,woff2).
| images - папка с картинками вашего проекта ( которые автоматически сжимаются *png , svg) .

| js - папка с вашими файлами JavaScript .

| scss - папка с вашими файлами SCSS .

| _fonts.scss - подключаем шрифты ( из папки ../fonts ) .
| _global.scss - глобальные стили для вашего проекта .
| _media.scss - файл с медиа-запросами.
| _vars.scss - файл с переменными .
| style.scss - ваш основной файл со стилями .
