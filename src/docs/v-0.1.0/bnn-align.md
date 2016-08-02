---
title: Home
description: index.
layout: docs.hbs
---

# bnn-align

*Banana code:*
```css
.demo {
  bnn-align: center center;
}
```

*Result:*
```css
.demo {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
}
```

*Banana code:*
```css
.demo {
  bnn-align: right bottom;
}
```

*Result:*
```css
.demo {
  display: flex;
  flex-wrap: wrap;
  justify-content: flex-end;
  align-items: flex-end;
}
```
