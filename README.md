# phoneLucky
手机号抽奖，号码抽奖，id抽奖

# 抽奖动画的调用方法

      lucky = $('.num-bg-box .num').phoneLucky({
          resultArrs: [15321353313, 18911534676, 13301060502, 15242924432, 18842936785, 14711551245, 18915544586, 15242925576, 18988991452],
          //result : 15321353313, //此为内定值，如果为空，那么结果就是resultArrs的随机值
      })
      lucky.startFun();

## lucky为phoneLucky返回的对象，对象下有两个方法
### startFun() //为开始滚动
### stop() //为停止滚动


       //调用抽奖逻辑

        var lucky = null;
        $('.start').click(function () {
            !!lucky || (function () {
                //$.get('index.php',function(res){
                lucky = $('.num-bg-box .num').phoneLucky({
                    resultArrs: [15321353313, 18911534676, 13301060502, 15242924432, 18842936785, 14711551245, 18915544586, 15242925576, 18988991452],
                    //result : 15321353313, //此为内定值，如果为空，那么结果就是resultArrs的随机值
                })
                lucky.startFun();
                //})
            })()
        })

        $('.stop').click(function () {
            !!lucky && lucky.closeFun();
            lucky = null;
        })

演示地址 ： [http://fy.035k.com/project/phonelucky](http://fy.035k.com/project/phonelucky)

![演示一](https://github.com/515184405/file/blob/master/1.gif)


