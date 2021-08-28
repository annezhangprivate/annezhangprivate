**测试的目的是验证需求，Bug**

# 业务需求

MRD（Market Requirement Document）： 市场需求书


# 用户需求

PRD(Product Requirement Document): 产品需求文档
HPC(High Performance Compute): 高性能计算

# 软件产品需求

## 功能性需求:

### 1. 特性需求
    根据系统特性即产品所提供的主要服务来提交给用户使用的软件功能，使用户可以通过使用产品所提供的特性来执行任务，达到自己的期望。
### 2. 安全性需求
    系统安全性、完整性或与私人问题相关的需求，这些问题将会影响到产品的使用和产品所创建或使用的数据的保护。
### 3. 互操作需求
    包括硬件接口互操作、软件接口互操作，以及通信接口互操作。
    硬件接口描述系统中软件和硬件每一接口的特性。这种描述可能包括支持的硬件类型、软硬件之间交流的数据和控制信息的性质以及所使用的通信协议。
    软件接口描述该产品与其他外部组件（由名字和版本识别）的连接，包括数据库，操作系统，工具，库和集成的商业组件。
    通信接口描述与产品所使用的通信功能相关的需求，包括电子邮件、Web 浏览器、网络通信标准或协议及电子表格等，定义了相关的消息格式，规定了通信安全或加密问题、数据传输速率和同步通信机制。
    
## 非功能性需求

## 文档需求

## 项目需求优先级定义


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




