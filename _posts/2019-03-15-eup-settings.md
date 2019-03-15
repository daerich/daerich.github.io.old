--- 
layout: post
title: "EUP Settings" 
date: 2019-03-15 15:43:01 -0600 
categories: ['Internet']
--- 

# LSPDFR's new settings xml

With the introduction of LSPDFR Version 0.4 we were allowed to modify crucial ambient data with the help of the custom folder.
Unfortunately adding outfits from the EUP Mod by Alex_Ashfold has been obstructed by the new outfit 'api' (at least if you want them to integrate
them natively).


Thanks to the research of  [mkalash](https://www.lcpdfr.com/profile/354879-mkalash/) he released a script to generate outfits from
the legacy _EUP Menu_ .ini files, which I'll break down today.

# The API
```

componentNames = {
    "Mask": 1,
    "UpperSkin": 3,
    "Pants": 4,
    "Parachute": 5,
    "Shoes": 6,
    "Accessories": 7,
    "UnderCoat": 8,
    "Armor": 9,
    "Decal": 10,
    "Top": 11
}
```
Those are the numerical ids of the '```<component>```' tag.

```
propNames = {
    "Hat": 0,
    "Glasses": 1,
    "Ear": 2,
    "Watch": 6
}
```
The numerical ids of the '```<prop>```' tag

## The maths
Apparently you'll have __to deduce 1 (-1) if one of them
have (or both) has(have a higher value than 0  from the corresponding eup numerical num:num structure defining the ``` drawable:texture``` .__ Apprehend them to the corresponding '```<component>```' and '```<prop>```' tags and __you'll have integrated
your eup outfits natively into LSPDFR's new outfit api.__










