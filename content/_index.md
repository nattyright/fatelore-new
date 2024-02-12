---
title: Styling Cheatsheet
type: docs
---

# Hugo Markdown Guide

*Basically* discord (discord uses a flavored Markdown syntax) but with support for more elements

https://www.markdownguide.org/tools/hugo/

# Formatting Shortcodes (enabled & tested)

## buttons

```tpl
{{</* button href="LINK_URL" */>}}BUTTON_NAME{{</* /button */>}}
```

{{< button href="https://sites.google.com/view/fatestarrynight/home?authuser=0" >}}Click Me{{< /button >}}
{{< button href="https://sites.google.com/view/fatestarrynight/home?authuser=0" >}}Click Me{{< /button >}}
{{< button href="https://sites.google.com/view/fatestarrynight/home?authuser=0" >}}Click Me{{< /button >}}

## columns (> 2 columns supported)

```tpl
{{</* columns */>}} 

1st column content

<---> <!-- magic separator, between columns -->

2nd column content

<---> <!-- magic separator, between columns -->

3rd column content, and so on...

{{</* /columns */>}} 
```
{{< columns >}} <!-- begin columns block -->

During the 5th Holy Grail War set in Fuyuki (2004), a catastrophe occurred near the end of that ritual. A Grail failed to produce a wish and there was no determined winner, resulting in the leftover energy produced by the defeated Servants to turn into thaumaturgical energy, also known as the 'Grail Mud'. This mud spread across Fuyuki, devouring the entire city as it grew in size with each landmark, building or organism it consumed. As such, it wasn't long until the rest of the world had to contend with the Grail Mud.


At its current rate, it was simply a matter of time until the mud consumed the entirety of the Earth. As such, Magi were forced to take the spotlight and defend themselves from this catastrophe via Magecraft and Servants of their own. This resulted in commoners finding out that Magecraft was real, gradually reducing the overall Mystery in the world and weakening Magecraft itself.

<---> <!-- magic separator, between columns -->

During the 5th Holy Grail War set in Fuyuki (2004), a catastrophe occurred near the end of that ritual. A Grail failed to produce a wish and there was no determined winner, resulting in the leftover energy produced by the defeated Servants to turn into thaumaturgical energy, also known as the 'Grail Mud'. This mud spread across Fuyuki, devouring the entire city as it grew in size with each landmark, building or organism it consumed. As such, it wasn't long until the rest of the world had to contend with the Grail Mud.


At its current rate, it was simply a matter of time until the mud consumed the entirety of the Earth. As such, Magi were forced to take the spotlight and defend themselves from this catastrophe via Magecraft and Servants of their own. This resulted in commoners finding out that Magecraft was real, gradually reducing the overall Mystery in the world and weakening Magecraft itself.
{{< /columns >}}

## wrap text around image - use single column

### float left
```tpl
{{</* columns img-left */>}}
![](IMG_UTL/RELATIVE_FILEPATH) MARKDOWN_CONTENT (img and text on the same line - don't type on a new line)
{{</* /columns */>}}
```

{{< columns img-left >}}
![](grailkun.png)  During the 5th Holy Grail War set in Fuyuki (2004), a catastrophe occurred near the end of that ritual. A Grail failed to produce a wish and there was no determined winner, resulting in the leftover energy produced by the defeated Servants to turn into thaumaturgical energy, also known as the 'Grail Mud'. This mud spread across Fuyuki, devouring the entire city as it grew in size with each landmark, building or organism it consumed. As such, it wasn't long until the rest of the world had to contend with the Grail Mud.

At its current rate, it was simply a matter of time until the mud consumed the entirety of the Earth. As such, Magi were forced to take the spotlight and defend themselves from this catastrophe via Magecraft and Servants of their own. This resulted in commoners finding out that Magecraft was real, gradually reducing the overall Mystery in the world and weakening Magecraft itself.

Unfortunately, not even the combined efforts of the Mage's Association and several other Magi organizations could halt the mud's pace. At best, it could be slowed down. Because of this, some Magi started to think about how to survive in a world completely corrupted by Grail Mud. This resulted in Magi working alongside scientists and engineers, which led to the creation of the nomadic cities. Unfortunately, their structure was deemed too weak to resist the potent curses of the mud.
{{< /columns >}}

### float right
```tpl
{{</* columns img-right */>}}
![](IMG_UTL/RELATIVE_FILEPATH) MARKDOWN_CONTENT (img and text on the same line - don't type on a new line)
{{</* /columns */>}}
```

{{< columns img-right >}}
![](grailkun.png)  During the 5th Holy Grail War set in Fuyuki (2004), a catastrophe occurred near the end of that ritual. A Grail failed to produce a wish and there was no determined winner, resulting in the leftover energy produced by the defeated Servants to turn into thaumaturgical energy, also known as the 'Grail Mud'. This mud spread across Fuyuki, devouring the entire city as it grew in size with each landmark, building or organism it consumed. As such, it wasn't long until the rest of the world had to contend with the Grail Mud.

At its current rate, it was simply a matter of time until the mud consumed the entirety of the Earth. As such, Magi were forced to take the spotlight and defend themselves from this catastrophe via Magecraft and Servants of their own. This resulted in commoners finding out that Magecraft was real, gradually reducing the overall Mystery in the world and weakening Magecraft itself.

Unfortunately, not even the combined efforts of the Mage's Association and several other Magi organizations could halt the mud's pace. At best, it could be slowed down. Because of this, some Magi started to think about how to survive in a world completely corrupted by Grail Mud. This resulted in Magi working alongside scientists and engineers, which led to the creation of the nomadic cities. Unfortunately, their structure was deemed too weak to resist the potent curses of the mud.
{{< /columns >}}

## image gallery

```tpl
{{</* gallery class="content-gallery" */>}}
  {{</* img src="IMAGE_PATH(url OR relative path (media upload))" */>}}
{{</* /gallery */>}}
```

{{< gallery class="content-gallery" >}}
  {{< img src="grailkun.png" >}}
  {{< img src="grailkun.png" >}}
  {{< img src="grailkun.png" >}}
{{< /gallery >}}
{{< gallery class="content-gallery" >}}
  {{< img src="https://cdn.discordapp.com/emojis/1150178198743691367.webp?size=96&quality=lossless" >}}
  {{< img src="https://cdn.discordapp.com/emojis/1150178198743691367.webp?size=96&quality=lossless" >}}
  {{< img src="https://cdn.discordapp.com/emojis/1150178198743691367.webp?size=96&quality=lossless" >}}
{{< /gallery >}}

## icons
```tpl
{{</* ico "ICONNAME" */>}}
```

{{< ico "heart" >}} {{< ico "star" >}} {{< ico "book" >}} {{< ico "cup" >}} {{< ico "sword" >}} {{< ico "sun" >}} {{< ico "snowman" >}} {{< ico "3d-rotate" >}}

list of available icons: https://github.com/RoneoOrg/hugo-shortcode-roneo-collection/tree/main/assets/svg

## details
```tpl
{{</* details title="Title" open=false */>}}
MARKDOWN_CONTENT
{{</* /details */>}}
```

{{< details title="Title" open=false >}}
## Markdown content
Lorem markdownum insigne...
{{< /details >}}

## expand
```tpl
{{</* expand "Custom Label" "..." */>}}
MARKDOWN_CONTENT
{{</* /expand */>}}
```

{{< expand "Custom Label" "..." >}}
## Markdown content
Lorem markdownum insigne...
{{< /expand >}}

## hints
```tpl
{{</* hint "info/warning/danger" */>}}
MARKDOWN_CONTENT
{{</* /hint */>}}
```

{{< hint "info" >}}
**Markdown content**  
Lorem markdownum insigne. Olympo signis Delphis! Retexi Nereius nova develat
stringit, frustra Saturnius uteroque inter! Oculis non ritibus Telethusa
{{< /hint >}}

{{< hint "warning" >}}
**Markdown content**  
Lorem markdownum insigne. Olympo signis Delphis! Retexi Nereius nova develat
stringit, frustra Saturnius uteroque inter! Oculis non ritibus Telethusa
{{< /hint >}}

{{< hint "danger" >}}
**Markdown content**  
Lorem markdownum insigne. Olympo signis Delphis! Retexi Nereius nova develat
stringit, frustra Saturnius uteroque inter! Oculis non ritibus Telethusa
{{< /hint >}}

## tabs
```tpl
{{</* tabs "UNIQUE_TAB_ID" */>}}
{{</* tab "TAB1_NAME" */>}} # TAB1_CONTENT {{</* /tab */>}}
{{</* /tabs */>}}
```

{{< tabs "uniqueid" >}}
{{< tab "MacOS" >}} # MacOS Content {{< /tab >}}
{{< tab "Linux" >}} # Linux Content {{< /tab >}}
{{< tab "Windows" >}} # Windows Content {{< /tab >}}
{{< /tabs >}}


# Media Shortcodes (enabled & tested)

## youtube
```tpl
{{</* youtube YOUTUBE_VID_ID */>}}
```
{{< youtube Q2HB7giCchY >}}

## audio
```tpl
{{</* audio "RELATIVE_FILE_PATH/URL(use file upload)" */>}}
```
{{< audio "spy_x_family_opening_-_mixed_nuts.mp3" >}}

## spotify
```tpl
Album 
{{</* spotify type="album" id="ALBUM_ID" */>}}
Track
{{</* spotify type="track" id="TRACK_ID" */>}}
Artist
{{</* spotify type="artist" id="ARTIST_ID" */>}}
Playlist 
{{</* spotify type="playlist" id="PLAYLIST_ID" */>}}
```

Album 
{{< spotify type="album" id="6bQkurEvgWIUUvKeqaJRq2" >}}

Track
{{< spotify type="track" id="3dsz3hT88uR2RJhtegnilY" >}}

Artist
{{< spotify type="artist" id="00FQb4jTyendYWaN8pK0wa" >}}

Playlist 
{{< spotify type="playlist" id="37i9dQZF1DX6dvuioZhoLo" >}}


# Archive
[Archive]({{< static "/archive/index.html" >}})


# Extended Shortcodes (In Development)
## Discord Tupper Style Posting
{{< tupper >}}

%%aida%%
**During the 5th Holy Grail War set in Fuyuki (2004)**, *a catastrophe occurred* near the end of that ritual. A Grail failed to produce a wish and there was no determined winner, resulting in the leftover energy produced by the defeated Servants to turn into thaumaturgical energy, also known as the ‘Grail Mud’. This mud spread across Fuyuki, devouring the entire city as it grew in size with each landmark, building or organism it consumed. As such, it wasn’t long until the rest of the world had to contend with the Grail Mud.

> At its current rate, it was simply a matter of time until the mud consumed the entirety of the Earth. As such, Magi were forced to take the spotlight and defend themselves from this catastrophe via Magecraft and Servants of their own. This resulted in commoners finding out that Magecraft was real, gradually reducing the overall Mystery in the world and weakening Magecraft itself.

%%ada%%
During the 5th Holy Grail War set in Fuyuki (2004), a catastrophe occurred near the end of that ritual. A Grail failed to produce a wish and there was no determined winner, resulting in the leftover energy produced by the defeated Servants to turn into thaumaturgical energy, also known as the ‘Grail Mud’. This mud spread across Fuyuki, devouring the entire city as it grew in size with each landmark, building or organism it consumed. As such, it wasn’t long until the rest of the world had to contend with the Grail Mud.

At its current rate, it was simply a matter of time until the mud consumed the entirety of the Earth. As such, Magi were forced to take the spotlight and defend themselves from this catastrophe via Magecraft and Servants of their own. This resulted in commoners finding out that Magecraft was real, gradually reducing the overall Mystery in the world and weakening Magecraft itself.

{{< /tupper >}}