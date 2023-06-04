## 创建数据库
`use test`
## 展示数据库
`show dbs`
## 删除数据库
`db.dropDatabase()`
## 插入语句
`db.test.insertOne("name":"dy")`
## 创建集合
`db.createCollection("list")`
## 查看集合
`show collections / show tables`
## 创建带参数集合
```cpp 
db.createCollection("myTables",{
    {capped: true ,autoIndexId: true,size:1<<10,max:1000}
})
```
## 删除集合
`db.collection.drop()`
## 插入文档
`db.collectionName.insert(document)`
`db.collectionName.save(document)` 
```cpp
db.collectionName.insertOne(
    <document>,
    {
        writeConcern:<document>
    }
)```
```cpp
db.collectionName.insertMany(
    [<document1>,<document2>,..],
    {
        writeConcern:<document>,
        ordered:<boolean>
    }
)
```
## 删除文档
```cpp

db.collection.remove(
    <query>,
    {
        justOne:<boolean>,
        writeConcern:<document>
    }
)
```
## 查询文档
`db.collection.find(query,projection)`
