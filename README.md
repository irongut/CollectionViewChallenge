# CollectionView Challenge

Details of the CollectionView Challenge can be found [here](https://github.com/pauldipietro/CollectionViewChallenge).

`CollectionView` docs can be found [here](https://docs.microsoft.com/en-us/xamarin/xamarin-forms/user-interface/collectionview/).

## My Implementation

I copied a screen from one of my current apps into the project including SVG images, converters, models and a cut down version of my ViewModel that fakes the data. I then converted it to use a CollectionView instead of a ListView.

I ran into one issue - ListView DataTemplates use a ViewCell, CollectionView DataTemplates do not. Unfortunately VS2019 did not spot anything wrong but at runtime Mono was throwing an Invalid Cast exception and closing the app. The exception confused me for a while until I looked at the docs more closely. This would not have been an issue if I was creating a new screen using CollectionView rather than converting one from a ListView.

This screen does not have a lot of data to display but each cell is quite complicated with two SVG images. Performance seems similar for both implementations as shown in the videos below from a Galaxy S6 Edge (Android 7.0).


## Using ListView

![ListView](https://github.com/irongut/CollectionViewChallenge/blob/master/CVC-ListView-S6Edge.gif)

## Using CollectionView

![ListView](https://github.com/irongut/CollectionViewChallenge/blob/master/CVC-CollectionView-S6Edge.gif)
