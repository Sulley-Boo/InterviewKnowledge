### 黑盒白盒测试

**黑盒测试**也称功能测试或数据驱动测试，它是在已知产品所应具有的功能，通过测试来检测每个功能是否都能正常使用，在测试时，把程序看作一个不能打开的黑盆子，在完全不考虑程序内部结构和内部特性的情况下，测试者在程序接口进行测试，它只检查程序功能是否按照需求规格说明书的规定正常使用，程序是否能适当地接收输入数锯而产生正确的输出信息，并且保持外部信息（如数据库或文件）的完整性。

“黑盒”法着眼于程序外部结构、不考虑内部逻辑结构、针对软件界面和软件功能进行测试。“黑盒”法是穷举输入测试，只有把所有可能的输入都作为测试情况使用，才能以这种方法查出程序中所有的错误。实际上测试情况有无穷多个，因此不仅要测试所有合法的输入，而且还要对那些不合法但是可能的输入进行测试。

常用的黑盒测试方法有：等价类划分法；边界值分析法；因果图法；场景法；正交实验设计法；判定表驱动分析法；错误推测法；功能图分析法。

**白盒测试**也称为结构测试或逻辑驱动测试，是针对被测单元内部是如何进行工作的测试。它根据程序的控制结构设计测试用例，主要用于软件或程序验证。白盒测试法检查程序内部逻辑结构，对所有的逻辑路径进行测试，是一种穷举路径的测试方法，但即使每条路径都测试过了，但仍然有可能存在错误。因为：穷举路径测试无法检查出程序本身是否违反了设计规范，即程序是否是一个错误的程序；穷举路径测试不可能检查出程序因为遗漏路径而出错；穷举路径测试发现不了一些与数据相关的错误。

白盒测试需要遵循的原则有：1. 保证一个模块中的所有独立路径至少被测试一次；2. 所有逻辑值均需要测试真（true）和假（false）；两种情况；3. 检查程序的内部数据结构，保证其结构的有效性；4. 在上下边界及可操作范围内运行所有循环。

#### 常见的黑盒测试方法

1. 等价类划分

等价类划分是将系统的输入域划分为若干部分，然后从每个部分选取少量代表性数据进行测试。等价类可以划分为有效等价类和无效等价类，设计测试用例的时候要考虑这两种等价类。

2. 边界值分析法

边界值分析法是对等价类划分的一种补充，因为大多数错误都在输入输出的边界上。边界值分析就是假定大多数错误出现在输入条件的边界上，如果边界附件取值不会导致程序出错，那么其他取值出错的可能性也就很小。

边界值分析法是通过优先选择不同等价类间的边界值覆盖有效等价类和无效等价类来更有效的进行测试，因此该方法要和等价类划分法结合使用。

3. 正交试验法

正交是从大量的试验点中挑选出适量的、有代表性的点。正交试验设计是研究多因素多水平的一种设计方法，他是一种基于正交表的高效率、快速、经济的试验设计方法。

4. 状态迁移法

状态迁移法是对一个状态在给定的条件内能够产生需要的状态变化，有没有出现不可达的状态和非法的状态，状态迁移法是设计足够的用例达到对系统状态的覆盖、状态、条件组合、状态迁移路径的覆盖。

5. 流程分析法

流程分析法主要针对测试场景类型属于流程测试场景的测试项下的测试子项进行设计，这是从白盒测试中路径覆盖分析法借鉴过来的一种很重要的方法。

6. 输入域测试法

输入域测试法是针对输入会有各种各样的输入值的一个测试，他主要考虑 极端测试、中间范围测试，特殊值测试。

7. 输出域分析法

输出域分析法是对输出域进行等价类和边界值分析，确定是要覆盖的输出域样点，反推得到应该输入的输入值，从而构造出测试用例，他的目的是为了达到输出域的等价类和边界值覆盖。

8. 判定表分析法

判定表是分析和表达多种输入条件下系统执行不同动作的工具，他可以把复杂的逻辑关系和多种条件组合的情况表达的即具体又明确；

9. 因果图法

因果图是用于描述系统输入输出之间的因果关系、约束关系。因果图的绘制过程是对被测系统的外部特征的建模过程，根据输入输出间的因果图可以得到判定表，从而规划出测试用例。

10. 错误猜测法

错误猜测法主要是针对系统对于错误操作时对于操作的处理法的猜测法，从而设计测试用例

11. 异常分析法

异常分析法是针对系统有可能存在的异常操作，软硬件缺陷引起的故障进行分析，分析发生错误时系统对于错误的处理能力和恢复能力依此设计测试用例。

#### 常见的白盒测试方法

1. 静态测试：

不用运行程序的测试，包括代码检查、静态结构分析、代码质量度量、文档测试等等，它可以由人工进行，充分发挥人的逻辑思维优势，也可以借助软件工具（Fxcop）自动进行。

2. 动态测试

需要执行代码，通过运行程序找到问题，包括功能确认与接口测试、覆盖率分析、性能分析、内存分析等。

白盒测试中的逻辑覆盖包括语句覆盖、判定覆盖、条件覆盖、判定/条件覆盖、条件组合覆盖和路径覆盖。六种覆盖标准发现错误的能力呈由弱到强的变化：

1.语句覆盖每条语句至少执行一次。

2.判定覆盖每个判定的每个分支至少执行一次。

3.条件覆盖每个判定的每个条件应取到各种可能的值。

4.判定/条件覆盖同时满足判定覆盖条件覆盖。

5.条件组合覆盖每个判定中各条件的每一种组合至少出现一次。

6.路径覆盖使程序中每一条可能的路径至少执行一次。

### 常见的测试用例

#### 用户登录界面测试

一、功能测试

1.输入正确的用户名和密码，点击提交按钮，验证是否能正确登录。

2.输入错误的用户名或者密码,验证登录会失败，并且提示相应的错误信息。

3.登录成功后能否能否跳转到正确的页面

4.用户名和密码，如果太短或者太长，应该怎么处理

5.用户名和密码，中有特殊字符（比如空格），和其他非英文的情况

6.记住用户名的功能

7.登陆失败后，不能记录密码的功能

8.用户名和密码前后有空格的处理

9.密码是否非明文显示显示，使用星号圆点等符号代替。

10.牵扯到验证码的，还要考虑文字是否扭曲过度导致辨认难度大，考虑颜色（色盲使 用者），刷新或换一个按钮是否好用

11.登录页面中的注册、忘记密码，登出用另一帐号登陆等链接是否正确

12.输入密码的时候，大写键盘开启的时候要有提示信息。

13.什么都不输入，点击提交按钮，检查提示信息。

二、界面测试

1.布局是否合理，testbox和按钮是否整齐。

2.testbox和按钮的长度，高度是否复合要求。

3.界面的设计风格是否与UI的设计风格统一。

4. 界面中的文字简洁易懂，没有错别字。

三、性能测试

1.打开登录页面，需要的时间是否在需求要求的时间内。

2.输入正确的用户名和密码后，检查登录成功跳转到新页面的时间是否在需求要求的时间内。

3.模拟大量用户同时登陆，检查一定压力下能否正常登陆跳转。

四、安全性测试

1.登录成功后生成的Cookie，是否是httponly (否则容易被脚本盗取)。

2.用户名和密码是否通过加密的方式，发送给Web服务器。

3.用户名和密码的验证，应该是用服务器端验证， 而不能单单是在客户端用javascript 验证。

4.用户名和密码的输入框，应该屏蔽SQL注入攻击。

5.用户名和密码的的输入框，应该禁止输入脚本 （防止XSS攻击）。

6.防止暴力破解，检测是否有错误登陆的次数限制。

7.是否支持多用户在同一机器上登录。

8.同一用户能否在多台机器上登录。

五、可用性测试

1.是否可以全用键盘操作，是否有快捷键。

2.输入用户名，密码后按回车，是否可以登陆。

3.输入框能否可以以Tab键切换。

六、兼容性测试

1.不同浏览器下能否显示正常且功能正常（IE,6,7,8,9, Firefox, Chrome, Safari,等）。

2.同种浏览器不同版本下能否显示正常且功能正常。

3.不同的平台是否能正常工作，比如Windows, Mac。

4.移动设备上是否正常工作，比如Iphone, Andriod。

5.不同的分辨率下显示是否正常。

七、本地化测试

1.不同语言环境下，页面的显示是否正确。

#### 朋友圈点赞功能测试

1.是否可以正常点赞和取消；

2.点赞的人是否在可见分组里；

3.点赞状态是否能即时更新显示；

4.点赞状态，共同好友是否可见；

6.性能检测，网速快慢对其影响；

7.点赞显示的是否正确，一行几个；

8.点赞是否按时间进行排序，头像对应的是否正确；

9.是否能在消息列表中显示点赞人的昵称、5.不同手机，系统显示界面如何；

备注；

10.可扩展性测试，点赞后是否能发表评论；

11.是否在未登录时可查看被点赞的信息。

#### 购物车测试
