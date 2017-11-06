
为了[将KendoUI集成并应用到Yii框架](http://vteams.com/blog/implementation-of-kendoui-with-yii-framework/)，踩坑一周，经过一系列调研，我认为在没有Telerik帮助的情况下，两者不适合同时使用，原因如下。


### 调研
Yii作为一个PHP框架，有一套自己的约定、准则、结构和规范，灵活性不高，难以顺利集成小组件，对于KendoUI组件，具体表现在

* 在数据处理发面，Yii使用DAO/ActiveRecord/Relational ActiveRecord,而KendoUI使用的是PDO，这就导致KendoUI不适应Yii的应用结构和运行逻辑，即使集成好也无法协调一致地运行

* [KendoUI和JQueryUI是有冲突的](http://jqueryuivskendoui.com/)，KendoUI本身使用JQueryUI作为它的基础框架，为了使用KendoUI，引用JQuery就需要恰当的顺序，可能与Yii引用JQuery的顺序不一致

### 实践 

* 集成KendoUI有两种方法，其一是使用Packagist上第三方开发者封装好的包，用composer来引用，但实际使用时发现有一些问题，比如所含功能不全、引用的库有未知错误；其二，KendoUI有提供PHP wrappers，直接将之引进工程目录中，也就是lib下的文件。由于第一种方法内容不全，缺少相关文档，所以采用第二种方法

* 在进行集成时发现，KendoUI的widget都依赖于自己的JQuery，而Yii也有提供自己的JQuery，由于这个冲突无法正常使用KendoUI，需要删除Yii在Asset下的JQuery，而这可能会导致其他地方出现bug

* 查看Telerik给的例子，数据部分主要是DataSource类来完成的，其使用的是PDO的方式实现直接操作数据库，数据输入输出都是经由DataSourceTransport类后转成JSON格式进行处理，这与Yii提供的ActiveRecord难以结合，不符合Yii提倡的应用运行逻辑
***
### 思考
* *KendoUI VS JQueryUI*
    在设计方提供了视图资源的情况下，是否仍需要使用KendoUI的wrappers？是为了更好的视觉，还是便利的开发，还是Gantt？
* *Framework VS Component*
    框架和组件之争，是否需要考虑，开发下一个独立模块时，还继续使用Yii框架吗？或者使用一系列Packagist上的组件？