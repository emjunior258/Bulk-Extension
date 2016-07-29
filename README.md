# Bulk-Extension
Bulk data manipulation extension for Hi-List component.
This component adds a checkbox to all

## Download it
Just click [here](https://talk-code.github.io/releases/get/bulk-extension/bulk.js).


## Using it
### Enabling it
```html

    <list ...each="row" repeatable-element=".row" extensions="bulk"
             bulk-placeholder=".checkbox" bulk-key="id"...>

       <!--Some stuff might be placed here-->

       <div class="row">


            <span class=".checkbox">
                <!--The checkbox will be placed here by bulk extension-->
            </span>

            {{row.property}}

       </div>

       <!--Other stuff might be placed here-->


    </list>

```

#### Explaining the attributes
##### bulk-placeholder
**This a mandatory attribute**. It defines a jQuery selector to be used on every instance of the repeated element to find the element where
the checkbox should be placed.

##### bulk-key
Defines the attribute that should be used as the checking key for each matched row.
This attribute is not mandatory and its default value is "id".

### Operations
The Bulk Extension adds its functions to the Hi-List instance in order to allow you to perform bulk operations
easily.

#### Checking all visible rows
```javascript

    $scope.myList.checkAll();

```
#### Unchecking all
```javascript

    $scope.myList.uncheckAll();

```

#### Getting the checked items
```javascript

    //This will return an array of ids
    $scope.myList.getAllChecked();


```

#### Clearing checked items
```javascript

    //Unchecks all checked rows, not only the visible ones
    $scope.myList.clearChecked();

```