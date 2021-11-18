# Cypress 简介
+ 基于 JavaScript 的前端测试工具，可以对浏览器中运行的任何内容进行快速、简单、可靠的测试
+ Cypress 是自集成的，提供了一套完整的端到端测试，无须借助其他外部工具，安装后即可快速地创建、编写、运行测试用例，且对每一步操作都支持回看
+ 不同于其他只能测试 UI 层的前端测试工具，Cypress 允许编写所有类型的测试，覆盖了测试金字塔模型的所有测试类型【界面测试，集成测试，单元测试】
+ Cypress 底层协议不采用 WebDriver
<img src="https://github.com/annezhangprivate/annezhangprivate/blob/main/Cypress/Image/%E9%87%91%E5%AD%97%E5%A1%94.jpg">
<img src="https://github.com/annezhangprivate/annezhangprivate/blob/main/Cypress/Image/%E9%87%91%E5%AD%97%E5%A1%942.jpg">

# Cypress 原理

## Webdriver 运行的方式

+ 大多数测试工具（如：Selenium/webdriver）通过在外部浏览器运行并在网络上执行远程命令来运行
+ 因为 Webdriver 底层通信协议基于 JSON Wire Protocol，运行需要网络通信
 

## Cypress 运行的方式
Cypress 和 Webdriver 方式完全相反，它与应用程序在相同的生命周期里执行

## Cypress 运行测试的大致流程
1. 运行测试后，Cypress 使用 webpack 将测试代码中的所有模块 bundle 到一个 js 文件中
2. 然后，运行浏览器，并且将测试代码注入到一个空白页中，然后它将在浏览器中运行测试代码【可以理解成：Cypress 将测试代码放到一个 iframe 中运行】
 

## Cypress 运行测试的技术流程
1. 每次测试首次加载 Cypress 时，内部 Cypress Web 应用程序先把自己托管在本地的一个随机端口上【如：http://localhost:65874】
2. 在识别出测试中发出的第一个  cy.visit()  命令后，Cypress 会更改本地 URL 以匹配你远程应用程序的 Origin【满足同源策略】，这使得你的测试代码和应用程序可以在同一个 Run Loop 中运行  
 

## Cypress 运行更快的根本原因
+ Cypress 测试代码和应用程序均运行在由 Cypress 全权控制的浏览器中
+ 且它们运行在同一个Domain 下的不同 iframe 中，所以 Cypress 的测试代码可以直接操作 DOM、Window Objects、Local Storages而无须通过网络访问
 
## Cypress 稳定性、可靠性更高的原因
+ Cypress 还可以在网络层进行即时读取和更改网络流量的操作
+ Cypress 背后是 Node.js Process 控制的 Proxy 进行转发，这使得 Cypress 不仅可以修改进出浏览器的所有内容，还可以更改可能影响自动化操作的代码
+ Cypress 相对于其他测试工具来说，能从根本上控制整个自动化测试的流程
 
## Cypress 架构图
<img src="https://github.com/annezhangprivate/annezhangprivate/blob/main/Cypress/Image/%E6%9E%B6%E6%9E%84%E5%9B%BE.jpg">
