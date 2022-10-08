# gulp-tgs

Uncompress [tgs](https://core.telegram.org/stickers) files in your [gulp](http://gulpjs.com) build pipeline

## Install

```bash
$ npm install --save-dev gulp-tgs
```

## Usage

```js
const gulp = require('gulp')
const gunzip = require('gulp-gunzip')
const rename = require('gulp-rename')

gulp.task("lottie", function () {
    return gulp.src("./tgs/*.tgs")
        .pipe(gunzip())
        .pipe(rename(function (path) {
            path.extname = ".json";
        }))
        .pipe(gulp.dest("./lottie"));
});
```

## License

[MIT](http://opensource.org/licenses/MIT)
