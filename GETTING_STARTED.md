使用Angular CLI开始使用Angular Material 2。

## 安装 CLI
 
 ```bash
 npm install -g angular-cli
 ```
 
## 创建一个新项目
 
 ```bash
 ng new my-project
 ```

The new command creates a project with a build system for your Angular app.

## 安装 Angular Material 组件

```bash
npm install --save @angular/material

# [Build a Material Design App with Angular 2](https://www.youtube.com/watch?v=hHhwg-VJxw8&gl=KR)

npm i -S @angular2-material/core @angular2-material/button @angular2-material/core @angular2-material/card

npm i -S @angular2-material{core,button,card,checkbox,icon,input,list,toolbar}@2.0.0-alpha.10

# ??? Error
```

## 导入 Angular Material NgModule
  
**src/app/app.module.ts**
```ts
import { MaterialModule } from '@angular/material';
// other imports 
@NgModule({
  imports: [MaterialModule.forRoot()],
  ...
})
export class PizzaPartyAppModule { }
```

## 包括核心和主题样式 :  
这是**必需**，以应用所有的核心和主题样式到您的应用程序。  
要么你可以使用一个预构建的主题，要么定义自己的自定义主题。

:trident:  请参阅[主题指南](docs/theming.md) 以获取说明.

### 其他设置 `md-slide-toggle` 和 `md-slider`:
The slide-toggle and slider components have a dependency on [HammerJS](http://hammerjs.github.io/).

Add HammerJS to your application via [npm](https://www.npmjs.com/package/hammerjs), a CDN 
(such as the [Google CDN](https://developers.google.com/speed/libraries/#hammerjs)), or served 
directly from your app.

### [可选的] 使用 Material Design 的图标 `md-icon`:

- If you want to use Material Design icons in addition to Angular Material components, 
load the Material Design font in your `index.html`.  
`md-icon` supports any font icons or svg icons, so this is only one option for an icon source.
       
**src/index.html**
```html
<link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet">
```

## Angular Material 2 项目样品 
- [Material 2 Sample App](https://github.com/jelbourn/material2-app)
- [Angular Connect 2016 Demo](https://github.com/kara/leashed-in)
