# Sintaxis Less

## Variables

```less
@primary-color: #4CAF50;
@padding: 10px;

.button {
  background-color: @primary-color;
  padding: @padding;
}

```

## Anidacion

```lessnav {
  nav {
  ul {
    margin: 0;
    padding: 0;
    li {
      display: inline-block;
    }
  }
}


```

## Mixins

```less
.rounded-corners(@radius: 5px) {
  border-radius: @radius;
  -webkit-border-radius: @radius;
  -moz-border-radius: @radius;
}

.box {
  .rounded-corners(10px);
  background: #eee;
}
```

## Mixins

```less
.rounded-corners(@radius: 5px) {
  border-radius: @radius;
  -webkit-border-radius: @radius;
  -moz-border-radius: @radius;
}

.box {
  .rounded-corners(10px);
  background: #eee;
}
```

## Operaciones

```less
@width: 100px;
@height: 50px;

.box {
  width: @width + 20px; // 120px
  height: @height * 2;  // 100px
}
```

## Funciones

```less@base: #111;
@color: lighten(@base, 20%);

.text {
  color: @color;
}
```

## Importar archivos

```less
@import "variables.less";
@import "mixins.less";

```

## Guardae Mixins

```less
.mixin(@a) when (@a > 10) {
  width: 100px;
}
.mixin(@a) when (@a <= 10) {
  width: 50px;
}

.box {
  .mixin(5); // aplicará el segundo
}
```