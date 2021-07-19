**测试的目的是验证需求，Bug**

# 业务需求：

MRD（Market Requirement Document）： 市场需求书








# 用户需求：

PRD(Product Requirement Document): 产品需求文档


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
<ul>
<li>link to Library or Profile content</li></li></li>

<li>use “search” to find their content</li></li>

<li>link directly to a folder</li>
</ul>
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
Disable click event

Do not change cursor from arrow to hand

Show tooltip on hover that reads “You do not have access to this content”

<li> Need to use the new “Highlight” option for any input that is selected  </li>
<ul>
<li>NOTE: This is a part of the new design system that changes the border color of the input when it is focused to make it clear to the user where they are in the UI. See Figma designs for more details
</ul>
 </ul>
