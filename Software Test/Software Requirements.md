**测试的目的是验证需求，Bug**

# 业务需求

MRD（Market Requirement Document）： 市场需求书


# 用户需求

PRD(Product Requirement Document): 产品需求文档
HPC(High Performance Compute): 高性能计算

# 软件产品需求

## 1. 功能性需求:

### 1.1 特性需求
    根据系统特性即产品所提供的主要服务来提交给用户使用的软件功能，使用户可以通过使用产品所提供的特性来执行任务，达到自己的期望。
### 1.2 安全性需求
    系统安全性、完整性或与私人问题相关的需求，这些问题将会影响到产品的使用和产品所创建或使用的数据的保护。
### 1.3 互操作需求
    包括硬件接口互操作、软件接口互操作，以及通信接口互操作。
    硬件接口描述系统中软件和硬件每一接口的特性。这种描述可能包括支持的硬件类型、软硬件之间交流的数据和控制信息的性质以及所使用的通信协议。
    软件接口描述该产品与其他外部组件（由名字和版本识别）的连接，包括数据库，操作系统，工具，库和集成的商业组件。
    通信接口描述与产品所使用的通信功能相关的需求，包括电子邮件、Web 浏览器、网络通信标准或协议及电子表格等，定义了相关的消息格式，规定了通信安全或加密问题、数据传输速率和同步通信机制。
    
## 2. 非功能性需求：
    指软件产品为满足用户业务需求而必须具有且除功能需求以外的特性，包括系统的性能、易用性、可靠性、可维护性、可支持性、可扩展性、可移植性以及对技术和对业务的适应性等。
### 2.1 性能（Performance）:
    响应时间、吞吐量、准确性、有效性、资源利用率（如要求系统能满足100个人同时使用，页面反应时间不能超过6秒）
### 2.2 易用性（Usability）:
    人性化因素、帮助、文档
### 2.3 可靠性（Reliability）:
    故障频率（如系统能7*24小时连续运行，年非计划宕机时间不能高于8小时)、可恢复性（系统出现故障时，能够快速切换到备用机）、可预测性
### 2.4 可支持性（Supportability）:
    适应性、可维护性、国际化、可配置性
### 2.5 可移植性（Portability）:
    是否有对原来产品进行软件硬件迁移的支持？迁移过程中是否有兼容性的要求？

## 3. 文档需求：
    文档需求列举出将与软件一同发行的用户文档部分，例如用户手册、在线帮助和教程，并明确所有已知的用户文档的交付格式或者标准。
## 4. 项目优先级:
    P1：是强制性的一定要完成的模块，如果出现问题，将会影响项目发布。
    P2：对项目发布非常重要，但是如果出现问题也不会影响项目发布（具体由项目经理决定）
    P3：重要， 但不是强制性的或预期的一定要发布。
 
# 审核（Review）软件产品需求
    一个合理的需求文档有如下特性：
    1. 完整性
    2. 正确性
    3. 一致性
## 1. 完整性：
    指不应该遗漏要求和必须的信息
### 1.1 演绎法:
### 1.2 比较法:
### 1.3 分解法:
### 1.1 打标签:



# Example:

## User Story
As a Content Creator, I want the ability to create a text link using the universal link so that I don't have to find the link separately and I can be sure that if content moves in the future that the link will not break. 

## Additional Context
Many of our customers will create a text link that links to a piece of content within Seismic. Right now this has to be done manually and it is not considered best practice due in part to the fact that if the content being linked to is moved to a new location, that link will break. 

We'd like to introduce the ability to link to a piece of Seismic content directly as a part of creating a text link (much like the DocList or Navigation widgets we have today).

## Requirements
<ul>
<li> New option added to the dialog box for link creation that reads “Internal URL” </li>
<li> Update the current “URL” option to read “External URL” 
<ul>
<li>No changes to functionality in this section, just updating the label</li>
</ul>
</li>
<li> Order of link options should be:
<ul>
<li>“Internal URL” (selected by default)</li>
<li>“External URL”</li>
<li>“Email”</li>
</ul>
</li>
<li> When “Internal URL” is selected, user should see a button reading “Add Content” </li>
<ul>
<li>This button design should match the same “Add Content” button visible in the DocList content selector</li>
</ul>
<li> Clicking “Add Content” should display UCP </li>
<ul>
<li>This means user can:</li>
</ul>
<ol>
<li>link to Library or Profile content</li></li></li>

<li>use “search” to find their content</li></li>

<li>link directly to a folder</li>
</ol>
<li> User can only link to a single item (no multi-select like DocList) </li>
<ul>
<li>NOTE: this is an initialization parameter that is provided by UCP</li>
</ul>
<li> User has the option to set link to “Open in New Window” (default should be same window) </li>

<li> Links do not break when content is moved to a new location via Content Manager </li>

<li> User has the option to “Cancel” </li>
<ul>
<li>If user clicks cancel, they should be redirected back to the Page editor
</ul>
<li> User can select “Remove Link” like they can with other link types </li>

<li> The link should respect profiles/permissions </li>
<ul>
<li>If the user viewing the page has access to the content that has been linked, allow user to click link and navigate to content
</ul>
<ul>
<li>If the user viewing the page does not have access to the content that has been linked, do the following:
</ul>
<ol>
  <li>Disable click event

  <li>Do not change cursor from arrow to hand

  <li>Show tooltip on hover that reads “You do not have access to this content”
</ol>
<li> Need to use the new “Highlight” option for any input that is selected  </li>
<ul>
<li>NOTE: This is a part of the new design system that changes the border color of the input when it is focused to make it clear to the user where they are in the UI. See Figma designs for more details
</ul>
 </ul>




