# Game-based-on-python
基于Python的pygame库设计实现的游戏，包含以下游戏:
1.人机五子棋
2.扫雷
3.飞机大战

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


3.1 数据结构设计
3.1.1对界面的设计   
    

 


3.1.2 点亮小方格
 
数据结构设计完毕



3.2 面向对象设计
3.2.1    定义对象——贪吃蛇
给对象定义初始坐标与初始长度和方向
起始坐标	（5,9）
（蛇头）	（6,9）
（蛇脖子）	（7,9）
（蛇身）	（8,9）
（蛇身）	（9,9）
（蛇尾）
初始长度	5	
方向标志	1（上）	2（下）	3（左）	4（右）	起始方向	1

 


3.2.2  定义对象---食物

定义食物的大小

初始食物列	15
初始食物行	15

 


3.3 核心算法分析
3.3.1 移动算法--蛇的移动：身体随着头动
 
贪吃蛇结构示意图

1）先保存原来的头
x, y = self.body_x[0], self.body_y[0]

2）头再动时坐标变化
向上（1）	if self.d == 1: self.body_x[0] -= 1
向下（2）	if self.d == 2: self.body_x[0] += 1
向左（3）	if self.d == 3: self.body_y[0] -= 1
向右（4）	if self.d == 4: self.body_y[0] += 1
      

3）身子跟着动
原来身子除身子的第一个小方格外的后部分(即蛇身和蛇尾),接替原来是身子的部分 i=4,3,2最前的小方格
条件	i in range(self.len - 1, 0, -1)
变化	self.body_x[i] = self.body_x[i - 1]
self.body_y[i] = self.body_y[i - 1]

原来身子的第一个小方格(即蛇脖子),接替原来的头
self.body_x[1], self.body_y[1] = x, y




 
红色为蛇头，蓝色为蛇身和蛇尾，黑色为移动留下印记（示意图）

3.3.2  吃食物
头与食物坐标一样则吃到食物，身体长度加一，而新食物随机出现
吃到食物条件	food.x = snake.body_x[0] 
food.y = snake.body_y[0]
整个身体变化	self.body_x.append(food.x)
self.body_y.append(food.y)
长度变化	snake.len = snake.len + 1
新食物刷新范围	food.x = random.randint(1, 24);
food.y = random.randint(1, 24);
 
 
 

3.3.3判断碰壁死亡
碰上壁	X[0]<0
碰下壁	X[0]>25
碰左壁	Y[0]<0
碰右壁	Y[0]>25

3.3.4 判断被自己咬死
咬死条件	snake.body_x[0]==snake.body_x[i]
snake.body_y[0]==snake.body_y[i]

3.3.5 时间变化
未成年速度	n=100
成年后速度变化	100 - int(snake.len / 2)
最快速度	n=10

3.3.6 开始延迟
游戏延迟	if (snake.len <= 15):
    pygame.time.wait(100)
游戏开始延迟次数	i=6
游戏开始延迟时间	if i > 0:
    pygame.time.wait(40 + i * 30)
    i -= 1

3.3.7 游戏结束检测
是否撞墙	是则设置flag=1，反之，不改变flag的状态值
是否咬到自己	是则设置flag=1，反之，不改变flag的状态值
弹出游戏结束提示
	font = pygame.font.SysFont('arial', 40)
text = font.render('Game Over!', True, [255, 0, 0])
screen.blit(text, [160, 220])
pygame.display.update()





四、项目实现
4.1 基础界面的绘制实现代码
# 绘制网格
def drawGird():
    i = 0
    while i <= 400:
        pygame.draw.line(screen, [0, 0, 0], [0, i], [400, i], 1)
        pygame.draw.line(screen, [0, 0, 0], [i, 0], [i, 400], 1)
        i += 20

4.2点亮方格实现代码
# 点亮第x行y列的小方块
def drawRect(x, y):
    pygame.draw.rect(screen, [200, 200, 200], [[(y - 1) * 20 + 1, (x - 1) * 20 + 1], [19, 19]])
4.3创建对象实现代码
# 食物类
class Food:
    def __init__(self):
        # 食物初始化在12行12列位置
        self.x = 12
        self.y = 12

    def show(self):
        drawRect(self.x, self.y)


# 蛇类
class Snake:
    def __init__(self):
        # 蛇的身体坐标集合；以第一个元素为蛇头
        self.body_x = [5, 6, 7, 8, 9]
        self.body_y = [9, 9, 9, 9, 9]
        # 长度
        self.len = 5
        # 方向1234代表上下左右
        self.d = 1
4.4 对象的显示代码实现
def show(self):
    for i in range(0, len(self.body_x)):
        drawRect(self.body_x[i], self.body_y[i])
4.5 贪蛇的移动代码实现
# 蛇的移动
def move(self):

    # 1.先保存原来的头
    x, y = self.body_x[0], self.body_y[0]
    # 2.头再动
    if self.d == 1: self.body_x[0] -= 1
    if self.d == 2: self.body_x[0] += 1
    if self.d == 3: self.body_y[0] -= 1
    if self.d == 4: self.body_y[0] += 1
    # 3.身子跟着动
    # 原来身子除身子的第一个小方格外的后部分,接替原来是身子的部分 i=4,3,2最前的小方格
    for i in range(self.len - 1, 0, -1):
        self.body_x[i] = self.body_x[i - 1]
        self.body_y[i] = self.body_y[i - 1]
    # 原来身子的第一个小方格,接替原来的头
    self.body_x[1], self.body_y[1] = x, y
    print(self.body_x)
    print(self.body_y)

4.6吃食物的代码实现

# 判断蛇吃食物
if snake.body_x[0] == food.x:
    if snake.body_y[0] == food.y:
        print("吃到食物了")
        snake.eat(food)
        # 新的食物随机出现
        food.x = random.randint(1, 24)
        food.y = random.randint(1, 24)

# 吃食物
def eat(self, food):
    self.body_x.append(food.x)
    self.body_y.append(food.y)
    self.len += 1

4.7 按键的设置代码实现
# 循环接收事件
for event in pygame.event.get():
    # 退出
    if event.type == pygame.QUIT:
        exit()
    if event.type == pygame.KEYDOWN:
        # 修改蛇的方向
        if event.key == pygame.K_UP and snake.d != 2: snake.d = 1
        if event.key == pygame.K_DOWN and snake.d != 1: snake.d = 2
        if event.key == pygame.K_LEFT and snake.d != 4: snake.d = 3
        if event.key == pygame.K_RIGHT and snake.d != 3: snake.d = 4
4.8 游戏结束代码实现
游戏主循环外
# 游戏状态标志，0进行1结束
flag = 0

游戏主循环内
# 游戏结束检测
def checkGameOver(snake):
    global flag
    # 是否撞墙
    if snake.body_x[0] > 25 or snake.body_x[0] < 1 or snake.body_y[0] > 25 or snake.body_y[0] < 1:
        # 设置游戏结束
        flag = 1
    # 是否被咬死
    if snake.len > 5:
        for i in range(3, snake.len - 1):
            if snake.body_x[0] == snake.body_x[i]:
                if snake.body_y[0] == snake.body_y[i]:
                    # 设置游戏结束
                    flag = 1
                    break

# 游戏结束检测
checkGameOver(snake)
# 判断游戏是否
if flag == 1:
    # 弹出游戏结束提示
    font = pygame.font.SysFont('arial', 40)
    text = font.render('Game Over!', True, [255, 0, 0])
    screen.blit(text, [160, 220])
    pygame.display.update()
# 蛇移动
else:
    # 游戏未结束蛇继续移动
    snake.move()

4.9 蛇速度变化代码实现
# 游戏延迟
if (snake.len <= 15):
    pygame.time.wait(100)
else:
    # 长度达到15,蛇成年,其移动速度跟其长度线性相关
    if 100 - int(snake.len / 2)>10:
        pygame.time.wait(100 - int(snake.len / 2))
4.10 游戏开始延迟实现代码
游戏主循环外
# 游戏开始延迟次数
i = 6

游戏主循环内
# 游戏开始延迟
if i > 0:
    pygame.time.wait(40 + i * 30)
    i -= 1
