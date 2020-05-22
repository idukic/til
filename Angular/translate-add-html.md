# Add HTML to translation strings

## 1. Include HTML tags
Text:
```
"text": "<h2>Test Title</h2><p>Let's test <strong>strong</strong>, <u>underline</u> and <i>italic</i>.</p>"
```
HTML
```html
<div [innerHtml]="'test.html' | translate"></div>
```

## 2. Include HTML tags and parameter
Text:
```
"text": "<p>Let's test name parameter: <strong>{{name}}</strong>.</p>"
```
HTML
```html
<div [innerHtml]="'text' | translate: {name: 'Moby Dick'}"></div>
```