# NameThat🐟

A cross-platform fish identifier app for anglers and fish hobbyists created using React Native, Flask, and Tensorflow.

Authors: Alex Li, Daniel Lee, and Yifan Zong

[![Demo CountPages alpha](https://j.gifs.com/PjEDvl.gif)](https://www.youtube.com/watch?v=A8j4WG5bz5Q)
> Click gif to see full demonstration of how our app works

## How does it work?

Users can capture an image of a fish using the in-app camera or upload and select from a gallery. The image is then serialized and passed through a CNN model (transfer-learned from the EfficientNetV2 that was trained on the ImageNet dataset) to be classified as 1 of 20 available species or as unrecognized. Furthermore, once a classification is made, the user can also navigate to our interactive library that contains 20 different cards with interesting facts on each of the fish species such as their life cycles, diet, and prominent features.

The current model is trained on 20 different classes of fish species commonly found in North America in areas like Lake Ontario or Lake Michigan.

We trained the data on publicly available images from Google Images and filtered down to around 100 images per class. Ideally, we would want a lot more data, but as we had to collect and process the data ourselves, we were limited in terms of time and resources. Nevertheless, we were able to observe visible performance improvement by employing different data-augmentation techniques (rotation, shear, flip, etc) on the available data. 

## Installation

When installing expo libraries/SDKs use

```
expo install [library]
```

For regular javascript and react libraries, simply run

```
yarn add [library]
```

## Usage

To start the application, navigate to the client directory and run

```
yarn start
```

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License

[MIT](https://choosealicense.com/licenses/mit/)
