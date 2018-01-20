# NgELExcel
Convert json collection to excel by angular services

**exportExcel.Excel(
    collection_Object,
    title_columns,
    count
)**

## Parameters

### collection_Object :: Require
An object or an array of object

### title_columns :: optional
Set the title_columns parameter as null If you are going to using JSON property as header, otherwise create an array of headers as Example #3

### count :: optional
top of selected rows


## Examples 

### sample input collection 

    data = [{ id: 10, name: 'ehsan' }, { id: 80, name: 'moslem' }, { id: 2, name: 'iman' }, { id: 11, name: 'javad' }];
    data2 = [{ family: 'lotfi', location: 'mashhad', age: '26' }, { family: 'shahsavan', location: 'mashhad', age: '27' }, { family: 'bahrampur', location: 'torbat', age: '28' }, { family: 'bakhshabadi', location: 'yazd', age: '30' }];
    
### Example #1 

    exportExcel.Excel(data);
    
### Example #2 

    exportExcel.Excel(data, null,2)
    
### Example #3

    exportExcel.Excel(data, [
        {
            title: "rows",
            name: "#rowNumber"
        },
        {
            title: "ID",
            name: "id"
        },
        {
            title: "UserName",
            name: "name"
        }
    ],2);
    
### Example #4 

    exportExcel.Excel([data, data2])
    
### Example #5

    exportExcel.Excel([data, data2],[null,null],[2,4]);