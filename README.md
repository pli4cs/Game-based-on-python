# Game-based-on-python
基于Python的pygame库设计实现的游戏

## For example：贪吃蛇游戏
### 介绍
在该游戏中，玩家通过键盘的上下左右键来对贪吃蛇的头部进行控制，来完成自身的移动。此外，当玩家控制贪吃蛇移动时，只被允许往前、往左和往右移动，不被允许往后移动，即后退，而贪吃蛇的食物则是通过是使用random库生成随机数，随机的出现在游戏界面内，从而完成了食物在地图上随机出现的效果。贪吃蛇吃到食物之后，其长度会自动加一，并且其长度增加到一定值后，即蛇成年后，蛇移动的速度开始变化，这时其移动速度跟其长度线性相关，而速度的改变基于游戏延迟快慢来实现的。总的来说长度越长，蛇的速度会越快。当他咬到自己身体的时候，或者撞墙之后就会死亡，然后，弹出“Game Over！”提示游戏结束，蛇将不能移动。
### 数据结构设计
#### 对界面的设计
<img width="683" height="210" alt="94605fb402b1c7eb8e283ccd0b108593" src="https://github.com/user-attachments/assets/db94a4e1-7dd9-432a-a200-54b0adb53f99" />
<img width="424" height="238" alt="fcd45a907ba1c5086eb07f9af93d3b1a" src="https://github.com/user-attachments/assets/3a088aef-9d3e-46ba-a066-3d8746ff4597" />

#### 点亮小方格
<img width="601" height="192" alt="88aa4e843d234c6bd2be7e17b6dd907a" src="https://github.com/user-attachments/assets/ac694049-6e62-4622-89ca-ecce67e10922" />

### 面向对象设计
#### 定义对象——贪吃蛇
给对象定义初始坐标与初始长度和方向
<img width="823" height="274" alt="image" src="https://github.com/user-attachments/assets/edef9177-8cea-42c2-9528-a4463aca2e10" />
<img width="493" height="260" alt="0c76f3b170ccc4188a2b96013097de28" src="https://github.com/user-attachments/assets/09850547-7ef4-41c7-bb70-c89b86646fdc" />

#### 定义对象---食物
定义食物的大小
<img width="830" height="92" alt="image" src="https://github.com/user-attachments/assets/9b051dca-b3be-4edc-a6a0-c5b81fad2b18" />
<img width="320" height="230" alt="9806360b2cc628c26ec9f0a4da13c204" src="https://github.com/user-attachments/assets/54e51c71-7415-438f-be3f-ff87fff1d9e5" />

### 核心算法分析
#### 移动算法--蛇的移动：身体随着头动

<img width="148" height="306" alt="c59baaecb5c5fc7e613b6dd561bc3fa4" src="https://github.com/user-attachments/assets/4181a9cf-75c9-48c4-9b26-d3c18e05c8cc" />
贪吃蛇结构示意图

<img width="342" height="237" alt="717f0080d0ad3e05b4de139ab09817fd" src="https://github.com/user-attachments/assets/ea274a78-7d8d-4cc4-ae8b-c159102b8dd2" />
红色为蛇头，蓝色为蛇身和蛇尾，黑色为移动留下印记（示意图）

### 功能测试
#### 吃食物与控制
<img width="632" height="665" alt="b53c0b6bfbd64d3cd3b33154e2c13423" src="https://github.com/user-attachments/assets/e10c35c5-8ff4-4e19-bc14-721d9f4fff9a" />
<img width="627" height="668" alt="image" src="https://github.com/user-attachments/assets/49bd7fe5-ef0a-49e6-ba23-2835ccc45363" />

#### 被咬死
<img width="629" height="667" alt="image" src="https://github.com/user-attachments/assets/a431a904-65a9-46c2-a48d-1ffea7632ee4" />

#### 被撞死了
<img width="633" height="670" alt="image" src="https://github.com/user-attachments/assets/dd864da6-7053-4b3f-96ad-437f68a258b4" />

#### 吃到食物变长
<img width="633" height="670" alt="6df656513e70a29472da35e4ccb43876" src="https://github.com/user-attachments/assets/4a1a9cfb-f969-42bb-b546-7852f26cdbea" />
<img width="626" height="664" alt="63408076940186cfe5696fc90749215d" src="https://github.com/user-attachments/assets/8690ff8b-75b7-49ea-ba24-9b37a44ee174" />
