---
layout: post
title: "Android Parallax Scrolling Fun"
description: ""
category: 
tags: []
---
{% include JB/setup %}

Recently I've been asked to do parallax scrolling, kind of like in the app Path. It turned out to be fairly easy and interesting. I thought I'd share how I did it. I've made a little demo for it on github.  I've borrowed 2 beautiful photos form Adrian Lumani for this project. The photos are here and here. 

The effect of the demo is straight forward. You have a ListView of photos, and its initial and scrolled positions look like these:

ListView initial position

Scrolled position
I am going to skip the mundane code of creating a ListView and populating it. The piece of code that does the parallax scrolling is this: 
```Java
@Override
public void onScroll(AbsListView listView, int fvi, int visibleItemCount, int tic) {
    if (visibleItemCount > 0){
        View topItem = listView.getChildAt(0);
        ImageView image = (ImageView)topItem.findViewById(R.id.image_view);
        int scrollOffset = topItem.getTop();
        image.setTranslationY((float)(scrollOffset*-0.5));
    }
}
```
View topItem = listView.getChildAt(0); gets the first visible item of the list view
get the ImageView within that item
topItem.getTop() gets us the offset the top item has with regard to its parent. For example, if the top item is 400px tall and half of it is scrolled beyond the screen, getTop() would return -200px.
We then take the scroll offset and move the image by HALF of that amount in the OPPOSITE direction. So it will look as if the image is scrolling at a slower speed, hence the effect!