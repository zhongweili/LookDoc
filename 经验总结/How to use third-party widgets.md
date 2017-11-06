# How to use third-party widgets

## Froala Editor
[Documentation](https://froala.com/wysiwyg-editor/docs)

#### Install and Use for Yii
> php composer.phar require --prefer-dist froala/yii2-froala-editor "*"


```
<?php echo froala\froalaeditor\FroalaEditorWidget::widget([
    'name' => 'content',
    'options'=>[// html attributes
        'id'=>'content'
    ],
    'clientOptions'=>[
        'toolbarInline'=> false,
        'theme' =>'royal',//optional: dark, red, gray, royal
        'language'=>'en_gb' // optional: ar, bs, cs, da, de, en_ca, en_gb, en_us ...
    ]
]);; ?>
```
(editor content ralated to 'name')

#### Customize the Look of the Editor

Look at this link:
[Customization](https://froala.com/wysiwyg-editor/customize)

edit online and download the CSS file

## yii2-comments

[Documentation](https://github.com/yii2mod/yii2-comments)

#### Install and Use
> php composer.phar require --prefer-dist yii2mod/yii2-comments "*"

Do not forget to configure the module.

```
// the model to which are added comments, for example:
$model = Post::find()->where(['title' => 'some post title'])->one();

<?php echo \yii2mod\comments\widgets\Comment::widget([
    'model' => $model,
    'relatedTo' => 'User ' . \Yii::$app->user->identity->username . ' commented on the page ' . \yii\helpers\Url::current(), // for example
    'maxLevel' => 3, // maximum comments level, level starts from 1, null - unlimited level. Defaults to `7`
    'showDeletedComments' => true // show deleted comments. Defaults to `false`.
]); ?>
```
(comments ralated to 'model')
#### Customize the Look of the Comments

##### Customize the view
1. cd vendor/yii2mod/yii2-comments/widgets/views
2. overwrite **index.php** **_list.php** **_newlist.php** **_form.php**

##### Customize the editor
1. cd vendor/yii2mod/yii2-comments/models
2. overwrite **getAvatar()** and **getUsername()** function in **CommentModel.php**