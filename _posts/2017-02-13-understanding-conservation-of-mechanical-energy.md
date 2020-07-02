---
title: "对于机械能守恒定律的应用条件的理解"
date: "2017-02-13"
---

“在只有重力和弹力做功的物体系统内，动能与势能可以相互转化，而总的机械能保持不变。”

我们看到，机械能守恒定律是有条件的，这个条件是除了重力和弹力，其他的力都不接受，为什么呢？

这里就要引入非保守力的概念了，因为非保守力参与整个过程的时候，有一些能量会悄悄地跑掉，这时候如果你没发现你所研究的过程有非保守力的参与的话，你想知道那些能量都是怎么变化的就很不清晰了。非保守力一参与进来的话，能量就都不守恒了。

非保守力 (nonconservative force) 做功的时候是和曲径有关系的，就像摩擦力那样，因为摩擦力就算大小不变，方向也随着位移而不断变化，所以必须一小段一小段的积分。而摩擦力的方向又等于这时候的位移方向，所以就是 功=$latex F $ \* 曲径，我们发现$latex \\cos{\\theta}$ 永远是1，摩擦力还效率挺高的，自己的力量一点都不浪费，全都用去偷走能量了。那么摩擦力就是非保守力了，沿任意闭合路径作功不等于零。（详见费曼的物理学讲义14-1对于非保守力的描述）

* * *

以下是很容易理解的功能关系

$latex W\_{net force} = \\Delta E\_{kinetic}$ 【动能定理】

$latex W\_{conservative Force} = - \\Delta E\_{potential}$ 【势能定理】

$latex W\_{nonconservative force} = \\Delta E\_{mechanical}$ 【机械能定理】

$latex - W\_{f\_{sliding}} = Q$ 【摩擦热定理】（名称是按照逻辑取的，当然这些定理是什么名字不是那么的重要）

$latex - W\_{ampere force} = Q$ 【电流热定理】

我们来看机械能定理，这里写的是非保守力做功 等于 机械能的变化，我们想这个机械能变化是从那里产生的？机械能是动能与势能的总和，这个总和应该是不会变的，因为能量不能创造和毁灭。那么这个机械能的变化一定是因为原来那些总和的能量跑掉了，而且是贡献给了不属于动能和势能的那部分能量。所以是由于非保守力的作用，摩擦力做功的时候会让原本的总能量中的一部分能量去生热，那么这种热也是一种能量，称之为热能。哦！我们发现机械能里面可不包括热能，那既然这样，机械能的的确确是会发生变化的，这就是$latex \\Delta E\_{mechanical energy}$的由来。  
  
如果我们从更加微观的角度观察摩擦力所造成的影响，那么我们就会发现，摩擦力的存在会让物体的边边上那一堆分子运动的更快，摩擦力做了一些功，驱动了那些分子，让它们的运动速度增大，这样就增加了这些分子的动能，这样就会让你感觉到这个物体好像变热了（详见费曼物理学讲义第I卷中 Atoms in Motion 那一章从分子运动的角度观察世界，解释为什么分子运动的快就会变热），所以这种热能实际上是分子的动能，那好，这时候所有的能量变化又回到了正常的机械能守恒，所以我们又可以用机械能守恒定律了。所以机械能是相对守恒的，就看你是喜欢生活在更大的世界中还是更小的世界中了。

* * *

现在我们用摩擦力参与运动过程来验证一下最上面的两个定理有没有道理：  
首先要清楚的是动能定理描述的是物体的动能变化与力量在物体上做功的关系，势能定理描述的是物体本身所具有的势能的变化与力量在物体上做功的关系。  
  
动能定理：如果摩擦力参与进来的话，它是会对运动造成阻碍从而影响一个物体运动的速度，那就影响了它的动能，所以摩擦力做功要算进来，也就是非保守力做功，所以就是物体受到的所有力做功都要算进来。  
  
势能定理：假设我抛起一个物体然后又在同样的高度接住，显然势能没有变。如果摩擦力参与进来的话，它就会对物体运动产生阻碍，还加热了物体，物体在空中运动的过程中，动能转化成了热能，物体初始的动能是我提供给它的，初始动能中的一小部分能量在空中被摩擦力生热了。非保守力做了功，在这个过程中势能却没有变化，现在我们在意的是物体本身势能的变化，所以势能定理只接受保守力。重力先做了负功，又做了正功，这些功相互抵消了，重力做功是0 等于 重力势能的变化是0。  
  
那么我们可以仔细想一想上面两个分析说明了什么？  
这就是，非保守力会打扰到动能的变化，同时会影响势能的时变率，但非保守力不会影响势能变化的开始和结果。有非保守力参与时，势能变化会慢一些，但最终势能要变化多少还是会变化多少的。