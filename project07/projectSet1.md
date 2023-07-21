# Prjects related to Doms

## Project link
[click here](https://stackblitz.com/edit/dom-project-chaiaurcode-venxw3?file=index.html)

# Solution code

## Project 1

```javascript
const buttons = document.querySelectorAll('.button');

const body = document.querySelector('body');

buttons.forEach((button) => {
  console.log(button);
  button.addEventListener('click', (event) => {
    console.log(event);
    console.log(event.target);
    if (event.target.id === 'grey') {
      body.style.backgroundColor = event.target.id;
    }
    if (event.target.id === 'white') {
      body.style.backgroundColor = event.target.id;
    }
    if (event.target.id === 'blue') {
      body.style.backgroundColor = event.target.id;
    }
    if (event.target.id === 'yellow') {
      body.style.backgroundColor = event.target.id;
    }
  });
});

```

# project 2

```javascript

const form = document.querySelector('form');

form.addEventListener('submit', (e) => {
  e.preventDefault();
  const height = parseInt(document.querySelector('#height').value);
  const weight = parseInt(document.querySelector('#weight').value);
  const results = document.querySelector('#results');

  if (height === '' || height < 0 || isNaN(height)) {
    results.innerHTML = `please give is a valid height ${height}`;
  }
  if (weight === '' || weight < 0 || isNaN(weight)) {
    results.innerHTML = `please give is a valid weight ${weight}`;
  } else {
    const bmi = (weight / ((height * height) / 10000)).toFixed(2);
    // results.innerHTML = `<span>${bmi}</span>`;
    let message = `<span>Your BMI: ${bmi}</span><br>`;
    if (bmi < 18.6) {
     message += "<span>underweight.</span>";
    } else if(bmi >=18.6 && bmi <= 24.9){
      message += "<span>Normal range.</span>";
    }
    else {
      message += "<span>overweight.</span>";
    }
    results.innerHTML = message;
  }
});


```

# project 3

``` javascript
const clock = document.getElementById('clock');

setInterval(function () {
  let date = new Date();
  // console.log(date.toLocaleTimeString())
  clock.innerHTML = date.toLocaleTimeString();
}, 1000);


```