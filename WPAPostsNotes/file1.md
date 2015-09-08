#Notes from WordPress Accessibilty Team Blog Posts
##Make WordPress Accessible dated 7 September 2015
###Location of actual blog post.  <a href="http://make.wordpress.org/accessibility/2015/09/07/accessibility-usertest-select2/">Accessibility Usertest: Select2</a>This is the original source of information.  What follows is copied content for personal review and a record for developing accessible JQuery
###Location of file on JQuery replacement for select boxes <a href="https://select2.github.io/">Select2 is a jQuery replacement for select boxes </a>
###Location of issues on GitHub <a href="https://github.com/select2/select2/search?q=accessibility&state=open&type=Issues&utf8=✓">Issues</a>
####Content from 7 Sept 2015 MWA Blog follows
Test results

1. Basic dropdown

Geof Collis: JAWS 14.5 IE 11.
 Not accessible. I tried to open the box but just got dead air and I found the edit field down the page but was confused on what to do so typed in the letter a and arrowed down to get a list of states only to realize that if I arrowed up and down I got the list I expected in the drop down box.

Bart Simons: JAWS15 and IE11,  JAWS15 and Firefox, JAWS16 and IE11, JAWS16 and Firefox
 JAWS says "combo box collapsed".
 I press enter to go to forms mode.
 Since I am told that this is a combobox I try using arrow down to scroll through the list. This does nothing. I can't go beyond Alaska. Also arrows up, left and right do nothing.
 Then I try to navigate by typing the first letter. This does not work either.

The test suggestions suggest to use space bar. This is something I would never have tried by myself.
 After pressing space bar, I am told that I am in an edit box. I type "new" and I hear "New Mexico". Again there is no possibility to use down arrow to go to New York for instance.
 Even New Mexico does not seem to be selected.

Besides, it is really not intuitive to require a space bar in a combo box.

Gabriela Nino de Rivera Torres: VoiceOver+Safari.
 The combo box does not respond to Control+Option+Space bar VoiceOver command to open the list of choices. It does respond to the space bar only.

When the list of choices it's open, the first element getting the focus is the link to go back to the list of examples. The second element is the search field text and lastly the table with the choices. I'm using Control-Option+right arrow to navigate inside the combo box element.

The texts for Time zone are ignored by VoiceOver.

VoiceOver offers me to navigate the table with the choices using Control-Option-right/left arrow or up/down arrow. Both commands worked fine.

There seems to be something different with the choice Hawaii. There is an intermittent behaviour that requires me to use the Control-Option-right/down arrow command several times before moving to California. It seems like the focus gets stuck on Hawaii choice for some reason.

It is not possible to move inside the list of choices using only up/down arrows.

Using only the Enter key will open/close the combo box choices. In this case the first element getting the focus is the search field text. When making a search, the user does not get feedback if the state that she is looking for it is found or not on the list of choices.

I could not find how to select an option of the list of choices. Normally I'll use Control+Option+Space bar command, but I don't get a response. Using Control+Option+Enter does not work either. Using only the Enter key will close the list without selecting the current choice (the one with the focus on it). But if I search for the state and click on Enter, the list will close but the current choice will be selected.

Michelle DeYoung: Windows 8.1 / FF 40.0.3 / NVDA 2015.2
 Keyboard only: Works fine.

FF/NVDA:
 Forms mode -  The state name is announced. This is considered the label via the aria-labelledby.  The label should be the ‘Select a US state”.
The text input in the expanded list is not labelled.
 Virtual mode – Can arrow through the items in the combobox, but all that is voiced by NVDA is “blank”.
Note: Can expand and collapse the list.

2. Multiple select boxes

Geof Collis: JAWS 14.5 IE 11.
 Not accessible. Entered the box but heard nothing.

Gabriela Nino de Rivera Torres: VoiceOver+Safari.

The combo box does not respond to Control+Option+Space bar VoiceOver command to open the list of choices. It does respond to the space bar only.

Using only the Enter key will open/close the combo box choices. In this case the first element getting the focus is the search field text. The second element getting the focus is the link to go back to the list of examples and lastly the table of choices.

VoiceOver offers me to navigate the table with the choices using Control-Option-right/left arrow or up/down arrow. Both commands worked fine.

I could not find how to select a choice directly from the list of choices. Control+Option+Space bar command does not work. Using only the Enter key will send me to the instructions page. But if I search for the state, I'm able to select it using the Enter key after entering the word (although I don't get any feedback to confirm me if the state I'm looking for was found or not).

I could not found how to remove a choice. Any of the common VoiceOver commands don't work to get focus on the selected choices.

Michelle DeYoung: Windows 8.1 / FF 40.0.3 / NVDA 2015.2
 Keyboard only:
•No visual indicator that it is a select box and offers choices.
•Yes, selections can be accessed and added.
•Yes, can remove selections by using the ‘Backspace’. Selection will be removed a letter at a time.

FF/NVDA:
 Combobox is missing a label. NVDA does announce that it is a combobox.
 List is announced that it is expanded, but the as user arrows through the list the items are announced as “blank”.

If user randomly selects and item (they will not know what they selected), the items are added to the input field, but they are not announced.
 Unable to access added items in the input to have them announced.  If I assume items exist in that form field, then I can select “Backspace” to remove them a letter at a time.
Note: Unable to type a selection name in the input field. 
3. Placeholders

Geof Collis: JAWS 14.5 IE 11.
 Semi accessible. I expected that I would hear the placeholder before going into forms mode but had to enter the field before I did.

Gabriela Nino de Rivera Torres: VoiceOver+Safari.
 No, VoiceOver did not announce the placeholder inside the first option. The combo box does not respond to Control+Option+Space bar VoiceOver command to open the list of choices. It does respond to the space bar and Enter key.

Michelle DeYoung: Windows 8.1 / FF 40.0.3 / NVDA 2015.2
 FF/NVDA: Yes, Placeholder is announced. (No labels for input fields)

4. Disabled mode

Geof Collis: JAWS 14.5 IE 11.
 Semi accessible. I expected a checkbox for the modes but realized to click on the button and it worked but I'm starting to wonder if I should be reading 2 drop down menus because that is what I am getting in all examples so far.

Gabriela Nino de Rivera Torres: VoiceOver+Safari.
 I was able to enable and disable the two select boxes. It does work with Control-Option-espace bar and with the Enter key.

Michelle DeYoung: Windows 8.1 / FF 40.0.3 / NVDA 2015.2
 Keyboard only: Yes, Enable/Disable buttons work

FF/NVDA:
•No labels.
•Yes, Enable/Disable buttons work.
•Tabbing backwards through the inputs after ‘Disable’ has been selected skips over the inputs initially, but if user continues one more tab backwards the 2nd input will be announced, “Combobox collapsed has autocomplete”.

5. Disabled results

Geof Collis: JAWS 14.5 IE 11.
 Not accessible. Sometimes it reads first and other times it doesn't it isn't consistent and I only get one box. Used the back button and it froze my browser and had to close it down, grrr!

Gabriela Nino de Rivera Torres: VoiceOver+Safari.
 I'm not able to move from the first option. I'm using Control-Option-right arrow to navigate between the options on the table. Using only right/left/up/down arrow to move from one option to the other won't work.

If I interact with the table choices (Control-Option-shift-down arrow) I'm able to move to the second option and it will be announced by VoiceOver. From the second option it is impossible to move to the third option.

Michelle DeYoung: Windows 8.1 / FF 40.0.3 / NVDA 2015.2
 Keyboard only:
•No labels for inputs.
•Yes, disabled item is skipped over when arrowing.

FF/NVDA:
•List items are announced as “blank”.
•Yes, disabled item is skipped over when arrowing.

6. Select with a button

Geof Collis: JAWS 14.5 IE 11.
 Semi accessible. But I find all of these boxes confusing and verbose so I'm quitting, I dont like it in the least, time to go back to the drawing board. :O)

Gabriela Nino de Rivera Torres: VoiceOver+Safari.
 Yes I can set the option in the select drop using the two buttons for each example. In both examples, VoiceOver does not give feedback after the setting function. I'm able to press the buttons using Control-Option-space bar, only the space bar key and the Enter key.

Also it is possible to open/close the select choices using Control-Option-space bar, only the space bar key and the Enter key. I think those two examples are easiest to use with VoiceOver.

Michelle DeYoung: Windows 8.1 / FF 40.0.3 / NVDA 2015.2
 Keyboard only:
•1st Example: ‘Set’ & ‘Init’ work, but the others do not.
•2nd Example: Yes, it works.

FF/NVDA:
•1st Example: ‘Set’ & ‘Init’ work, but the others do not.
•2nd Example: Yes, it works.   Note: Selected items are not announced in the input field they are added to.

7. Limiting the number of selections

Gabriela Nino de Rivera Torres: VoiceOver+Safari.
 I was not able to select any of the choices. Once in the table choices I tried selecting with the Enter key (it sent me back to the instructions page), using space bar key only and Control-Option-espace bar did not work either.

The combo box does not respond to Control+Option+Space bar VoiceOver command to open the list of choices. It does respond to the space bar key and the Enter key.

Michelle DeYoung: Windows 8.1 / FF 40.0.3 / NVDA 2015.2
 Keyboard only: Yes, it works.

FF/NVDA:
•Yes, can only select two items.
•No, the feedback is not announced.
•No, the item choices are not announced.
•No, selected items are not announced.

8. Hiding the search box

Gabriela Nino de Rivera Torres: VoiceOver+Safari.
 The search box it is very well hidden, VoiceOver did not notice it.

Michelle DeYoung: Windows 8.1 / FF 40.0.3 / NVDA 2015.2
 Keyboard only: Yes, it works.
 FF/NVDA: Yes, Search box is hidden and not voiced by screen reader.

9. Add choices automatically

Gabriela Nino de Rivera Torres: VoiceOver+Safari.
 I was able to add choices using the coma and the space. The combo box does not respond to Control+Option+Space bar VoiceOver command to open the list of choices. It does respond to the space bar key and the Enter key.

Michelle DeYoung: Windows 8.1 / FF 40.0.3 / NVDA 2015.2
 Keyboard only: Yes, it works.
 Note:
Using space – Cannot add more than two rows of items.
Using comma – Cannot fill past one row of items.

FF/NVDA:
 Yes, can add items with space or comma, and they will appear in the list.
 If too many items are added to the list they are dynamically removed except for the first item.
 >Note:
Using space – Cannot add more than two rows of items, but NVDA will still voice like items are being added.
Using comma – Cannot fill past one row of items, but NVDA will still voice like items are being added.
 Items – Items in list are announced as “blank”.  Items added to the input are also not announced.

Notes from @bramd

I had a quick look at Select 2 using Firefox + latest NVDA nightly build.

The Select 2 widget is announced as combo box, however it doesn’t respect the common keyboard navigation conventions on Windows. I expect to be able to use the arrow keys to select an item when the select box is in closed state, that doesn’t work. The alt+down arrow hotkey, which is the default to open a dropdown in Windows, works. However, when the select box is open, the active item is not announced by a screenreader. I can select an option by pressing enter and after closing the box the selected item is readable.

Conclusions: It seems that some aria support has been implemented. This causes a screenreader to pick up the role (select box) and the state (open/closed).
 However, much more work is needed to support the focus in an open Select 2 widget. All the special Select 2 features such as grouping items and typing to filter/search the list has not been tested, but this also needs additional aria markup to be read by screenreaders.

Another issue is the expected keyboard shortcuts. These are different on every platform and Select 2 should feel native on all of these platforms, so this has to be implemented and tested prety well. E.g. on Windows I don’t expect a dropdown to open when I press space bar, but on Mac this is the common way to open such an element.

Notes on the test results by @afrecia
•Difficult to understand how to open the combo box. Users expect to open the combo box using just the down arrow key. Previous version worked that way.
•Missing label for the input field (The text input in the expanded list is not labelled). It gets announced with the name of the first option, e.g.: "Alaska  combo box  collapsed  has auto complete". Investigate on current usage of "aria-labelledby".
• Searching: ◦leaving the field empty, it is possible to arrow through the items in the list but every option gets announced as "blank"
◦entering some charavters e.g. "mi" and arrowing through the results e.g. "Minnesota", "Mississippi", "Missouri" will read out just "mi" which is the entered value in the input
◦no feedback about how many search results - the previous version announced "5 results are available, use up and down arrow keys to navigate" or "No matches found".

•"I could not find how to select an option of the list of choices". I guess that's because all you hear is "blank" or the characters you entered in the search field.
•No feedback when selecting an item: If user randomly selects and item (they will not know what they selected), the items are added to the input field, but they are not announced.
•Multiple select boxes: "Unable to access added items in the input to have them announced.  If I assume items exist in that form field, then I can select “Backspace” to remove them a letter at a time."Once you've added options, they're not announced so users really have to guess they're in the input field.


Conclusion

The main problems are:
•There is no or not enough feedback for screen readers on what is selected or what can be selected (list items are announced as “blank”.)
•No feedback about how many search results.
•The select dropdown does not behave like a user expects, quoting Bart: "It is really not intuitive to require a space bar in a combo box.This is something I would never have tried by myself"
•Select2 has at the moment too many accessibility issues to be included into WordPress core
