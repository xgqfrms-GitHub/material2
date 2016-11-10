# 定制你 Angular 2 Material 2应用程序的主题


### 什么是主题？

一个**主题** 是一组将应用于Angular Material组件的颜色。  
库对主题的方法是基于[材料设计规范][1]的指导。

材料设计的颜色灵感来自大胆的色调与静音环境，深阴影和明亮的亮点并列。

在Angular Material中，通过组合多个调色板创建一个主题。  
  尤其是，一个主题包括：  
* A primary palette: colors most widely used across all screens and components.
* An accent palette: colors used for the floating action button and interactive elements.
* A warn palette: colors used to convey error state.
* A foreground palette: colors for text and icons.
* A background palette: colors used for element backgrounds.

在Angular Material 2中, 所有主题样式都是在构建时生成_statically_，以便你的应用程序不必在启动时花费周期生成主题样式。


[1]: https://material.google.com/style/color.html#color-color-palette

### 使用一个预构建的主题
Angular Material comes prepackaged with several pre-built theme css files. These theme files also
include all of the styles for core (styles common to all components), so you only have to include a
single css file for Angular Material in your app.

你可以直接将主题文件包含到你的应用程序中,从  

`@angular/material/core/theming/prebuilt`

如果你在使用 Angular CLI, 这就像在你的`style.css`文件中,包含一行一样简单 ：  
```css
@import '~@angular/material/core/theming/prebuilt/deeppurple-amber.css';
```

或者，你可以直接引用文件。 这看起来会像  
```html
<link href="node_modules/@angular/material/core/theming/prebuilt/indigo-pink.css" rel="stylesheet">
```
实际路径将取决于您的服务器设置。

你还可以将文件与你的应用程序的的其余部分css文件连接。 

### 定义一个自定义的主题
When you want more customization than a pre-built theme offers, you can create your own theme file.

A theme file is a simple Sass file that defines your palettes and passes them to mixins that output
the corresponding styles. A typical theme file will look something like this:
```scss
@import '~@angular/material/core/theming/all-theme';
// Plus imports for other components in your app.

// Include the base styles for Angular Material core. We include this here so that you only
// have to load a single css file for Angular Material in your app.
@include md-core();

// Define the palettes for your theme using the Material Design palettes available in palette.scss
// (imported above). For each palette, you can optionally specify a default, lighter, and darker
// hue.
$candy-app-primary: md-palette($md-indigo);
$candy-app-accent:  md-palette($md-pink, A200, A100, A400);

// The warn palette is optional (defaults to red).
$candy-app-warn:    md-palette($md-red);

// Create the theme object (a Sass map containing all of the palettes).
$candy-app-theme: md-light-theme($candy-app-primary, $candy-app-accent, $candy-app-warn);

// Include theme styles for core and each component used in your app.
// Alternatively, you can import and @include the theme mixins for each component
// that you are using.
@include angular-material-theme($candy-app-theme);
```

You only need this single Sass file; you do not need to use Sass to style the rest of your app.

If you are using the Angular CLI, support for compiling Sass to css is built-in; you only have to
add a new entry to the `"styles"` list in `angular-cli.json` pointing to the theme
file (e.g., `unicorn-app-theme.scss`).

If you're not using the Angular CLI, you can use any existing Sass tooling to build the file (such
as gulp-sass or grunt-sass). The simplest approach is to use the `node-sass` CLI; you simply run:
```
node-sass src/unicorn-app-theme.scss dist/unicorn-app-theme.css
```
and then include the output file in your application.

The theme file can be concatenated and minified with the rest of the application's css.

#### 多个主题
You can extend the example above to define a second (or third or fourth) theme that is gated by
some selector. For example, we could append the following to the example above to define a
secondary dark theme:
```scss
.unicorn-dark-theme {
  $dark-primary: md-palette($md-blue-grey);
  $dark-accent:  md-palette($md-amber, A200, A100, A400);
  $dark-warn:    md-palette($md-deep-orange);

  $dark-theme: md-dark-theme($dark-primary, $dark-accent, $dark-warn);

  @include angular-material-theme($dark-theme);   
}
```

With this, any element inside of a parent with the `unicorn-dark-theme` class will use this
dark theme.

### 定制你自己的组件
For more details about theming your own components, see [theming-your-components.md](https://github.com/angular/material2/blob/master/docs/theming-your-components.md)

### 未来的工作
* Once CSS variables (custom properties) are available in all the browsers we support,
  we will explore how to take advantage of them to make theming even simpler.
