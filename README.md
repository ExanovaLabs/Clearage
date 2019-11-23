![Clearage Exanove Labs](https://github.com/ARKHN3B/Clearage/blob/master/images/promotional/banner.png)

***

Hi! This is a documentation on how to use this extension.


## Simple use

Click on icon or press Alt-L, It couldn't be **easier**!


## Specific use cases

*We want to preserve your precious time by allowing you to clean your local storage as quickly and efficiently as possible.* 

It is on this **concept** that the extension is intended to be as simple as possible to use.

We do not seek to complicate its use. But we want to make it possible to use methods developed **for specific cases**. 

We have chosen to integrate these methods through the web console to avoid missing our main principle: *its speed and ease of use*.

### Understand the Clearage history

The Clearage history keeps each cleaned local storage in the console's cache memory. 

This history is based on the design principle: [**K.I.S.S.**](https://en.wikipedia.org/wiki/KISS_principle)

We have opted for simplicity by avoiding any unnecessary complexity. So the Clearage history is a simple array of objects. **Nothing more, nothing less.** Each object always has *three* properties: *key, localStorageSaved and date*.

| Properties | What they do |
|--|--|
|**key**|The *key* is a specific and distinct property between each object. It allows the use of certain actions on the Clearage history through this element   
|**localStorageSaved**|The *localStorageSaved* property contains the cleaned and saved "local storage" in the history.
|**date**|The *date* property represents the date and time, specific to your region, of the recording of the local storage within the Clearage history.|
> Note: key and date properties are automatically generated 
***

### Use the console's methods

#### 👽 How to use

To use the methods through your web console, you must keep in mind that it is necessary to use the keywords `clearage` or `clx` .

```javascript
// e.g.
clx.doSomething()
// or
clearage.doSomethingElse()
```

> **Warning!** Each of these methods operates only in the context in which they are used. To make it simple, a method cannot be used on a chrome tab other than its own.
***

#### 👾 Show the entire history

The  `showClearageHistory` method allows you to display the history of the extension on a web console.

**∙ Example**
```typescript
// from the web console
clx.showClearageHistory()
```

**∙ Screenshot**

![Show the entire history screenshot](https://github.com/ARKHN3B/Clearage/blob/master/images/screenshots/showClearageHistory.png)

***

#### 🚀 Remove an element from history

The  `removeElementFromClearageHistory` method allows you to remove an element (i.e. local storage) from the history by its key.

**∙ Example**
```typescript
// from the web console
clx.removeElementFromClearageHistory(key: number)
```

**∙ Screenshot**

![Remove an element from history screenshot](https://github.com/ARKHN3B/Clearage/blob/master/images/screenshots/removeElementFromClearageHistory.png)

***

#### 🧨 Clean all the history

The  `cleanClearageHistory` method allows you to completely clean the history. 

**∙ Example**
```typescript
// from the web console
clx.cleanClearageHistory()
```

**∙ Screenshot**

![Clean all the history screenshot](https://github.com/ARKHN3B/Clearage/blob/master/images/screenshots/cleanClearageHistory.png)

***

#### 🔦 Reset a specific local storage from history

The  `resetLocalStorageWith` method allows you to re-inject an element (i.e. local storage) by its key, from the history to the local storage of the active page. 

**∙ Example**
```typescript
// from the web console
clx.resetLocalStorageWith(key: number)
```
> If a local storage is already present, it would be saved in the Clearage history and then replaced by the new one.

**∙ Screenshot**

![Reset a specific local storage from history screenshot](https://github.com/ARKHN3B/Clearage/blob/master/images/screenshots/resetLocalStorageWith.png)

***

#### 🛠 Reset the last local storage saved in history

The  `resetLocalStorageWithLastStorageSaved` method allows you to re-inject the last recorded element (i.e. local storage) from the history to the local storage of the active page.

**∙ Example**
```typescript
// from the web console
clx.resetLocalStorageWithLastStorageSaved()
```
> If a local storage is already present, it would be saved in the Clearage history and then replaced by the new one.

**∙ Screenshot**

![Reset the last local storage saved in history screenshot](https://github.com/ARKHN3B/Clearage/blob/master/images/screenshots/resetLocalStorageWithLastStorageSaved.png)

***


#### 📡 Copy a specific local storage from history

The  `copyLocalStorageWithKey` method allows you to copy an element (i.e. local storage) of the history by its key. 

**∙ Example**
```typescript
// from the web console
clx.copyLocalStorageWithKey(key: number)
```

**∙ Screenshot**

![Copy a specific local storage from history screenshot](https://github.com/ARKHN3B/Clearage/blob/master/images/screenshots/copyLocalStorageWithKey.png)

***

#### 🔌 Copy the last local storage saved in history

The  `copyLocalStorageWithLastStorageSaved` method allows you to copy the last recorded element (i.e. local storage) of the history by its key.

**∙ Example**
```typescript
// from the web console
clx.copyLocalStorageWithLastStorageSaved()
```

**∙ Screenshot**

![Copy the last local storage saved in history](https://github.com/ARKHN3B/Clearage/blob/master/images/screenshots/copyLocalStorageWithLastStorageSaved.png)

***

#### 🔋 Set manually your local storage

The  `setLocalStorage` method allows you to inject your own states from a previously copied or received local storage.

This method can:
- inject a new local storage automatically by taking the last item saved in your clipboard

- inject a new local storage stringified (by a previous action, e.g. `copyLocalStorageWithKey`) provided as an argument
	
- inject a new local storage in the right format JSON provides as an argument
	
**∙ Example**
```typescript
// from the web console

// Automatically takes the value of your clipboard
clx.setLocalStorage()

// Injection of a stringified local storage
clx.setLocalStorage({"bundle-urls":"{\"frameworks.css\":\"https://github.githubassets.com/assets/frameworks-481a47a96965f6706fb41bae0d14b09a.css\",\"site.css\":\"https://github.githubassets.com/assets/site-d3c48f1b58ea95d9efb184fd4592b411.css\",\"github.css\":\"https://github.githubassets.com/assets/github-0003cf1223f3f480cee651b538355dcb.css\"}"})

// Injection of a local storage in the right JSON format
clx.setLocalStorage({  
  "bundle-urls":{  
	  "frameworks.css":"https://github.githubassets.com/assets/frameworks-481a47a96965f6706fb41bae0d14b09a.css",  
	  "site.css":"https://github.githubassets.com/assets/site-d3c48f1b58ea95d9efb184fd4592b411.css",  
	  "github.css":"https://github.githubassets.com/assets/github-0003cf1223f3f480cee651b538355dcb.css"
	}  
})
```
> If a local storage is already present, it would be saved in the Clearage history and then replaced by the new one.

**∙ Screenshot**

![Set manually your local storage screenshot](https://github.com/ARKHN3B/Clearage/blob/master/images/screenshots/setLocalStorage.png)

***

### Thanks for using this extension
##### If you like it, shares with your friends or with your collaborators ! 😉👍
