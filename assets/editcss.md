Steps to edit css
1. find the element's class or id or tag
2. css css within in main.css or code.css that should to
3. Use inspect element feature to find the right DOM or tag or class

/* Selects all <span> elements inside <div> elements */
div span {
    color: blue;
}

/* Selects all <p> elements that are direct children of <div> elements */
div > p {
    color: green;
}

/* Selects all <li> elements inside <ul> elements with class .nav-secondary */
. is used to select elements by class attribute

for nested simply right
.nav-secondary ul li {
    display: inline;
    margin-right: 15px;
}

/* Selects all <a> elements inside <li> elements that are inside <ul> elements with class .nav-secondary */
.nav-secondary ul li a {
    color: #007bff;
    text-decoration: none;
}

.nav-secondary ul li a:hover {
    color: #0056b3;
    text-decoration: underline;
}


The z-index property in CSS controls the stacking order of elements. Elements with a higher z-index value will appear in front of elements with a lower z-index value. The z-index property only works on positioned elements (i.e., elements with a position value other than static).


padding gives space around all the elements
