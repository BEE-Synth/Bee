# Bee-File

In the file management domain, Bee uses one table schema.
Each file (excluding folder) is a row in the table.
Attributes include basename, extension, file path, modTime, etc.

For instance, below is the table of example input files in Hades01.

```
----------------------------------------------------------------------------------------------------------------------------------------
|Fid   |Basename|Extension|FilePath|Size  |ModTime         |Readable|Writable|Executable|Group  |Year |Month|Day  |YearS |MonthS|DayS  |
|MyFile|String  |String   |String  |Int32 |DateTime        |Boolean |Boolean |Boolean   |String |Int32|Int32|Int32|String|String|String|
----------------------------------------------------------------------------------------------------------------------------------------
|i1    |members |csv      |./      |8132  |2016/6/5 0:00:00|True    |True    |False     |public |2016 |6    |5    |2016  |6     |5     |
|i2    |diaries |csv      |./      |202818|2016/6/5 0:00:00|True    |True    |False     |secrete|2016 |6    |5    |2016  |6     |5     |
|i3    |manual  |pdf      |./      |20329 |2016/6/5 0:00:00|True    |True    |False     |public |2016 |6    |5    |2016  |6     |5     |
|i4    |logs    |txt      |./      |996   |2016/6/5 0:00:00|True    |True    |False     |public |2016 |6    |5    |2016  |6     |5     |
----------------------------------------------------------------------------------------------------------------------------------------
```

The user actions include common user actions, e.g., rename, unzip, move.

The `FileEntity.cs` specifies the detailed schema and actions using the annotation APIs provided by Bee.
