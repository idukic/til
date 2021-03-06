# @mixin placeholder()

### Example 1.
**Set @mixin**
```scss
@mixin placeholder(){
  ::-webkit-input-placeholder {@content}
  :-moz-placeholder           {@content}
  ::-moz-placeholder          {@content}
  :-ms-input-placeholder      {@content}
}
```

**Use @mixin**
```scss
@include placeholder {
    color: red;
    font-weight:noraml;
}
```

### Example 2.
**Set @mixin**
*optional: set default values*
```scss
@mixin placeholder($color, $opacity: 1, $font-weight: 100) {
    &::-webkit-input-placeholder {
        color: $color;
        opacity: $opacity;
        font-weight: $font-weight;
    }

    &:-moz-placeholder {
        color: $color;
        opacity: $opacity;
        font-weight: $font-weight;
    }

    &::-moz-placeholder {
        color: $color;
        opacity: $opacity;
        font-weight: $font-weight;
    }

    &:-ms-input-placeholder {
        color: $color;
        opacity: $opacity;
        font-weight: $font-weight;
    }
}
```

**Use @mixin**
```scss
@include placeholder($input-placeholder-color)

// or
//-------

@include placeholder(red, 0.8, 400)
```