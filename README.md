# Paint와 Composite 차이

[css 속성](https://csstriggers.com/)

[브라우저 렌더링 원리 정리](https://blog.naver.com/pjt3591oo/222495673377)

```html
<!DOCTYPE html>
<html>

<head>
  <style>
    .base {
      height: 50px;
      width: 50px;
      transition-duration: 3.5s;
    }
    
    .a {
      background-color: blue;
      transform: translateX(0px);
    }

    .b {
      background-color: red;
      position: relative;
      left: 0px;
    }
  </style>
</head>

<body>
  <div class="base a" id="a"></div>
  <div class="base b" id="b"></div>
  <button id="btn">btn</button>
  <button id="trigger">trigger</button>
  <script>
    const a = document.getElementById('a');
    const b = document.getElementById('b');

    document.getElementById('btn').addEventListener('click', () => {
      a.style.transform = 'translateX(400px)';
      b.style.left = '400px';
    })

    document.getElementById('trigger').addEventListener('click', () => {
      alert(1)
    })
  </script>
</body>

</html>
```