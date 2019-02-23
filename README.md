一、Sonar介绍
Sonar是一个代码质量管理的开源平台，用于管理源代码的质量，通过插件形式，可以支持包括java、C#、JavaScript等二十余种编程语言的代码质量管理与检测。

Sonar是从七个维度检测代码质量，而作为开发人员至少需要处理前5中代码质量问题。

1、不遵循代码标准

sonar可以通过PMD，CheckStyle，Findbugs等代码规则检测工具规范代码编写

2、潜在的缺陷

sonar可以通过PMD，CheckStyle，Findbugs等代码规则检测工具检测出潜在的缺陷

3、糟糕的复杂度分布

文件、类、方法等，如果复杂度过高将难以改变，这会使得开发人员难以理解它们，且没有自动化的单元测试，对于程序中的任何组件的改变都将可能导致需要全面的回归测试

4、重复

显然程序中包含大量复制粘贴的代码是质量低下的，sonar可以展示源码中重复严重的地方

5、注释不足或者过多

没有注释将使代码可读性变差，特别是当不可避免出现人员变动时，程序的可读性大幅度下降，而过多的注释又会使得开发人员将奖励过多的花费在阅读注释上，亦违背初衷

6、缺乏单元测试

sonar可以很方便地统计并展示单元测试覆盖率

7、糟糕的设计

通过sonar可以找出循环，展示包与包、类与类之间相互依赖关系，可以检测自定义的架构规则 通过sonar可以管理第三方的jar包，可以利用LCOM4检测单个任务规则的应用情况，检测耦合。

补充：PMD，CheckStyle，Findbugs这些工具都叫静态代码分析工具。何为静态代码分析？静态代码分析是指无需运行被测代码，仅通过分析或检查源程序的语法、结构、接口等来检查程序的正确性，找出代码隐藏的错误或缺陷，如参数不匹配，有歧义的嵌套语句，错误的递归，非法计算，空指针引用等。

\

二、Sonar工具介绍
1、sonarqube

sonarqube 是 sona r的服务端，相当于一个web服务器，用来发布应用，在线浏览、配置分析等。目前官网最近版本为sonarqube-7.3。sonarqube如下所示。怎么样？有没有很面熟的感觉？是不是和tomcat特别像呢？

下面简单说一下每个文件夹的作用

bin：sonarqube运行命令文件夹

conf：sonarqube配置文件夹

data：嵌入式数据库的数据（H2数据库引擎），建议只用于测试和演示

extensions：sonarqube的插件等存放文件夹

lib：sonarqube存放的运行库文件夹（jar）

logs：sonarqube日志文件夹

temp：sonarqube临时文件夹

web：sonarqube系统UI界面文件夹

\

2、sonarqube-scanner
sonarqube-scanner相当于sonar客户端，目前最新版本为sonar-scanner3.0。sonarqube-scanner如下图所示。每个文件夹的作用和sonar类似，具体不在赘述。

3、sonarlint
SonarLint相当于sonar的一个插件，它及时反馈给开发人员新的bug和质量问题。是常用IDE的一个扩展。如Eclipse、VS、IntelliJIDEA。
