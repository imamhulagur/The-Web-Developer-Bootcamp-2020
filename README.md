# The-Web-Developer-Bootcamp-2020

Change Log 
https://www.notion.so/Web-Developer-Bootcamp-ChangeLog-45e3eab6be724c5f9a4b83c01044e126

##HTML basics

- HTML Boilerate - suggetions

- inline elements
    They will share space with other elements
    inline will adjust its space with other elements like anchor tag <a/>
- block elements
    They will not share space with other elements
    like h1, p, etc will take new line whole space
- DIV
    block level element
    generic container elements
- span
    inline element
    generic container
- special character in HTML - 
    starts with & and ends with ;
    using entity codes[https://dev.w3.org/html5/html-author/charref]

- semantic marksup
    instead of keeping all as DIV, use specilized tags
    If others are redenring through code its should to feasible(like which is nav, section, article, footer, header)
    they dont give extra features, same as div but helps in understanding code while rendered by other person.
    ex <main> <section> <article>

- Emmet VS tools : https://docs.emmet.io/
    main>section>h1
        <main>
            <section>
                <h1></h1>
            </section>
        </main>

    h1+h2+h3
        <h1></h1>
        <h2></h2>
        <h3></h3>

        
    div>h1+h2+div
        <div>
            <h1></h1>
            <h2></h2>
            <div></div>
        </div>


    Gnerate multiple tags at once : ul>li*5
            <ul>
                <li></li>
                <li></li>
                <li></li>
                <li></li>
                <li></li>
            </ul>

    numbering : use dollar $ symbol
    nav>ul>li*5>a
    <nav>
        <ul>
            <li><a href=""></a></li>
            <li><a href=""></a></li>
            <li><a href=""></a></li>
            <li><a href=""></a></li>
            <li><a href=""></a></li>
        </ul>
    </nav>

    nav>ul>li*5>a[href=$]
    <nav>
        <ul>
            <li><a href="1"></a></li>
            <li><a href="2"></a></li>
            <li><a href="3"></a></li>
            <li><a href="4"></a></li>
            <li><a href="5"></a></li>
        </ul>
    </nav>

<!-- text use {} braces -->
nav>ul>li*5>a[href=www.google$.com]{click me}
<nav>
    <ul>
        <li><a href="www.google1.com">click me</a></li>
        <li><a href="www.google2.com">click me</a></li>
        <li><a href="www.google3.com">click me</a></li>
        <li><a href="www.google4.com">click me</a></li>
        <li><a href="www.google5.com">click me</a></li>
    </ul>
</nav>

- Label
<!-- here the in[ut field id name should be same as for attribute of label, so that when you click on label the respective input field gets clicked --> 
<form action="">
    <!-- common way -->
    <label for="firstnasme">First name</label>
    <input type="firstname" id="firstname"><br/>
    <!-- Good way, No need to specify id here  -->
    <label>
        click me
        <input type="radio" id="click">
    </label>
</form>


-HTML button tag
    <button> : default when you click its will submit and redirect
    <button type="button"> simply acts a button instead submit button

-name attribute
    name is aka/alias name for value being entered/submitted inside input field
    we can query param etc
-Radio Buttons, Checkboxes, & Selects
    checkbox
        multiple selction is possible
    radio box
        single selction allowed
        slection i query param send it as - ? name=on
        name attribute of all radio button should be same
-Range & Text Area
    Range
    input type range
    min, max, step, etc
    Text Area
    <textarea>
    default rows-2, deault col-20.

-HTML5 Form Validations
    required,
    minlength and maxlenght for string inputs
    min and max for numeric inputs
    type - email, url with regex
whatever used after colon VS Code emmet will be consider it an type
    input:radio - <input type="radio">

CSS
selector {
    porp : value
}
-CSS styles
    inline
        using style attribute
        bad way
        if i have multiple elements with same style, need to duplicate same code
    internal
        using <style> tag inside <head>
        bad way
        id i want tp add same style foe elements which reside in different files, code duplication
    external style sheet
        good way
        using   <link rel="stylesheet" href-"location"> inside <head>

- Colors Systems:
    RGB - additve colors- we can egt any other color if we mix them.
        each channel go from 0 to 255
        rgb(0,0,0) is black 255 is
    HEX
        ranges from 0 to 255 but in hexadecimal
        #RRGGBB anges from 00 to ff
missig semicolon after property u wont fet error, even brower wont recognise it. But style wont apply.

- CSS selctors
    Universal - using *
        * {
            porp : value;
        }
    Elements - using element_name
    multiple elemnts at a time with comma seperated
    h1, h2 { coloe: gree;}

    ID  -  using #
        unique
        id="x"

    Class  - using dot(.)
        keyword in input field is class="x"

    Descendant
    li a { prop:value;} - apply to nested elements inside li

    Adjacent - using +
    h1 + p{ p:v;}

    Direct Descendant/direct child -  using >
    div > li {p:v;}

    Attribute -  using []

Psuedo classes
    Keywords added to selectors that sepcifies a special state of an elements
    ex :hover :active :checked :nth-of-type(n)

Psuedo elements
    Keywords added to selectors that lets you to style particular part of selected elements
    ex ::first-letter, ::first-line, ::selction, ::after, ::before

Conflicting styles
    same selector 
        cascading style order - first<second<external
        diff selector/Specificaity
            element select < element selector + elementselector(this seems more specific)
            ID > Class >Elements
            speicifity calculator - 3 digits - 1 0 0(if there is one ID

        Two things which ignores specificity are below
        Inline styles specificity
            Inline styles > ID > Class >Elements but forget about inline dont use it.
        !important - oveeride/super specific
            since it oveeride all other sryle never recomended to use. But depending on sitution you can use it.

CSS inheritance

BOX Model
    box sizing - making border box included with border width too.
    beter to use shorthand prop.
    In css everything is considered as BOX.
    padding - space between actual content and border.
    Margin - space between boxes/between elements.
    Display
        inline
            width and height are ignored
            margin and padding push elements away horizontally, not vertically.
        block
            block level elements beak the flow of the document
            width height, margin and padding are considered.
        inline-block(important property)
            Behaves like inline elments except its considers width height margin and padding.

CSS Units
    absolute
        px - 1px doesnt necesserally equal to width of exactly one pixel.
        Not recomended to use for responsive applications
        Rarely used - pt, cm, in, mm
    relative    
        %-sometimes value from parent or sometimes elements itself.

        em - 1em equal to the font size of parent.
        scale size base on parent elements size
        rems - root em - relative to html root elements.
        easy to work with since scaling is realtive to html root element.

Opacity and alpha channel
    alpha channel
        backgroung- color:rgba(0,0,0,0) - 0 to 1
        only applies to backgroung not to content
    Opacity
        opacity: vary from 0 to 1
        applies to contents also/entire element
position prop - absolute, relative, fixed, sticky.

transition

transform   -  rotate(), scale(), translate(),skew()

Resposive CSS & Flex model
    Flex box - 1D layout method for laying out item in rows and col.
    main axis - x, cross axix -Y
    disply:flex - adjust boxes
    flex-diretion: row, row-riverse, column, column-reverse
    justify-content - work with main axis or cross axis depending on flex-direction.
        :start,end,between,end,space-across, space-evenly, flex-wrap:wrap, reverse-wrap
    aleign-items - distributes spaces along the cross axis
        :flex-start,flex-end,center,flex-wrap,reverse-wrap
    aleign-content, aleigh-self
    flex-basis-without any unit/uses porpertion,flex-grow,flex-shrink
        shorthand-flex:grow,shrink,basis

Media queries - allow us to modify our style depending on particular parameters like screen width or device type.
    @media(diff param){
        selector {prop:val;}
    }
    diff paam- min-width,max-width

BOTSTRAP - go through docs
    every row in bootstrap devided into 12 units.
    form grid
        form-control, form-group, for-row etc
    Utilities
        margin, padding ex mt-2 - varies from 0 to 5 (t,b,l,r,x,y)
        Display, flex etc
























General
Ctrl+Shift+P, F1 Show Command Palette
Ctrl+P Quick Open, Go to File…
Ctrl+Shift+N New window/instance
Ctrl+Shift+W Close window/instance
Ctrl+, User Settings
Ctrl+K Ctrl+S Keyboard Shortcuts
Basic editing
Ctrl+X Cut line (empty selection)
Ctrl+C Copy line (empty selection)
Alt+ ↑ / ↓ Move line up/down
Shift+Alt + ↓ / ↑ Copy line up/down
Ctrl+Shift+K Delete line
Ctrl+Enter Insert line below
Ctrl+Shift+Enter Insert line above
Ctrl+Shift+\ Jump to matching bracket
Ctrl+] / [ Indent/outdent line
Home / End Go to beginning/end of line
Ctrl+Home Go to beginning of file
Ctrl+End Go to end of file
Ctrl+↑ / ↓ Scroll line up/down
Alt+PgUp / PgDn Scroll page up/down
Ctrl+Shift+[ Fold (collapse) region
Ctrl+Shift+] Unfold (uncollapse) region
Ctrl+K Ctrl+[ Fold (collapse) all subregions
Ctrl+K Ctrl+] Unfold (uncollapse) all subregions
Ctrl+K Ctrl+0 Fold (collapse) all regions
Ctrl+K Ctrl+J Unfold (uncollapse) all regions
Ctrl+K Ctrl+C Add line comment
Ctrl+K Ctrl+U Remove line comment
Ctrl+/ Toggle line comment
Shift+Alt+A Toggle block comment
Alt+Z Toggle word wrap
Navigation
Ctrl+T Show all Symbols
Ctrl+G Go to Line...
Ctrl+P Go to File...
Ctrl+Shift+O Go to Symbol...
Ctrl+Shift+M Show Problems panel
F8 Go to next error or warning
Shift+F8 Go to previous error or warning
Ctrl+Shift+Tab Navigate editor group history
Alt+ ← / → Go back / forward
Ctrl+M Toggle Tab moves focus
Search and replace
Ctrl+F Find
Ctrl+H Replace
F3 / Shift+F3 Find next/previous
Alt+Enter Select all occurences of Find match
Ctrl+D Add selection to next Find match
Ctrl+K Ctrl+D Move last selection to next Find match
Alt+C / R / W Toggle case-sensitive / regex / whole word
Multi-cursor and selection
Alt+Click Insert cursor
Ctrl+Alt+ ↑ / ↓ Insert cursor above / below
Ctrl+U Undo last cursor operation
Shift+Alt+I Insert cursor at end of each line selected
Ctrl+L Select current line
Ctrl+Shift+L Select all occurrences of current selection
Ctrl+F2 Select all occurrences of current word
Shift+Alt+→ Expand selection
Shift+Alt+← Shrink selection
Shift+Alt +
(drag mouse)
Column (box) selection
Ctrl+Shift+Alt
+ (arrow key)
Column (box) selection
Ctrl+Shift+Alt
+PgUp/PgDn
Column (box) selection page up/down
Rich languages editing
Ctrl+Space Trigger suggestion
Ctrl+Shift+Space Trigger parameter hints
Shift+Alt+F Format document
Ctrl+K Ctrl+F Format selection
F12 Go to Definition
Alt+F12 Peek Definition
Ctrl+K F12 Open Definition to the side
Ctrl+. Quick Fix
Shift+F12 Show References
F2 Rename Symbol
Ctrl+K Ctrl+X Trim trailing whitespace
Ctrl+K M Change file language
Editor management
Ctrl+F4, Ctrl+W Close editor
Ctrl+K F Close folder
Ctrl+\ Split editor
Ctrl+ 1 / 2 / 3 Focus into 1
st, 2nd or 3rd editor group
Ctrl+K Ctrl+ ←/→ Focus into previous/next editor group
Ctrl+Shift+PgUp / PgDn Move editor left/right
Ctrl+K ← / → Move active editor group
File management
Ctrl+N New File
Ctrl+O Open File...
Ctrl+S Save
Ctrl+Shift+S Save As...
Ctrl+K S Save All
Ctrl+F4 Close
Ctrl+K Ctrl+W Close All
Ctrl+Shift+T Reopen closed editor
Ctrl+K Enter Keep preview mode editor open
Ctrl+Tab Open next
Ctrl+Shift+Tab Open previous
Ctrl+K P Copy path of active file
Ctrl+K R Reveal active file in Explorer
Ctrl+K O Show active file in new window/instance
Display
F11 Toggle full screen
Shift+Alt+0 Toggle editor layout (horizontal/vertical)
Ctrl+ = / - Zoom in/out
Ctrl+B Toggle Sidebar visibility
Ctrl+Shift+E Show Explorer / Toggle focus
Ctrl+Shift+F Show Search
Ctrl+Shift+G Show Source Control
Ctrl+Shift+D Show Debug
Ctrl+Shift+X Show Extensions
Ctrl+Shift+H Replace in files
Ctrl+Shift+J Toggle Search details
Ctrl+Shift+U Show Output panel
Ctrl+Shift+V Open Markdown preview
Ctrl+K V Open Markdown preview to the side
Ctrl+K Z Zen Mode (Esc Esc to exit)
Debug
F9 Toggle breakpoint
F5 Start/Continue
Shift+F5 Stop
F11 / Shift+F11 Step into/out
F10 Step over
Ctrl+K Ctrl+I Show hover
Integrated terminal
Ctrl+` Show integrated terminal
Ctrl+Shift+` Create new terminal
Ctrl+C Copy selection
Ctrl+V Paste into active terminal
Ctrl+↑ / ↓ Scroll up/down
Shift+PgUp / PgDn Scroll page up/down
Ctrl+Home / End Scroll to top/bottom
Keyboard shortcuts for Windows
Other operating systems’ keyboard shortcuts and additional
unassigned shortcuts available at aka.ms/vscodekeybindings