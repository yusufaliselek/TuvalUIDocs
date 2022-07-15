# TUVAL UI
## HStack Usage
Sorts objects or structures **horizontally**
``` 
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

## VStack Usage
Sorts objects or structures **vertically**

```
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

## Text Usage
Creates a text block and you can shape it
```
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
```
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
```
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




# Örnek Kullanımlar
| Plugin | README |
| ------ | ------ |
| Dropbox | [plugins/dropbox/README.md][PlDb] |
| GitHub | [plugins/github/README.md][PlGh] |
| Google Drive | [plugins/googledrive/README.md][PlGd] |
| OneDrive | [plugins/onedrive/README.md][PlOd] |
| Medium | [plugins/medium/README.md][PlMe] |
| Google Analytics | [plugins/googleanalytics/README.md][PlGa] |





```sh
cd dillinger
docker build -t <youruser>/dillinger:${package.json.version} .
```

This will create the dillinger image and pull in the necessary dependencies.
Be sure to swap out `${package.json.version}` with the actual
version of Dillinger.


```sh
docker run -d -p 8000:8080 --restart=always --cap-add=SYS_ADMIN --name=dillinger <youruser>/dillinger:${package.json.version}
```

> Note: `--capt-add=SYS-ADMIN` is required for PDF rendering.

