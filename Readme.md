# React Embedable Components
Collection of embedable react components. Ready to use on any website without further installing. 

## Table of content
* [Premise](#Premise)
* [General info and usage](#General-info-and-usage)
* [Component List](#Component-List)
* [Technologies](#Technologies)
* [Setup](#Setup)
* [App's Future](#App's-future)


## Premise
As keeping all in one file is rather bad practice sometimes the specific environment can force on us certain limitations. For example when You build website from templates (from different provides of "ready" websites that You just need to ) You have little control on the application scope(and You can just add certain subpages, but You are restricted to just modify part of one html file which will be loaded, so You have to keep all in this one place), and You may want to add some more advanced features (and not necessarily create the website from scratch or with use of a framework - for whatever reason).
And here those "embedable components" come to help. They are build with such limitations in mind, one file for one specific feature You may want to have on the subpage.


## General info and usage
In this project each file represents one component. Those are all html files as those are designed with situation when You'll have to work just with HTML input. All needed JS is provided (or linked) inside ``<script>`` tags, and CSS styling inside ``<style>`` tags. 
To use the component just paste the code inside the file to desired part of HTML page. The desired component will be rendered where You put ``<div id="Component name"></div>``. If You use more than one component on single webpage 
```
<script src="https://unpkg.com/react@17/umd/react.production.min.js" crossorigin></script>
<script src="https://unpkg.com/react-dom@17/umd/react-dom.production.min.js" crossorigin></script>
<script src="https://unpkg.com/babel-standalone@6/babel.min.js"></script>
```
is needed just once. Those have to be linked to make React and JSX syntax work

All components are pre-filled with some exemplary content to show how it can work and comments should help to understand what changes should be made to adjust component for You need. More info about how to tweak the component will be provided in the list of components.

Notice, that in most cases You would have to provide data statisticaly. It's design decision as it was intended to be easy to use even with little knowledge about web development and providing data inside the file is way more starightforward than need to call some API. And if someone would have proper API to fill all of the component content he most likely would be doing it in own project and don't have this strict limitations this was intended to work around. 
And adjusting them to use API calls still shouldn't be too much time consuming. 


## Component List
Note: For every component listed the components it consists of will be reffered as "subcomponents"

### Playlist Component
Component which displays a embedded YouTube playlist, for which You have to specify Playlist Id (how to find it You can read here: https://support.google.com/youtube/answer/171780). 

In SongText subcomponent You have to provide the text and title for songs. 
Text of the songs as a list (array) of objects, where every object represents one song. With ``id`` being the numeric id (which make easy to keep track with the playlist) ``title`` being song title as a string and text being a list (array) of sublists of strings, where every sublists represents a verse or chorus (or otherwise separated part of text), and every strings represents one line (which should be displayed separately).
Those text and titles could be whatever You want: just a song lyrics, its translated version or even some completely alternate version of the song (the same goes to title)

In Description subcomponent You have a simple list of strings, when every of them is describing one song. Again You can put there whatever You want, just remember that first must corespondent to first song text etc.

The last subcomponent that needs to be adjusted is Buttons subcomponnent where You have to manualy put the quantity of song texts (decreased by 1 as ids starts with 0) by the next button to ensure proper rendering of buttons to toggle beetwen songs. 

In example data component is filled with, You have two songs (although provided playlist is actually longer) which are both alternate version of songs from german musical Count Monte Cristo but in Polish and putted to completely new context(this is the factor uniting all songs on the playlist, though not all texts are ready yet). Those are not full texts actually, just part of it as it was merely to 


## Technologies
- React
- Javascript
- JSX
- CSS
- HTML


## Setup
Those components require no installation. And no excesive knowledge of React, all what needs to be modify to fulfill your needs is in the comments and in Components list of this readme. 

## App's Future
Currently there's just one component - Playlist component, which displays embedded YouTube playlist with some addons - but next may be added in undetermined future. 
The Playlist component will have some updates to. 