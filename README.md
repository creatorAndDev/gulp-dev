# gulp-dev
## NODE last v18
### GULP 4

## List plugins
- "gulp": "^4.0.2",
- "gulp-autoprefixer": "^8.0.0",
- "gulp-changed": "^4.0.2",
- "gulp-clean-css": "^4.3.0",
- "gulp-compile-handlebars": "^0.6.1",
- "gulp-concat": "^2.6.1",
- "gulp-connect": "^5.7.0",
- "gulp-ftp": "^1.1.0",
- "gulp-if": "^3.0.0",
- "gulp-livereload": "^4.0.2",
- "gulp-notify": "^4.0.0",
- "gulp-rename": "^2.0.0",
- "gulp-sass": "^4.1.0"


## markup handelbars

```
{{> header pageTitle="Index"}}
{{#repeat 24}}
	{{> thumb}}
{{/repeat}}
{{> footer}}
```

## Helpers
1. npm i from root folder
2. cd dev
3. open terminal => gulp

## grid thumbs

```
.thumbs-parent {
    --flex-gap: 6px;
    --flex-items: 5;
    display: flex;
    flex-wrap: wrap;
    gap: var(--flex-gap);
}
.thumbs-child {
    width: calc((100% / var(--flex-items)) - (((var(--flex-items) - 1) / var(--flex-items)) * var(--flex-gap)));
    @media screen and (max-width: 991px) {
        --flex-items: 4;
    }
	@media screen and (max-width: 767px) {
        --flex-items: 3;
    }
}
```