#### 问题描述

在页面中使用ActiveForm时，如果使用了多个Button，点击每一个Button，都会触发所有Button的动作。

#### 原因分析
页面中Yii的ActiveForm，在渲染时会自动加载隐藏的JS。

#### 调研结果

这是yiisoft/yii2的一个issue，见[这个页面](https://github.com/yiisoft/yii2/issues/10555)
![](http://p1.bpimg.com/567571/bb1dbb8e472723d7.png)

#### 解决方法

如果是多个SubmitButton，给它们设置相同的name='submit'，不同的value，而后
> public function actionAcceptUserSubmit() {
>
>        if(isset($_POST['button1']))
>        {
>        echo "Accept code here ";
>        }
>      if(isset($_POST['button2']))
>        {
>        echo "Reject code here ";
>        }
> }

如果是还有除了SubmitButton之外的其他按钮，则要对它们设置不同的name，然后在Controller里if语句判断

> if(\Yii::$app->request->post('submit1')=='button1') {
>    
> }