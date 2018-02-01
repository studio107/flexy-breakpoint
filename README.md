[![Build Status](https://travis-ci.org/studio107/flexy-breakpoint.svg?branch=master)](https://travis-ci.org/studio107/flexy-breakpoint)

# flexy-breakpoint-has

```scss
@include assert-true(flexy-breakpoint-has(small));
@include assert-false(flexy-breakpoint-has(unknown));
```

# flexy-breakpoint-limit

```scss
@include flexy-breakpoint-limit(medium) {
  font-size: 2rem;
}

// Output

@media only screen and (min-width: 769px) {
  font-size: 2rem;
}
```

```scss
@include flexy-breakpoint-limit(medium, large) {
  font-size: 2rem;
}

// Output

@media only screen and (min-width: 769px) and (max-width: 991.9px) {
  font-size: 2rem;
}
```
