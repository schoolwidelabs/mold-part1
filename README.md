
# Mold Tutorial Part 1
Create your program to measure some of the conditions for mold growth

## Step 1
When you turn the micro:bt on, what is happening?``||gatorEnvironment: initialize||`` the environmental sensor

```template
gatorEnvironment.beginEnvironment()
```

## Step 2
How will you ``||input:tell the micro:bit||`` to collect data?
```blocks
input.onButtonPressed(Button.A, function () {
   
})
```

## Step 3
How many measurements do you need to ``||basic: show||``?
```blocks
input.onButtonPressed(Button.A, function () {
    basic.showNumber(0)
    basic.showNumber(0)  
})
```

## Step 4
What ``||gatorEnvironment: measurements||`` do you want to take?
```blocks
input.onButtonPressed(Button.A, function () {
    basic.showNumber(gatorEnvironment.getMeasurement(measurementType.degreesF))
    basic.showNumber(gatorEnvironment.getMeasurement(measurementType.humidity)) 
})
```

## Step 5
How will you ``||basic: know which measurement||`` you are taking?
```blocks
input.onButtonPressed(Button.A, function () {
    basic.showString("T")
    basic.showNumber(gatorEnvironment.getMeasurement(measurementType.degreesF))
    basic.showString("H")
    basic.showNumber(gatorEnvironment.getMeasurement(measurementType.humidity))
})
```

## Step 6
What happens if the value of the data collected is a really long decimal? 
How could you make ``||Math:the data easier to read?||``?

```blocks
input.onButtonPressed(Button.A, function () {
    basic.showString("T")
    basic.showNumber(Math.round(gatorEnvironment.getMeasurement(measurementType.degreesF)))
    basic.showString("H")
    basic.showNumber(Math.round(gatorEnvironment.getMeasurement(measurementType.humidity)))
})
```

## Step 7
You need to record your information, so you might want to ``||basic: take a break||``
in between measurements

```blocks
input.onButtonPressed(Button.A, function () {
    basic.showString("T")
    basic.showNumber(Math.round(gatorEnvironment.getMeasurement(measurementType.degreesF)))
    basic.pause(1000)
    basic.showString("H")
    basic.showNumber(Math.round(gatorEnvironment.getMeasurement(measurementType.humidity)))
    basic.pause(1000)
})
```

## Step 8
``|Download your code|`` and try it out


```package
gatorEnvironment=github:sparkfun/pxt-gator-environment
```

