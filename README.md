# Laravar-admin 图片管理拓展

## 依赖

  -    | 版本  
 ---- | ----- 
 php  | >=7.0.0 
 laravel-admin  | >=~1.6 

## 安装

### composer 安装

```
composer require yelphp/narwhalformmedia
```


### 发布资源

```
php artisan vendor:publish --provider=Narwhal\FormMedia\FormMediaServiceProvider
```

## 使用

#### 单图 数据库结构 varchar

##### 可删除

```
$form->photo('photo','图片')->limit(1)->remove(true)->help('单图，可删除');
```

##### 不可删除

```
$form->photo('photo','图片')->limit(1)->remove(false)->help('单图，可删除');

$form->photo('photo','图片')->limit(1)->help('单图，可删除');
```

#### 多图 数据库结构 json

```
$form->photos('photo','图片')->limit(9)->remove(true);  //可删除

```

### 参数说明
```
limit(int)      ： 图片限制条数
remove(boolean) :  是否有删除按钮
```



