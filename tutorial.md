# tutorial
# Project moveSMART Pedometer Tutorial- Level 6
```blocks
loops.everyInterval(500,function () {if (0 < 0) {}})
```

## Step 1

In this tutorial, we will improve the accuracy of the physical activity monitor. On your screen is the step counter you built before, using the on ``||Input:on shake||`` block.
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

```blocks
Here we have chosen the value 1500 for you as a starting point. You will have a chance to change it later!
```

## Step 4
Now using the 
``||logic: if true then||`` and 
so that the microbit can recognize when the 

## Step 5
Now replace the ``||Input: on shake||`` block with your conditional statement so that the ``||variables: step||`` count increases every time acceleration goes over 1500.

## Step 6
Now put the entire conditional code in the ``||Basic: forever||`` block so the microbit keeps checking the acceleration strength.

## Step 7
Now download your code onto the microbit and experiment whether the threshold value is good! Try walking around thirty steps and check the accuracy. Adjust the threshold value and download the program again as necessary.