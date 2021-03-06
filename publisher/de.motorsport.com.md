# de.motorsport.com

In this documentation you find the placement details for your Website.  Please find an test-site on the following link:    [Xandr test site](https://adtechnology.mediaimpact.de/test-Xandr/)

## AdLib

Please use the following JS for the adLib: ```https://acdn.adnxs.com/as/1h/pages/motorsport.js```


## Placements

 Desktop

| Placement Name|Xandr|
| ------------- | ----- |
|Superbanner|superbanner|
|Sky|sky|
|Sky|sky_btf|
|Billboard|billboard|
|Billboard_btf|billboard_btf|
|Medium Rectangle|mrec|
|Medium Rectangle|mrec_btf|
|Richmedia / Outstream|inpage|
|regteaser01|teaser|
|regteaser02|teaser_2|

 Mobile


| Placement Name|Xandr|
| ------------- | ----- |
|Reminder|banner|
|Content Ad|mrec|
|Rectangle_Mobil/Rectangle01|mrec_btf|
|Richmedia / Outstream|inpage|
|regteaser01|teaser|
|regteaser02|teaser_2|


 AMP


| Placement Name|Xandr|
| ------------- | ----- |
|Reminder|banner|
|Content Ad|mrec|


 [Placement Codes](https://github.com/spring-media/adsolutions-implementationReference/blob/master/publisher-display-reference.md#3-define-the-ad-placements-for-the-website)

# Display

### Desktop - Index:

`	adPlacements: ["superbanner","sky","sky_btf","billboard","billboard_btf","mrec","mrec_btf","inpage","teaser","teaser_2"],`

### Desktop - Story:

`	adPlacements: ["superbanner","sky","sky_btf","billboard_btf","mrec","mrec_btf","inpage","teaser","teaser_2"],`

### Desktop - Bildergalerien:

`	adPlacements: ["superbanner","mrec"],`

### Desktop - Statistiken:

`	adPlacements: ["superbanner","sky","sky_btf","billboard_btf","mrec","mrec_btf","inpage","teaser","teaser_2"],`

### Desktop - Liveticker:

`	adPlacements: ["superbanner","sky","sky_btf","billboard_btf","mrec","mrec_btf","inpage","teaser","teaser_2"],`

### Mobile:

`	adPlacements: ["banner","mrec","mrec_btf","inpage","teaser"],`

### AMP:

`	adPlacements: ["banner_sticky","mrec"],`




# Video

### Desktop - Video:

`	adPlacements: ["preroll","midroll"],`

### Mobile - Video:

`	adPlacements: ["preroll","midroll"],`

### AMP - Video:

`	adPlacements: ["preroll","midroll"],`




[Placement Sizes](https://github.com/spring-media/adsolutions-implementationReference/blob/master/publisher-display-reference.md#4-define-the-sizes-for-every-ad-placement)


# Desktop:

```
	adSlotSizes: {
		"superbanner": [{
			"minWidth": 1023,
			"sizes": [[728,90],[728,600],[1000,600],[800,250],[970,250]]
		}],
     
		"sky": [{
			"minWidth": 1,
			"sizes": [[160,600],[120,600],[300,600],[500,1000],[1000,1000]]
		}],
    
    		"sky_btf": [{
			"minWidth": 1,
			"sizes": [[160,600],[120,600],[300,600],[500,1000],[1000,1000]]
		}],
    
		"billboard": [{
			"minWidth": 799,
			"sizes": [[800,250]]
		},{
			"minWidth": 969,
			"sizes": [[970,250],[800,250]]
		},{
			"minWidth": 767,
			"sizes": [[728,90]]			
		}],
    
    		"billboard_btf": [{
			"minWidth": 799,
			"sizes": [[800,250]]
		},{
			"minWidth": 969,
			"sizes": [[970,250],[800,250]]
		},{
			"minWidth": 767,
			"sizes": [[728,90]]			
		}],
    
		"mrec": [{
			"minWidth": 1,
			"sizes": [[300,250],[300,600]]
		}],
    
    		"mrec_btf": [{
			"minWidth": 1,
			"sizes": [[300,250],[300,600]]
		}],
    
    		"inpage": [{
			"minWidth": 1,
			"sizes": [[1,1],[640,360],[1000,300]]
		}],
    
    		"teaser": [{
			"minWidth": 1,
			"sizes": [[300,150]]
		}],

		"teaser_2": [{
			"minWidth": 1,
			"sizes": [[300,150]]
		}],
		
	},
```

# Mobile:

```
	adSlotSizes: {
		"banner": [{
			"minWidth": 1,
			"sizes": [[320,50],[320,75],[320,80]]
		}],
     
		"mrec": [{
			"minWidth": 1,
			"sizes": [[300,250],[320,50],[320,75],[320,160],[300,300]]
		}],
     
		"mrec_btf": [{
			"minWidth": 1,
			"sizes": [[300,250],[320,50],[320,75],[320,160],[300,300]]
		}],
				
		"teaser": [{
			"minWidth": 1,
			"sizes": [[300,150]]
		}],

		"teaser_2": [{
			"minWidth": 1,
			"sizes": [[300,150]]
		}],		
     
		"inpage": [{
			"minWidth": 1,
			"sizes": [[1,1],[640,360],[1000,300]]
		}],
		    
	},
```



# AMP:

For AMP-Integration follow the guides on [publisher-amp-reference](https://github.com/spring-media/adsolutions-implementationReference/blob/master/publisher-amp-reference.md). Include your pagenames in "invCode":

## connected ads
```html
<amp-ad width=300 height=250
        type="Xandr"
        data-target="mrec"
        json='{
            "pageOpts": {
                "member": 7823
            },
            "adUnits": [{
                "disablePsa": true,
                "invCode": "mywebsite.de-amp-your_pagename-mrec",
                "sizes": [[300, 250]],
                "keywords": {
                    "misc": ["rock", "pop"]
                },
                "targetId": "mrec"
            },{
                "disablePsa": true,
                "invCode": "mywebsite.de-amp-your_pagename-mrec",
                "sizes": [[300, 250]],
                "keywords": {
                    "misc": ["rock", "pop"]
                },
                "targetId": "mrec_2"
            }]
        }'
></amp-ad>
```

Under [amp-sticky-ad](https://www.ampproject.org/docs/reference/components/amp-sticky-ad) is explained how the placement "sticky_banner" must be installed to be sticky and which script you have to include.



## Important notes

- For Intext Outstream and for Richmedia we just need one placement with Xandr.
- __IMPORTANT__ Please palace the "inpage" placement in the required position for InText. Take care that we need the whole website wide for it.
- You can repeat the btf placements as much as you want. Please use the following schema:
```
Example for 3 Medium Rectangle btf

mrec_btf
mrec_btf_2
mrec_btf_3
```



## Help

If you have some question don't hesitate to contact us:



__Carlos Bracho__
 
  Head of Ad Technology
  Spring
  
  Tel: +49 30 2591 76784
  Mobile: +49 151 44619807 
  carlos.bracho@axelspringer.de

__Ad Technology Team__
  adtechnology@axelspringer.de
  
