# TUVAL UI_
## HStack
Sorts objects or structures **horizontally**
``` sh
return ( 
    HStack(
        VStack( 
        ).width(100).height(100).background(Color.aqua), 
        VStack( 
        ).width(100).height(100).background(Color.black), 
    ).background(Color.gray) 
) 
```
>![Tuval UI Playground](https://cdn.discordapp.com/attachments/997404959052148736/997405367338287104/unknown.png)

## VStack
Sorts objects or structures **vertically**

```sh
return ( 
    VStack( 
        HStack( 
        ).width(100).height(100).background(Color.aqua), 
        HStack( 
        ).width(100).height(100).background(Color.black), 
    ).background(Color.gray) 
) 
```
>![Tuval UI Playground](https://cdn.discordapp.com/attachments/997404959052148736/997407671495954493/unknown.png)


## Height

You can change the **height** of the views

```sh
return (
    VStack(
        Text("Hello World")
    ).height(100).background(Color.aqua)
)
```
>![Tuval UI Playground](https://cdn.discordapp.com/attachments/997404959052148736/999212799051968542/unknown.png)

## Width

You can change the **width** of the views

```sh
return (
    VStack(
        Text("Hello World")
    ).width(100).background(Color.aqua)
)
```
>![Tuval UI Playground](https://cdn.discordapp.com/attachments/997404959052148736/999213833514139648/unknown.png)



# Stack Customization
## alignment
By using alignment, you can place the child of the stack you are on at 9 points of the grid.
```c
return(
    VStack({alignment: "hereAlignment" })(
    )
)
```

### cTop

Center and top alignment
```c
return(
    VStack({alignment: cTop})(
        Text("Hello World")
    )
)
```
>![Tuval UI Playground](https://cdn.discordapp.com/attachments/997404959052148736/999265494123171941/unknown.png)

### cTopLeading

Left and top alignment
```c
return(
    VStack({alignment: cTopLeading})(
        Text("Hello World")
    )
)
```
>![Tuval UI Playground](https://cdn.discordapp.com/attachments/997404959052148736/999266055895662682/unknown.png)

### cTopTrailing

Right and top alignment
```c
return(
    HStack({alignment: cTopTrailing})(
        Text("Hello World")
    )
)
```
>![Tuval UI Playground](https://cdn.discordapp.com/attachments/997404959052148736/999267232897044581/unknown.png)

### cLeading
Center and left
```c
return(
    HStack({alignment: cLeading})(
        Text("Hello World")
    )
)
```
>![Tuval UI Playground](https://cdn.discordapp.com/attachments/997404959052148736/999271173034614814/unknown.png)
### cTrailing
Center and right
```c
return(
    HStack({alignment: cTrailing})(
        Text("Hello World")
    )
)
```
>![Tuval UI Playground](https://cdn.discordapp.com/attachments/997404959052148736/999271505475158016/unknown.png)

## Spacing 
Throws a space between each view except the space below the subview
```c
return (
    HStack({ spacing: 50 })(
        VStack({ spacing: 50 })(
            HStack().width(100).height(100).background("red"),
            HStack().width(100).height(100).background("red"),
            HStack().width(100).height(100).background("red"),
        ),
        VStack({ spacing: 50 })(
            HStack().width(100).height(100).background("red"),
            HStack().width(100).height(100).background("red"),
            HStack().width(100).height(100).background("red"),
        ),
        VStack({ spacing: 50 })(
            HStack().width(100).height(100).background("red"),
            HStack().width(100).height(100).background("red"),
            HStack().width(100).height(100).background("red"),
        ),
    )
)
```
>![Tuval UI Playground](https://cdn.discordapp.com/attachments/997404959052148736/1001025020325281833/unknown.png)
## Text
Creates a text block and you can shape it
```sh
return ( 
    VStack( 
        HStack( 
            Text("Hello World!")
        )
    ) 
) 
```

>![Tuval UI Playground](https://cdn.discordapp.com/attachments/997404959052148736/997411008928821248/unknown.png)

#### Text Customization
##### **Change Text Color** / .foregroundColor() 
* You can change the color of the text using the .foregroundColor() property.
```sh
return ( 
    VStack( 
        VStack( 
            Text("Hello World!").foregroundColor(Color.blue),
            Text("Hello World!").foregroundColor("blue"),
            Text("Hello World!").foregroundColor("#0000ff"),
            Text("Hello World!").foregroundColor("rgb(0, 0, 255)"),
            Text("Hello World!").foregroundColor("hsl(240, 100%, 50%)")
        )
    ) 
) 
```
>![Tuval UI Playground](https://cdn.discordapp.com/attachments/997404959052148736/997421412400771132/unknown.png)

#### Text Background Color Customization
##### **Change Text Background Color** / .backgroundColor() 
* You can change the background color of the text using the .backgroundColor() property.
```sh
return ( 
    VStack( 
        VStack({spacing:10})( 
            Text("Hello World!").backgroundColor("blue").foregroundColor("white"),
            Text("Hello World!").backgroundColor("#0000ff").foregroundColor("white"),
            Text("Hello World!").backgroundColor("rgb(0, 0, 255)").foregroundColor("white"),
            Text("Hello World!").backgroundColor("hsl(240, 100%, 50%)").foregroundColor("white"),

        )
    ) 
) 
```
>![Tuval UI Playground](https://cdn.discordapp.com/attachments/997404959052148736/997424941907591178/unknown.png)

## Icons
You can shape your design using the framework's unique large icon library.
```sh
return (
    VStack(
        Icon(IconLibrary.Accessibility).size(70)
    )
)
```
>![Tuval UI Playground](https://cdn.discordapp.com/attachments/997404959052148736/999222267986845776/unknown.png)

## Padding
Padding is used to create space around an element's content, inside of any defined borders.
You have full control over the padding. There are properties for setting the padding for each side of an element (top, right, bottom, and left).
### Padding Top
usage is .paddingTop(" ")
```sh
return (
    VStack(
        Text("This text has a top padding of 30 px")
        .background("red").foregroundColor("white").paddingTop("30px")
    )
).background("#fffff0")
```
>![Tuval UI Playground](https://cdn.discordapp.com/attachments/997404959052148736/1001035443992805376/unknown.png)

### Padding Bottom
usage is .paddingBottom(" ")
```sh
return (
    VStack(
        Text("This text has a bottom padding of 30 px")
        .background("red").foregroundColor("white").paddingBottom("30px")
    )
).background("#fffff0")
```
>![Tuval UI Playground](https://cdn.discordapp.com/attachments/997404959052148736/1001035815817850920/unknown.png)
### Padding Right
usage is .paddingRight(" ")
```sh
return (
    VStack(
        Text("This text has a right padding of 30 px")
        .background("red").foregroundColor("white").paddingRight("30px")
    )
).background("#fffff0")
```
>![Tuval UI Playground](https://cdn.discordapp.com/attachments/997404959052148736/1001036138091389028/unknown.png)

### Padding Left
usage is .paddingLeft(" ")
```sh
return (
    VStack(
        Text("This text has a left padding of 30 px")
        .background("red").foregroundColor("white").paddingLeft("30px")
    )
).background("#fffff0")
```
>![Tuval UI Playground](https://cdn.discordapp.com/attachments/997404959052148736/1001036837026017352/unknown.png)
### Other Padding Usages
#### Padding All
usage is .padding(" ")
```sh
return (
    VStack(
        Text("This text has a top, bottom, left, and right padding of 30px.")
        .background("red").foregroundColor("white").padding("30px")
    )
).background("#fffff0")
```
>![Tuval UI Playground](https://cdn.discordapp.com/attachments/997404959052148736/1001041107796377671/unknown.png)

#### Padding Left-Right Top-Bottom
usage is .padding("TOPBOTTOMpx LEFTRIGHTpx")
```sh
return (
    VStack(
        Text("This text has a top and bottom padding of 25px, and a right and left padding of 50px.")
        .background("red").foregroundColor("white").padding("25px 50px")
    )
).background("#fffff0")
```
>![Tuval UI Playground](https://cdn.discordapp.com/attachments/997404959052148736/1001042329081221130/unknown.png)

#### Padding Top Right-Left Bottom,
usage is .padding("TOPpx LEFTRIGHTpx BOTTOMpx")



# Customize Shapes
| Using | Forming |
| ------ | ------ |
| .size() | You can give value in integer format and change size |


This will create the dillinger image and pull in the necessary dependencies.
Be sure to swap out `${package.json.version}` with the actual
version of Dillinger.


```sh
docker run -d -p 8000:8080 --restart=always --cap-add=SYS_ADMIN --name=dillinger <youruser>/dillinger:${package.json.version}
```

> Note: `--capt-add=SYS-ADMIN` is required for PDF rendering.






