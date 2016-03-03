# ECharts

<a href="http://echarts.baidu.com">
    <img style="vertical-align: top;" src="./asset/logo.png?raw=true" alt="logo" height="50px">
</a>

ECharts is a free, powerful charting and visualization library offering an easy way of adding intuitive, interactive, and highly customizable charts to your commercial products. It is written in pure JavaScript and based on <a href="https://github.com/ecomfe/zrender">zrender</a>, which is a whole new lightweight canvas library.

## X轴的Label增加显示图片功能

+ 配置如下，通过`formatter`函数返回图片链接(后面加上|``text``可以在图片上面加文字)，可以相对路径/绝对路径，可以通过``textStyle``的``width``, ``height``参数控制图片宽高

	```javascript
	xAxis : [
	 {
	     type : 'category',
	     data : ['周一','周二','周三','周四','周五','周六','周日'],
	     axisLabel: {
	         formatter: function(value, index) {
	             if(value === "周一"){
	                 return 'http://www.highcharts.com/demo/gfx/sun.png|太阳';
	             }else{
	                 return value;
	             }
	         },
	         textStyle: {
	             width: 50,
	             heigth: 50
	         }
	     }
	 }
	],
	```
	
## 图例增加显示图片功能

+ 配置如下，通过`formatter`函数返回图片链接，可以相对路径/绝对路径，可以通过``imageWidth``, ``imageHeight``参数控制图片宽高

	```javascript
	legend: {
        data:['直接访问','邮件营销','联盟广告','视频广告','搜索引擎','百度','谷歌','必应','其他'],
        formatter: function(value, index) {
            if(value === "直接访问"){
                return 'http://www.highcharts.com/demo/gfx/sun.png';
            }else{
                return value;
            }
        },
        imageWidth: 50,
        imageHeight: 50
    },
	```

## Get ECharts

+ Download on [echarts.baidu.com](http://echarts.baidu.com/download.html)
+ `npm install echarts --save`

## Docs

+ [Tutorial](http://echarts.baidu.com/tutorial.html)
+ [API](http://echarts.baidu.com/api.html)
+ [Option Manual](http://echarts.baidu.com/option.html)

We will release the English doc soon:)

## License
Copyright (c) 2013, Baidu Inc.
All rights reserved.

Redistribution and use in source and binary forms, with or without
modification, are permitted provided that the following conditions are met:

1. Redistributions of source code must retain the above copyright notice, this
   list of conditions and the following disclaimer.
2. Redistributions in binary form must reproduce the above copyright notice,
   this list of conditions and the following disclaimer in the documentation
   and/or other materials provided with the distribution.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND
ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED
WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE
DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT OWNER OR CONTRIBUTORS BE LIABLE FOR
ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES
(INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES;
LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND
ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT
(INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS
SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

The views and conclusions contained in the software and documentation are those
of the authors and should not be interpreted as representing official policies,
either expressed or implied, of the FreeBSD Project.
