/**
  * Sample sahi commands and documentation. Still
  * needs documentation for html tag, table, form, etc. 
  * accessor methods as found at http://sahi.co.in/w/browser-accessor-apis
  * 
  * @author Fleming Slone
  * @see http://sahi.co.in/w/browser-action-apis
  * @see http://sahi.co.in/w/sahi-scripting-basics
  * @see http://sahi.co.in/w/browser-accessor-apis
  * @see http://sahi.co.in/w/sahi-script-and-javascript
  * @see http://sahi.co.in/w/sahi
  * @see http://sahi.co.in/w/sahi-api-examples 
  *
*/


/** Sample browser API calls */
_assert(condition, message);
_assertContainsText(expectedText, object, message);
_assertEqual(expected, actual, message);
_assertEqualArrays(expected, actual, message);
_assertExists(object, message);
_assertFalse(condition, message);
_assertNotContainsText(expectedText, object, message);
_assertNotEqual(expected, actual, message);
_assertNotExists(object, message);
_assertNotNull(object, message);
_assertNotTrue(condition, message);
_assertNull(object, message);
_assertTrue(condition, message);
_blur(element);
_check(checkBoxOrRadioElement);
_click(_link("Login"));
_closeBrowser();
_closeWindow();
_collect(apiType, id, inEl);
_count(apiType, id, inEl);
_createCookie(name, value, days);
_deleteCookie(name);
_doubleClick(element, combo);
_dragDrop(elementToDrag, elementToDropOn);
_dragDropXY(elementToDrag, x, y[, isRelative]);
_focus(element);
_keyDown(element, charInfo, combo);
_keyPress(element, charInfo, combo);
_keyUp(element, charInfo, combo);
_log(message, logLevel);
_mouseDown(element, isRight, combo);
_mouseOver(element, combo);
_mouseUp(element, isRight, combo);
_navigateTo(url, forceReload);
_openBrowser();
_removeFocus(element);
_rightClick(element, combo);
_rteWrite(iframe, text);
_setFile(element, filePath);
_setSelected(element, option_identifier, isMultiple);
_setValue(element, text);
_setValue(_password("password"), $pwd);
_setValue(_textbox("username"), $usr);
_type(element, text);
_uncheck(checkBoxElement);
_wait(timeInMilliseconds, condition);

/** if statement */
if ($username == "PartnerUser"){
  _click(_link("Partner Login"));
}


/** for statement */
for (var $i=0; $i<$max; $i++){
  // statements
}


/** This loop will login with user1, password1, user2, password2 etc.
  * login and logout are custom functions.
  *
*/
for (var $i=0; $i<10; $i++){
  login("user"+$i, "password"+$i);
  logout();
}


/** example while loop */
$i = 0;
while ($i++ < 10) {
  login("user"+$i, "password"+$i);
  logout();
}


/** sample file include */
_include("includes/common_functions.sah");


/** Using index in the page; assuming it is the 13th link on the page.
  * Using indexes works fine as long as the page is static, but it is 
  * not recommended for dynamic applications, as it makes scripts fail 
  * when changes are made to the web pages.
*/
_link(12);


/** Using id as string */
_link("sahi_link");


/** Using id as regular expression */
_link(/.*_link/);


/** Using visible text as string */
_link("Link to Sahi website");


/** Using visible text as regular expression */
_link(/Link to .* website/);


/** Using visible text as regular expression */
_link("/Link to .* website/");	


/** Using an associative array with id */
_link({id:"sahi_link"});	


/** Using an associative array with visible text as regular expression */
_link({sahiText:"/Link to .*/"});	


/** Using an associative array with multiple attributes like className and sahiText */
_link({className:"low",sahiText:"/Link.*/"});	


/** When elements are not uniquely identifiable by themselves, we should try to 
  * identify them in relation to the DOM.
  * _near is a DOM relation marker which specifies that the element should be 
  * searched near another element. 
  * _in is a DOM relation marker which specifies that the element should be 
  * searched within another element.
*/


/** example points to the 0th link near cell with text “User Two”.
  * Note that the index is 0 here since it is the nearest link.
*/
_link(0, _near(_cell("User Two")));


/** points to the nearest link with text “delete” near cell with text “User Two”.
  * Note that we do not need to specify "delete[1]" since it is the delete.
  * link nearest to User Two.  
*/
_link("delete", _near(_cell("User Two")));

/** points to the nearest link with text which matches
  * regular expression /del/ near cell with text “User Two”. 
*/
_link(/del/, _near(_cell("User Two")));


/** points to the 3rd nearest link with text “delete” near 
  * cell with text “User Two”. 
*/
_link("delete[2]", _near(_cell("User Two")));


/** points to the 3rd nearest link with text matching /del/ near cell with text “User Two”.
  * Note how the regular expression is appended with the index in square brackets
  * and quoted to make it a string 
*/
_link("/del/[2]", _near(_cell("User Two")));

/** 
  * points to the 0th link in cell with id “del2”
*/
_link(0, _in(_cell("del2")));


/** 
  * points to the link with text “delete” within cell with id “del2”
*/
_link("delete", _in(_cell("del2")));


/** 
  * _under is a Positional Relation which helps narrow down elements under another element. 
  * Specifically it looks for elements which have the same left offset (within a threshold) 
  * as the anchoring element.
*/


/** Finds first cell near User One and under Status */
_cell(0, _near(_cell("User One")), _under(_cell("Status")));


/** Finds first Inactive cell under Status */
_cell("Inactive", _under(_cell("Status")));


/** 
  * If we want to verify the cost of a Ruby for Rails book in a table with a column called 
  * "cost" we would to first look at that cell which is in the “Ruby for Rails” row and 
  * then under the “Cost” column to determine the cost value
*/
_cell(0, _near(_cell("Ruby for Rails")), _under(_cell("Cost")));


/** 
  * Another way is to find the table accessor, and then use it with some unique text 
  * contained within a row and then by unique text within the column.
*/
_cell(_table("listing"), "Ruby for Rails", "Cost");


/** 
  * If we wanted to access the checkbox under the "Recommended" column of the table 
  * within the "Ruby on Rails" row...
*/
_checkbox(0, _near(_cell("Ruby for Rails")), _under(_cell("Recommend")));



