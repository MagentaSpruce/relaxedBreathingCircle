# relaxedBreathingCircle

This simple JS project is for relaxation and breathing excercises. It can be utilized in a variety of ways and is also set up for mobile responsivness already.

The code is very short so it will be posted all here:
```JavaScript
const container = document.querySelector('.container')
const text = document.querySelector('#text')

const totalTime = 7500
const breatheTime = (totalTime / 5) * 2
const holdTime = totalTime / 5

breathAnimation()

function breathAnimation() {
    text.innerHTML = 'Breath In!'
    container.className = 'container grow'

    setTimeout(() => {
        text.innerText = 'Hold'

        setTimeout(() => {
            text.innerText = 'Breathe Out!'
            container.className = 'container shrink'
        }, holdTime)
    }, breatheTime)
}

setInterval(breathAnimation, totalTime)
```

