# tutorial
# Project moveSMART Pedometer Tutorial- Level 7 Ver 1
# Learning about calibration, experimenting, comparisons

## Step 1

In this tutorial, we will improve the accuracy of the physical activity monitor. On your screen is the step counter you built before, using the on ``||Input:on shake||`` block. We will replace that portion of the code in this tutorial.
```template
let counting = false
let step = 0
input.onButtonPressed(Button.A, function () {
    counting = true
})
input.onButtonPressed(Button.B, function () {
    counting = false
})
input.onGesture(Gesture.Shake, function () {
    if (counting) {
        step += 1
    }
})
basic.forever(function () {
    basic.showNumber(step)
})
```

## Step 2
We want the ``||variables: step||`` count to increase by 1 every time you take a step. To accurately do that, we will use the ``||Input:acceleration (mg) strength||`` value.

## Step 3
Use ``||logic: > ||`` to code a block that returns ``||logic: true||`` when ``||Input:acceleration (mg) strength||`` is bigger than 1500.

Hint: Here we have chosen the value 1500 for you as a starting point. You will have a chance to change it later!
```blocks
loops.everyInterval(500,function () {if (input.acceleration(Dimension.X) < 0) {}})
```

## Step 4
Now use the block ``||logic: if true then||`` so that the microbit can recognize when the acceleration strength is over 1500.

## Step 5
Now use the block ``||loops: everyInterval(100ms, )||`` to make the microbit check the acceleration strength every 100 miliseconds.

## Step 6
Now use a variable block so that ``||variables: step||`` would increase by 1 every time the threshold is passed.

## Step 7
Now download your code onto the microbit and experiment whether the threshold value is good! Try walking around thirty steps and check the accuracy. Adjust the threshold value from 1500 and download the program again as necessary.