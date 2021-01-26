[![](https://jitpack.io/v/JobGetabu/search-dialog.svg)](https://jitpack.io/#JobGetabu/search-dialog)


# SearchDialog
Android Search Dialog Library

# Setup
## 1. Provide the gradle dependency

Add it in your root build.gradle at the end of repositories:
```
	allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}
```

Add the gradle dependency to your `app` module `build.gradle` file:

```
	dependencies {
	        implementation 'com.github.JobGetabu:search-dialog:Tag'
	}

```

## 2. Initialization of the SearchDialog

#### Java
<SearchListItem> model contains id and title
``` java
      List<SearchListItem> searchListItems = new ArrayList<>();
      SearchableDialog  searchableDialog = new SearchableDialog(this, searchListItems, "Title");
```

#### Kotlin
<SearchListItem> model contains id and title
``` kotlin
    val searchableDialog = SearchableDialog(this, searchListItems, getString(R.string.country))
    searchableDialog.setOnItemSelected(this) // implement 'OnSearchItemSelected'in your Activity
```


## 3. Show the SearchDialog

``` java
        searchableDialog.show();
```

## 4. Get Selected Item from the SearchDialog

#### Java
``` java
         @Override
         public void onClick(int position, SearchListItem searchListItem) {
                searchableDialog.dismiss();
               // searchListItem.getId(); returns id
              // searchListItem.getTitle(); returns title
         }
```

#### Kotlin
``` kotlin
        override fun onClick(position: Int, searchListItem: SearchListItem) {
           searchableDialog.dismiss()
           //searchListItem.id.toString()
           //searchListItem.title
        }
```
## 5. Screen Shots

![Search Dialog](https://i.imgur.com/47IHtQH.png)
