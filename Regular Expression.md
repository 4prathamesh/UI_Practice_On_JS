#Regular #Expression

// test method
// return true and falus
// --------------      1)  ------------
// let str="prathamesh g";
// let regx=/g/;
// console.log(regx.test(str));   /* this method return true*/

// let str="prathamesh";
// let regx=/Prathamesh/;
// console.log(regx.test(str));   /* this method return false */

// Matching a literal String with Different Possibilities
// let str="pratha mesh wrs";
// let regx=/prahta|mesh|ppp/; /* | this is pipe operator */
// console.log(regx.test(str));

// How to Create Case Insensitive
// i flag ------------ case insensitive
// let str="Prathamesh";
// let regx=/prathaMesH/i; /* when we use (i) with regx then we create insensitive String */
// console.log(regx.test(str));

// match method  -------------  2)   ---------
// let str="prath mesh Wrr";
// let regx=/mesh/;
// console.log(str.match(regx)); /* if regx is not present in string the match method return null */

// g flag ------ g flag search global in string
// let str="abc def abc";
// let regx=/abd/g; /* if regx is present in String than the return all String other wise return null*/
// console.log(str.match(regx));

// ---- Match Anything with Wildcard period ---- 
// let str="I'll hug a song";
// let regex=/.g/g; /* . dot is use for get one single character from str */
// console.log(str.match(regex));

// let str="bag bug cat";
// let regex=/b[au]g/g; /* in this regex we fing string start with b and end with g and mid char is a or u */
// console.log(str.match(regex));

// ---- Match letters of the Alphabet ---- 
// let str="abc dEf 213";
// let regex=/[a-z]/ig; /* useing this regex match method only return a to z alphabet */
// console.log(str.match(regex));

// ---- Match number and latter of alphabet ---- 
// let str="rty oi km rtyui 123.214789";
// let regex=/[2-7a-z]/ig;
// console.log(str.match(regex));

// ---- Match Single character not specified  ------
//  let str="3 blind mice.";
// let regex=/[^1-9]/g;  /* when we use ^ this symbole than we  not alow that value means match method return all value but not 1 to 9 value*/
// console.log(str.match(regex));

// ---- Match Character that occer one or more time ----
// let str ="praathameshaa";
// let regex =/a+/g;    /* match method return a if a present one or more than one time useing + */
// console.log(str.match(regex));

// ---   match character that occer zero or more time   ----
// let str1="ggooooooal!";
// let str2="gut feelingg";
// let str3="over the moon";
// let regex=/go*/g;
// console.log(str1.match(regex));
// console.log(str2.match(regex));
// console.log(str3.match(regex));

// --- Find the character with lazy matching ---
1.
let str="titanic";
let regex=/t[a-z]*?i/;
console.log(str.match(regex));
// out put :- ti

2.
let str ="<h1>Winter is coming</h1>";
let regex=/<.*?>/;
console.log(str.match(regex));
// out put:- <h1>


// ---- Q) Find one or more Criminals in a Hunt Criminal is (c) ----
let crowd = 'p1p2p3p4p5cccp6p7p6';
let regex=/c+/;
console.log(crowd.match(regex));
 // Out Put:- ccc


 // ---  Match Beginning String Patterns  ---
let str="Cal and Rick both like racing.";
let regex = /^Cal/;  /* ^ this symbol help as to chack Beginning String Patterns  return true if String is match*/
console.log(regex.test(str));
// out Put :- true

// --- Match Ending String Patterns ---
let str ="the laste car on a train is the caboose";
let regex=/caboose$/;
console.log(regex.test(str));
// out put :- true


//   --- Match String with a to z and 0 to 9 by using (\w) ---
let str="The five boxing wizards jump quickly. 123";
let regex=/\w/g; /* \w is use for a to z and 0 to 9 verification */
console.log(str.match(regex)); /* when we use .length we get how many character are present in String */
out put:- 34


//   ----  Match Everything int String but not Letters and numbers ---
// let str="The five boxing wizards jump quickly.";
// let regex=/\W/g; /* when we use capital character then we match non letters and number */
// console.log(str.match(regex).length);
// out put:- 6


// ---  Match all number ---
// let str="Your sandwich will be $5.00";
// let regex=/\d/g; /* \d is use for digit */
// console.log(str.match(regex).length); /* return the length of digit */
// out put :- 3


// ---- match all non number ---
let str="Your sandwich will be $5.00";
let regex=/\D/g;  /*  \D  is use for non number matching */
console.log(str.match(regex).length);
// out put:- 24


//    --- Restrict Possible usernames (3 requirement for user name )----
/*
\d*$  --> \d is use for number and * is use for zero or more number $ is use for laste character of string
1) If there are numbers, they must be at the end.  
2) letters can be lowercase and uppercase (i)
3) At least two characters long.   {3,}
4) Two-letter names can't have numbers.
(^[a-z]{3,}) --- >       ^ this symbol use for start [a-z] use for later 
{3,}  means first parameter is for must be take 3 latter and second is for infinit
*/
let str="JackOfAllTrades54";
let regex=/^[a-z]{3,}\d*$/ig;
console.log(regex.test(str));
// out put :- true



//      ---- Match Whitespace ---
let str="Whitespace is important in separating words";
let regex=/\s/g; /* using \s we can find Whitespace */
console.log(str.match(regex).length);
out put :- 5



//      ---  Match Not whitespace ----
let str="Whitespace is important in separating words";
let regex=/\S/g; /* Capital \S is use for find not WhiteSpace value */
console.log(str.match(regex).length);
// out put :- 38



//      ---  Specify Upper and Lower Number of Matches
let str ="Ohhh no";
let regex=/Oh{3,4} no/; /* {min character , max Character} */
console.log(regex.test(str));
// out put:- true



//      --- Specify Only the Lower Number Of Match ---
let str="Hazzzzah";
let regex=/z{3,}/g;
console.log(regex.test(str));
// out put :- true


//       --- Specify Exact number of MAtch ---
let str = "Timmmmber";
let regex=/Tim{4}ber/;
console.log(regex.test(str));
// out put:- true



//       --- Check for All or None ---
let str="favorite";
let regex =/favou?rite/; /* we use u? if u is present then return true or not then also true */
console.log(regex.test(str));



//       --- Positive and negetive Lookahead ---
1)
// Positive Lookahead --> ?=
// Negetive Lookahead --> ?!
let str = "qu";
let str1 = "qt";
let regex = /q(?=u)/;  // if after q , u is present then return true 
let regex1 = /q(?!=u)/;  // if after q , u is not present then return true 
console.log(str.match(regex));
console.log(str.match(regex1));
console.log(regex.test(str));
console.log(regex1.test(str1));
// out put :- q
//            q
//            true
//            true


2)
let str="astronaut12";
let regex = /(?=\w{5,})(?=\D{2,}\d{2})/;
  console.log(regex.test(str));



//       --- Reuse Patterns Using Capture Groups ---
// 1)
let str="regex regex";
let RegEx=/(\w+)\s\1/;
console.log(RegEx.test(str));
console.log(str.match(RegEx));
// out put:- ["regex regex","regex"]


//2)
let str="12 12 12";
let regex=/(\d+)\s\1\s\1/; // check first number is equls to next 2 number  
console.log(str.match(regex));
out put :- ['12 12 12' , '12']
