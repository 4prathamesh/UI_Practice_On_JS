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

// Match Anything with Wildcard period
// let str="I'll hug a song";
// let regex=/.g/g; /* . dot is use for get one single character from str */
// console.log(str.match(regex));

// let str="bag bug cat";
// let regex=/b[au]g/g; /* in this regex we fing string start with b and end with g and mid char is a or u */
// console.log(str.match(regex));

// Match letters of the Alphabet
// let str="abc dEf 213";
// let regex=/[a-z]/ig; /* useing this regex match method only return a to z alphabet */
// console.log(str.match(regex));

// Match number and latter of alphabet
// let str="rty oi km rtyui 123.214789";
// let regex=/[2-7a-z]/ig;
// console.log(str.match(regex));

// Match Single character not specified
//  let str="3 blind mice.";
// let regex=/[^1-9]/g;  /* when we use ^ this symbole than we  not alow that value */
// console.log(str.match(regex));

// Match Character that occer one or more time
// let str ="praathameshaa";
// let regex =/a+/g;
// console.log(str.match(regex));

// match character that occer zero or more time
// let str1="ggooooooal!";
// let str2="gut feelingg";
// let str3="over the moon";
// let regex=/go*/g;
// console.log(str1.match(regex));
// console.log(str2.match(regex));
// console.log(str3.match(regex));
