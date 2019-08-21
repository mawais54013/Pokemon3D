# Pokemon3D

IOS application that renders a 3d model of a pokemon card that is scanned. For this project the following pokemon are only available for rendering 3d models: Eevee, Oddish, and Darkrai. 

Example Image Below 
 
![index](dark1.PNG)

# Getting Started 

Users can add more images of pokemon by including the image of a pokemon card in the Assets and download 3d models from ROEStudios and add them to the Art file as an scn file. 

## Prerequisites
This AR project can only be viewed on an actual Iphone and will not work on a simulator. 

# Code Snippets
The code below checks the image to see if there is a match with any of the cards in the assets. If there is then it renders the 3d model for it and add to a node child to be return at the end of the function. 
```
if imageAnchor.referenceImage.name == "eevee" {
    if let pokeScene = SCNScene(named: "art.scnassets/eevee.scn") {
        
        if let pokeNode = pokeScene.rootNode.childNodes.first {
            
            pokeNode.eulerAngles.x = .pi / 2
            
            planeNode.addChildNode(pokeNode)
            
        }
        
    }
}
```

# Built With
- Swift
- ARKit
- UiKit
- SceneKit 
- Cardicuno
- ROEStudios for 3D models


# Author
* **Muhammad** - https://github.com/mawais54013