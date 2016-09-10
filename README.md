Fork [yii-loganalyzer](https://github.com/d4rkr00t/yii-loganalyzer) for yii2

### Installation ###


```
#!composer

composer require egorspk/yii2-loganalyzer
```


```
#!php

'log' => [
            'traceLevel' => YII_DEBUG ? 3 : 0,
            'targets' => [
                [
                    'class' => 'spk\yii2loganalyzer\LogAnalyzerFileTarget',
                    'levels' => ['error', 'warning'],
                ],
            ],
        ],
```

### Widget Example ###


```
#!php

 <?= \spk\yii2loganalyzer\LogAnalyzerWidget::widget([
        'log_file_path' => Yii::getAlias('@frontend') . '/runtime/logs/app.log',
    ]) ?>
```