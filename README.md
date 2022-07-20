# TUVAL UI
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






