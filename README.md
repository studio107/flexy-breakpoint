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

# flexy-breakpoint-step

```scss
@include assert-equal(flexy-breakpoint-step(small, xlarge), (max-width: 1199.9px, min-width: 0));
@include assert-equal(flexy-breakpoint-step(medium), (min-width: 769px));
```

# flexy-breakpoint-get

```scss
@include assert-equal(flexy-breakpoint-get(small), 0);
@include assert-equal(flexy-breakpoint-get(medium), 769px);
@include assert-equal(flexy-breakpoint-get(large), 992px);
@include assert-equal(flexy-breakpoint-get(xlarge), 1200px);
@include assert-equal(flexy-breakpoint-get(xxlarge), 1600px);
```

# flexy-breakpoint-next-step
``
```scss
@include assert-equal(flexy-breakpoint-next-step(small), (min-width: 0, max-width: 768.9px));
@include assert-equal(flexy-breakpoint-next-step(medium), (min-width: 769px, max-width: 991.9px));
@include assert-equal(flexy-breakpoint-next-step(large), (min-width: 992px, max-width: 1199.9px));
@include assert-equal(flexy-breakpoint-next-step(xlarge), (min-width: 1200px, max-width: 1599.9px));
@include assert-equal(flexy-breakpoint-next-step(xxlarge), (min-width: 1600px));
```
