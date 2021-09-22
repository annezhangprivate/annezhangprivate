# 1. 什么是用户故事
  用户故事是一个备忘录似的交互模型，是从用户角度来描述用户渴望得到的功能。它强调的是通过有效、及时的沟通，帮助用户澄清和优化需求，用户故事有一个通用的模板，如下：
  As a role(作为一个角色)，I want to do something or a piece of functionality(通过某项功能，执行一些操作)，so that achieve some business value or statement of intent.(以便能够实现特定的目标/价值)
  用户角色（Who）
  某项功能（功能即用户能亲自执行的操作）
  实现了某个目标，获得了某种价值（Global/Value）
# 2. 用户故事特点
## 2.1 体现用户价值
  用户故事主要是为了通过某个功能来体现用户价值。
  对产品而言，永远应该把那些最能体现用户价值观的功能置于最高优先级。
## 2.2 不要出现技术术语
    一般用户故事是由用户来写的，或者由用户口述，我们的需求人员（有可能就是PM）来整理。
    注意到，一个用户故事里面的事件可以这样描述：
    1. 用户做AA
    2. 系统做BB
    3. 用户做CC
    4. 系统做DD
    5. ... ...
    用户故事只是描述系统的外在行为，以客户能够明白的方式，描述了一个系统的外在行为，它完全忽略了系统的内部动作。
## 2.3 可测试性
   不可测试的故事发生在一些非功能性的需求上。所以，可测试性意味着用户故事尽量采用功能性来做描述
# 3. 用户故事分解、细化、合并
  Epic(史诗级故事)，通俗讲就是大型的故事。本身不能直接通过其完成迭代（逐层分解）和开发，而是首先需要划分成较小的真正的用户故事。Epic分为两类：
  复合故事（compound story）:由多个小的故事组成。
  复杂故事（complex story）:本身就很大且不容易分解的故事。
## 3.1 按用户角色细化
  用户（用户组）、角色、权限
  用户所拥有的权限就是用户个人拥有的权限与该用户所在的用户组拥有的权限之和。
## 3.2 根据用户的操作细化
  CRUD(Create/Read/Update/Delete,即增删读改来细化)
## 3.3 按用户角色合并



# Example:
## Epic
![image](https://user-images.githubusercontent.com/86548745/134346235-fa2bf67c-3dd2-48a9-ab7b-dc2545e8f770.png)

![image](https://user-images.githubusercontent.com/86548745/134346189-ea899f21-e979-4fc1-a06b-a220f4aeda7b.png)


## User Story
![image](https://user-images.githubusercontent.com/86548745/134346413-f3751537-7ac1-4585-bbf0-db18c70c9b59.png)
![image](https://user-images.githubusercontent.com/86548745/134346585-9c01ffac-2922-4fc9-aa0a-852af7107317.png)

# Description
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
