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

- semantic markups
    instead of keeping all as DIV, use specialized tags
    If others are rendering through code its should to feasible(like which is nav, section, article, footer, header)
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



JAVASCRIPT
string functions
    trim - trims the empty spaces before anf after the string
    ${} - its a literal used in JS to insert and evaluate expression and the convert them into string again.
    while comp string its based on their unicode numbers
    Always out the <script></script> at the end i.e before closing body tag, because HTML elements need to be load before working running jd scripts
    push and pop for end, shift and un-shift are related to beginning
    shift - removes and returns first ele
    un-shift - adds new element at first place
    JS return -1 if it does not contains element.
Array methods
    Concat/indexOf/includes/reverse - done
    Slice/Splice
        Slice(startIndex, endIndex) - delete from start to end
        Splice(startIndex, deleteCount, 'optionalInsert');
    sort - irs will convert all array value into its UTF-16 value and the sort according to it. Its quite confusing.
Array comparision
    JS doesnt care about the whats inside of array, its only compares array references in memory.
    hence [] === [], ['hi] === ['hi'], ['hi']==['hi'] returns false
    const arr[] = [1,2,3] - we can change the content but we cant change ref name
Object literals
    every key in JS object converted down to string even though we have integer
    while access values of object using [] operator we need to provide key name within quotes
        ex Info["firstname]
    accessing using dot(.) operator directly using key value ex: Info.firstname

JS loops
    for,while, for..of, for..in
    *for(let some of something) - is used to iterate array elements
    *for(let some in something)  - is used to iterate object values

JS Functions
    Return key stops the execution of a function, the stmts after return ll not be executed.

JD variable scope/visibility
    Functional scope
        variable declared inside any function is only available to access inside it
        otherwise we will get 'undefined error'
    Block scope - conditional stmts, loops.
        let and const keyword in ES6/ECMA2015 because of this block scope.
        before that only one keyword i.e always function scoped.
    *lexical scope
    function outer() {
        let msg="fromOuter";
        function inner() {
            console.log(msg);
        }
    }
    case 1 : outer.inner() //u will get error here since you are calling inner function from outside out outer function scope
    case 2 : if you call inner function from inside of outer function scope, due to "lexical scope" the variable msg is available to inner() also.
    Note : if something exist in outer its by default available to inner but not vice versa

Function expressions / returning function as a variable
    Storing an anonymous function inside a variable. 
    The anonymous function body is treated as a expression and gets evaluated.
    The final calculated value returned by function evaluation is gets stored inside a variable.
    ex:
    let sum = function(x, y){
        return x+y;
    }

Higher Order function - function that work with other functions
    Accept a function as argument
    function callTwice(func) {
        func();
        func();
    }

    function diceRoll() {
        return math.floor((math.radom()*6)+1);
    }

    callTwice(diceRol());

    Returning function

    function surpriseFunction(){
        let randNum = (math.floor(math.random())); //its will return value between 0 and 1
        if(randNum > 0.5) {
            return function(){
                console.log("happy");
            }
        }
        else {
            return function(){
                console.log("sad");
            }
        }
    }


JS methods
    methods  = functions as properties on objects
    ex:
    let myInfo = {
        FirstName : function() {
            return "imam";
        }
        LastName : function() {
            return "hulagur";
        }
    };
    accessing FirstName-> myInfo.FistName()
    Here myInfo is method variable, FirstName and LastName as functions as properties
    *Every method is function, but not vice versa.

    Now we can write as below also to avoid confusion(Remove function keyword, by default it wil take it as function only )
    
    Better way 
    let myInfo = {
        FirstName() {
            return "imam";
        }
        LastName() {
            return "hulagur";
        }
    };
    ex: 
    let square = {
        area(side) {
            return side*side;
        },
        perimeter(side) {
            return side*4;
        }
    };
JS this keyword in method
    The value of this id depends on the context where is user/invoked.
    let myInfo = {
        firstName: "imam",
        lastName:"hulagur",
        info() {
            //console.log("THIS IS:", this); pointing to window object
            console.log("Hey my first name is:" + this.firstName);
        }
    };
    case 1: 
    myInfo.info(); //you will get correct o/p since this is represent the object myInfo which used left side access it.
    case :2 if you male copy of that function to other variable, try to call it. 
    It will give an error, because that 'this' is pointing to 'window object in which its doesnt contains firstname property.
    let iInfo = myInfo.info; // undefined. we can test by just printing that 'this' keyword into the console

Try/Catch
    To avoid breaking of code
    try{
        //somtehing
    } catch(e){
        //something
    }

Callback and Array methods
1.forEach()
    older way
        let nums = [1,2,3,4,5,6,7,8,9];
        function print(num) {
            console.log(num); 
        }
        nums.forEach(print);

    modern way - anonymous function callbacks
        let nums = [1,2,3,4,5,6,7,8,9];
        nums.forEach(function(num){
            console.log(num);
        })
2.Map - creates new array with a result of calling callback function on every element in the array
    - extracting another array with require only data from array.
    let imams=['imam1','imam2','imam3','imam4','imam5'];
    let capsImams = imams.map(function(el){
        console.log(el.toUpperCase());
    });
    o/p : new array ->capsImams['IMAM1','IMAM2','IMAM3','IMAM4','IMAM5']

3.Arrow functions/fat arrow/'=>'
    syntactically compact function expression
        let add = function(x,y){

        }
        let add = (x,y)=> {

        }
    ex
        let greet = (el)=>{
            return `Hey ${el}!`;
        };
        greet('imam'); //o/p -> Hey imam!

    If there is only one expression can be evaluated
    *Implicit return - just remove those function curly braces i.e {} and also 'return' and ';' !!!
        let greet = (el)=>(
            `Hey ${el}!`
        );
    //regular function expression
    const isEven = function(num) {
        return num%2 === 0;
    }
    //arrow function with round brackets
    const isEven = (num) => {
        return num%2 === 0;
    }
    //arrow function without round brackets
    const isEven = num => {
        return num%2 === 0;
    }
    //Implicit arrow function without round brackets
    const isEven = num => num%2 === 0;
4.setTimeout() and setInterval() functions
    setTimeout:
    console.log('Hello..')
    setTimeout(()=>{
        console.log("Are you there");
    }, 3000)            //3000 ms, hence first God bye will print
    console.log('Good bye');

    setInterval and clearInterval(id)
    clearId  = setInterval(()=>{
        console.log("i will come again after 3 sec");
    }, 3000) 
    clearInterval(id);

5.filter method -creates a new array with all the elements that passes the test provided by the implemented function
    let nums = [1,2,3,4,5,6,7,8,9];
    let odd = nums.filter((el)=>{
                    return el%2 !== 0; //here the implemented function return true if number is odd
                })
    let even = nums.filter((el)=>{
                    return el%2 === 0; //here the implemented function return true if number is even
                })
    
6.some() function - its return boolean true value if condition passed
    let colors = ['red','green','blue'];
    colors.some((el)=>{
        return el.length <= 3;
    });

7.every() function - returns boolean true only if each and every elements of array satisfies the condition
    let colors = ['red','green','blue'];
    colors.every((el)=>{
        return el.length <= 3;
    });

ex: some and every function
    let allEvens = [2,4,6,8];
    allEvens.every((el)=>{
        return el%2 === 0;
    });
    true
    let allEvens = [2,4,6,8];
    allEvens.some((el)=>{
        return el%2 === 0;
    });
    true
    let allEvens = [1,2,4,6,8];
    allEvens.some((el)=>{
        return el%2 === 0;
    });
    true
    let allEvens = [1,2,4,6,8];
    allEvens.every((el)=>{
        return el%2 === 0;
    });
    false

8.reduce - execute a regular function on each element of a array, resulting in a single.
    -helps to find a single value i.e total, min, max in array elements
    -second argument to reduce(1st, 2nd) will be the initializer
    ex : 
    To find total
        let prices = [10, 5, 20.5, 35];
        prices.reduce((total, curPrice){
            return total + curPrice;
        })
    To find max and min values
        let prices = [10, 5, 20.5, 35];
        let max= prices.reduce((highest, curPrice)=>{
            if(highest > curPrice) return highest;
            else return curPrice;
        });
        o/p
        max
        35

        let prices = [10, 5, 20.5, 35];
        let max= prices.reduce((highest, curPrice)=>{
            if(highest < curPrice) return highest;
            else return curPrice;
        });
        o/p
        main
        5
Arrow function and this keyword
    *in a traditional function definition 'this' keyword always point to 'object' hence we can easily access properties of that function.
    let person = {
        firstName : 'imam',
        lastName : 'hulagur',
        fullName: function(){
            console.log(this);
            console.log(`My name is: ${this.firstName} ${this.lastName}`);
        }
    };
     o/p : My name is: imam hulagur

    *in a arrow function definition 'this' keyword always point to 'window' hence accessing properties of that object give us an error.

    let person = {
        firstName : 'imam',
        lastName : 'hulagur',
        fullName: ()=>{
            console.log(this);
            console.log(`My name is: ${this.firstName} ${this.lastName}`);
        }
    };
    o/p : My name is: undefined undefined

    *imp If the arrow function defined inside tradition function, the i will not an error
    let person = {
        firstName : 'imam',
        lastName : 'hulagur',
        fullName: function(){
            setTimeout(()=>{
                console.log(this);
                console.log(`My name is: ${this.firstName} ${this.lastName}`);
            }, 3000)
        }
    };
    o/p : after 3 sec -> My name is: imam hulagur

    Note : its always better to use arrow functions inside traditional function methods.

New features of JS
    1.default parameters
        -its an parameter where the optional parameter value would be initialized
        -the parameter should be initialized at the end
        ex: without default params
            function greetPerson(greeting, personName){
                console.log(`Hey ${personName} ${greeting}!`);
            }
            greetPerson("morning", "imam") 
            o/p  Hey imam morning
        ex: with default params - *the default param should be placed in the end, if placed before you will get undefined.
            function greetPerson(personName, greeting="Nice to meet you!"){
                console.log(`Hey ${personName}, ${greeting}`);
            }
            greetPerson("imam") 
        o/p  Hey imam, Nice to meet you!

    2.spread function[In java its var-arg method]
        -Its will take zero or more arguments(functions)/key-values pairs(objects)
        -it will spread the array into its individual arguments which are separated by spaces
        -spread in function calls
        ex: console.log('hello'); // hello
            console.log(...'hello'); // h e l l o
            let nums = [1,2,3,4,5,6,7,8,9];
            Math.max(...nums); //9
        -spread with array literals - copy one array to another
            let nums = [1,2,3,4,5,6,7,8,9];
            Math.min(...nums); //1
            -spread in array literals
            let cats = ['cat1', 'cat2'];
            let dogs = ['dog1', 'dog2', 'dog3'];
            let allPets = [...cats, ...dogs, 'newcat'];
            //cat1 cate2 dog1 dog2 dog3 newcat

        -spread with object literals - copy one object into other
            let user = {
                firstName : "imam",
                lastName : "hulagur"
            }
            let newUser = {...user, id:12}//retain old user info and add an additional fields
            let newUser = {
                firstName : "imam",
                lastName: "hulagur",
                id=12
            }
        -REST function (...)  - its not spreading things out its collecting thing in
            function sums(..nums){
                console.log(nums);
            }
            i/p - sum(1,2,3) -> 1,2 3
            sum(1,2) - >1,2

    3.destructuring arrays - unpacking array elements in variable cleanly
        let nums = [1,2,3,4,5,6,7,8,9];
        let [one, two] = nums;//we are not changing nums array, but we creating new variables one and two which holds respective values.
        o/p 
        nums
        (9) [1, 2, 3, 4, 5, 6, 7, 8, 9]
        one
        1
        two
        2
    destructuring objects - unpacking objects elements in variable cleanly
        let person = {
            firstName:"imam",
            lastName:"hulagur"
            age:24
        }
    //if i just want firstName and lastName variable from the object person
        let {firstName, lastName } = person;
        o/p 
        person
        {firstName: "imam", lastName: "hulagur", age: 24}
        firstName
        "imam"
        lastName
        "hulagur"
    //if i just want override the properties of the origin name object
        let {firstName: first, lastName:last } = person;

    Destructuring params

    let function fullName() {
        lets{firstName, lastName} = person;
        console.log(`${firstName} ${lastName}`);
    }

DOM World - Document Object Model
    -The JS representation of a webpage
    -its makes bunch of object to interact each other via JS
    -it combines HTML CSS JS
    -HTML, CSS Go in... JS object come out..
    selection
        window,document, console.dir('element');
        document.getElementById('#el');
        document.getElementsByTagName('.el'); document.getElementsByClassName('el'); - return HTML collections
    *we can replace above tags using below queryselector tags
        querySelector('#el') or querySelector('.el') or querySelector('el[some=something]')- >only return the first matching element
        querySelectorAll('#el') or querySelectorAll('.el') or querySelectorAll('el[some=something]')- >return Node List
        querySelectorAll('el')
    
    Updating content
    -innerText - print content without retaining spaces
        shows content at the moment i.e if display none i will not show that content.
    -textContent - retains format with spaces
        irrespective of Display prop i ll show everything.
    -innerHTML -  we can set content using HTML script, i will sanitize the script and provide content. 

    Important properties
        innerText
        textContent
        innerHTML
        value
        parentElement
        children
        nextSibling
        previousSibling
        style -> wiered thing is that style object doesnt consists of applies style, its empty.
            it ony track internal styling.
            imp* the property values of style object doesnt contains hyphen(-) i.e instead it cotain in camelCase
                ex : font-size - >you can find using fortSize
                    document.getElementsByTagName('h1').style.fontColor = "green"

    Important methods
        classList
        getAttribute()
        setAttribute()
        appendChilde()
        append()
        prepend()
        removeChild()
        remove()
        createElement
    classList - to apply multiple styles a time
    methods - add(), remove(), toggle(), contains()
    ex : let h1 = document.getElementsByTagName('h1');
          h1.classList.add('purple');
          h1.classList.add('border');
    ex: document.querySelectorAll('li');
        let lis = document.querySelectorAll('li');
        for(let li of lis){
            li.classList.toggle('highlight');
            }

    Traversing
    To parent element
        cur = document.querySelector('el');
        cur.parentElement;
    To child 
        cur.children[i];
    To directly access prev or next ele/nodes
        cur.nextSibling
        cur.nextElementSibling
        cur.previousSibling
        cur.prevElementSibling

    create new element and append
        newEle = document.createElement(p);//<p></p>
        newEle = "hello!";//<p>Helo</p>
    case 1 : oldEle.document.body.appendChild(p); 
    case 2 : body.append(newEle) or body.prepend(newEle)

    adding Adjacent elements
        -using function
        oldEle.insertAdjacentElement('where', what);
        where  - beforenegin,afterbegin,beforend,afterend.
        what - newEle

    Removing elements
        remove() & removeChild()
        ele.parentElement.removeChild(ele);
        ele.remove();

DOM events
    onclick
    addEventListener
    events and this keyword
        HTML -> button*{button clicked} and h1*5{header clicked}
        JS
        buttons = document.querySelectorAll('button');
        for(let button of buttons){
            button.addEventListener('click',() =>{
                console.log('button clicked');
            })
        }

        h1s = document.querySelectorAll('h1');
        for(let h1 of h1s){
            h1.addEventListener('click',() =>{
                console.log('header clicked');
            })
        }

    By using this we can reduce it as below, bcz this refers to clicked element
        buttons = document.querySelectorAll('button');
        for(let button of buttons){
            console.log(this);
            this.addEventListener('click', clickListener)
        }

        h1s = document.querySelectorAll('h1');
        for(let h1 of h1s){
            console.log(this);
            this.addEventListener('click', clickListener)
        }

        function clickListener() {
            console.log(this);
            this.style.backgroundColor = rgb(122,112,222);
        }

    Keyboard events and event object analysis
        const input = document.querySelector('input');
        input.addEventListener('keyup',function() {
            console.log('KEYUP!');
        })

        input.addEventListener('keydown',function() {
            console.log('KEYDOWN!');
        })
    Form event and prevent default
        const form = document.querySelector('form');
        form.addEventListener('submit',function(e){
            e.preventDefault();
            let productInput = form.elements.product;
            let quantityInput = form.elements.qty;
            createLi(productInput,quantityInput);
            productInput.value="";
            quantityInput.value="";
        })

        function createLi(productInput, quantityInput) {
            let ul = document.querySelector('ul');
            let li = document.createElement('li');
            li.append(`${quantityInput.value} ${productInput.value}`);
            ul.appendChild(li);
        }

    input and change events
        let input = document.querySelector('input');
        input.addEventListener('input',function() {
            console.log('each character entered);
        })    
        input.addEventListener('change',function() {
            console.log('when you click outside);
        })

    Event bubbling and e.stopPropagation()
        <section onclick="alert('section clicked')">section here
            <p onclick="alert('paragraph clicked')">paragraph here
                <button onclick="alert('button clicked')">button here</button>
            </p>
        </section>
    The event bubbles from child to parent element
    to avoid this we can you e.stopPropagation()

    Event Delegation / to check whether the listiening event on crct element or not

    HTML
    <body>
        <input type="enter name">
        <button>submit</button>
        <ul>
            <li>initial li1</li>
            <li>initial li2</li>
        </ul>
        <p>dont delete me, im not li, I am paragraph</p>
        <script src="app.js"></script>
    </body>
    JS
    let input = document.querySelector('input');
    let button = document.querySelector('button');
    let ul = document.querySelector('ul');
    button.addEventListener('click', function(){
        let li = document.createElement('li');
        li.append(input.value);
        ul.appendChild(li);
        input.value="";
    })
    //The clickmevent will only on work manually added lis in HTML but not on dynamically added
    // let lis = document.querySelectorAll('li');
    // for(let li of lis) {
    //     li.addEventListener('click', function(e){
    //         li.remove();
    //     })
    // }
    //To remove dynamically added lis we need to listen to parent element
    ul.addEventListener('click',function(e) {
        //console.log('click on ul');
        //console.dir(e);
        //to varify whether the clicked element is LI or not. we can check nodeName
        e.target.remove() && e.target.nodeName === 'LI';
    })

Async JS
    CALL STACK[stack trace in JAVA]
        The mechanism in which the JS interpretator uses to keep track of its place in a 
        script that calls multiple functions.
        How JS 'know' which function is currently running and which all other function had been called from that function.
        the tracking will be LIPO in call stack.
        Once done with excution interpratator will take of that function trace from call stack.
    ex:
    Analyse the call stack section in chrom debbugger.
        // let multiply = function(x,y){
        //     returns x*y;
        // };
        let multiply  = (x,y)=> x*x;

        let square = (x,y)=> multiply(x,y);

        let rightAngleTriangle = (x,y,z)=> {
            console.log(square(x) + square(y) === square(z));
        }

        rightAngleTriangle(3,4,5);

WEB APIs and single threaded - why promises, asyc etc all these ,atters in JS not in other languages???
    Because JS IS SINGLE THREADED!!!
        thats means - at a given point time, a single threaded js can execute at most one line of JS code.
    what happenes whe something take long time in JS i.e huge db data object..?
        JS will handover some tasks to BROWSER that other languagescant do.
        The browers comes with webapis that can perform some background tasks like request or set timeout etc..
        The JS call stack recognises the web API function and pass them off to the browser to take care of.
        Once browser finishes those tasks, they return and are pushed onto JS stack as a callback.
    demo:
    console.log('I print first');
    setTimeout(()=>{
        console.log('sending request to server, i ll print after 3 sec');
    }, 3000);
    console.log('i print second!');

    in above example JS interpretator will send this setTime() to brower and print next statment.
    Then once browser done with execution i will say to JS a there is call back function, then JS wil run that also.

JS PROMIESE
    Why did promises?
    ex: serachMovie('KGF',()=>{
        //if exist do this
    },()=>{
        //if its not do this..go on
    }, 3000);
    Becaus of call back nesting and single thred nature of JS..the exection time increase and performanace of a app decreases.
    To tackle this promises and async function comes inJS.
    promise - its an object representing eventual completion or failure of an asynchronous operation.
        it mainly consists of first success call function and failure call funtion on makeRequest()
        ex
        request = fakeReuqestPromise('someurl')
        request
        .them(()=>{
            //resolves
        })
        .catch(()=>{
            //rejected
        })
    Crete your own promise
        new Promise((resolve,reject)=> {
            resolve();
        })
        PromiseState - resolved
        new Promise((resolve,reject)=> {
            reject();
        })
        PromiseState - rejected
        new Promise((resolve,reject)=> {
        })
        PromiseState - pending

    example of creating out own promise
    let fakeRequest = (url)=>{
            return new Promise((resolve,reject)=>{
                const rand = Math.random();
                setTimeout(()=> {
                    if(rand > 0.7){
                        resolve('Your fake data here!');
                    }
                    reject('Request error!')
                    
                },1000)
            })
        }

        fakeRequest('god1/dog/')
            .then((data)=>{
                console.log("Done with request");
                console.log('You data here: ', data);
            })
            .catch(()=> {
                console.log('Oh NO!!!');
                console.log('occured error is: ', data);
            })
Async keyword - makeup for promises
    *async function are always retunr a prmise
        This below function will return any promise
        function hello() {
        }
        hello();
        but below function will always retunr promise
        async function hello() {
            }
        hello();
    example
        let asyncFun = async () => {
            //if rejected
            throw " Oh noo!!"
            //if resolved
            return "OLALAL";
        }

        asyncFun()
            .then((data)=>{
                console.log('resolved with data : ', data)
            })
            .catch((err)=>{
                console.log('Got an error', err)
            })
await keyword
    *await keyword make asynchronous code look a like synchonous one.
    we can use await key inside function with ' asnc ' keyword.
    await will pause the execution of a function, waiting for a promise to be resolved.
Handling errod in async functions when promise is rejected - using try and catch block
    async funcName = ()=> {
        try{
            let data  = await fakeReq('page1/ss);
            console.log(data);
        } catch(e){
            consolo.log('Erron oaccurs" e);
        }
    }













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