# Clearage documentation

Hi! This is a simple documentation on how to use this extension.


## Simple use

Click on icon or press Alt-L, It couldn't be **easier**!


## Console methods

We want to preserve your precious time by allowing you to clean your local storage as quickly and efficiently as possible. 

It is on this concept that the extension is intended to be as simple as possible to use.

We do not seek to complicate its use. But we want to make it possible to use methods developed for specific cases. 

We have chosen to integrate these methods through the web console to avoid missing our main principle: its speed and ease of use.

### Understand the Clearage history

The Clearage history is based on the design principle: *K.I.S.S.* 

We have opted for simplicity by avoiding any unnecessary complexity.

The Clearage history is a simple array of objects. **Nothing more, nothing less.** Each object always has *three* properties: *key, localStorageSaved and date*.

***
| Properties | What they do |
|--|--|
|**key**|The *key* is a specific and distinct property between each object. It allows the use of certain actions on the Clearage history through this element   
|**localStorageSaved**|The *localStorageSaved* property contains the cleaned and saved "local storage" in the history.
|date|The date property represents the date and time, specific to your region, of the recording of the local storage within the Clearage history.|
***

