# kaltura-video-player-ui
Video Player UI for Kaltura Android SDK

## Integrate in your project
1. Clone this library
2. Select File -> New -> Import Module
3. Navigate to the library folder and select the directory named `kalturavideoplayer`
4. Go to your app's build.gradle and add the following line in dependencies `implementation project(path: ':kalturavideoplayer')`
5. Sync project

## Usage
This library provides a fragment that consists of the player. To use this follow these steps:

1. Instantiate `KalturaPlayerConfig` class
Eg:
```
KalturaVideoPlayer.KalturaPlayerConfig config 
= new KalturaVideoPlayer.KalturaPlayerConfig("123",  // Partner ID
                "123", // Subpartner ID
                true, //Autoplay 
                "random", Media Source ID
                0L, // Start Position for the video
                "12432", // Kaltura Entry ID
                null, // Source URL
                200, // Thumbnail Height
                400 // Thumbnail Width
        );
```

2. Use the above config to create a fragment and add it to your activity:

```
Fragment f = KalturaVideoFragment.getInstance(config);
```

### KalturaPlayerConfig params

1. **Partner ID** - Partner ID for your project
2. **Subpartner ID** - subpartner ID for your project
3. **Autoplay **- if set to `true`, it will start playing the video automatically, else shows a thumbnail of the video
4. **Media Source ID** - Media Source ID,
5. **Start position** - Start position in seconds
6. **Kaltura Entry ID** - Kaltura Entry ID of the video 
7. **Source URL (optional)** - If provided, the player will ignore all params passed in partner ID, subpartner ID and entry ID. This is a direct streaming URL to the video.
8. **Thumnail Height** - Height of the thumbnail to be displayed. Decided as per the layout of your view
9. **Thumnail Width **- Width of the thumbnail to be displayed. Decided as per the layout of your view


## Screenshots
![Portrait](https://drive.google.com/file/d/1nWKgawqev3-v6SiKdmwBwYuTPc1wo_xa/view?usp=sharing)

![Landscape](https://drive.google.com/file/d/1l325U6FmjvYR081GHCDJwdwFX85D-vBQ/view?usp=sharing)

![Options](https://drive.google.com/file/d/1xqDPb50lYPrsGXeaCQbXDcDJXiKZjxm9/view?usp=sharing)


