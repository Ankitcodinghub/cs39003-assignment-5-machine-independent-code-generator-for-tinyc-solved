# cs39003-assignment-5-machine-independent-code-generator-for-tinyc-solved
**TO GET THIS SOLUTION VISIT:** [CS39003 Assignment 5-Machine Independent Code Generator for tinyC  Solved](https://www.ankitcodinghub.com/product/cs39003-assignment-5-machine-independent-code-generator-for-tinyc-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;92884&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;0&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;0&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;0\/5 - (0 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS39003 Assignment 5-Machine Independent Code Generator for tinyC&nbsp; Solved&quot;,&quot;width&quot;:&quot;0&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 0px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            <span class="kksr-muted">Rate this product</span>
    </div>
    </div>
<div class="page" title="Page 1">
<div class="layoutArea">
<div class="column">
Assignment 5: Machine Independent Code Generator for tinyC

1 Preamble – tinyC

The Lexical Grammar (Assignment 3) and the Phase Structure Grammar (As- signment 4) for tinyC have already been defined as subsets of the C language specification from the International Standard ISO/IEC 9899:1999 (E).

In this assignment you will write the semantic actions in Bison to translate a tinyC program into an array of 3-address quad’s, a supporting symbol table, and other auxiliary data structures. The translation should be machine-independent, yet it has to carry enough information so that you can later target it to a specific architecture (x86 / IA-32 / x86-64).

2 Scope of Machine-Independent Translation

Focus on the following from the different phases to write actions for translation.

2.1 Expression Phase

Support all arithmetic, shift, relational, bit, logical (boolean), and assignment expressions excluding:

<ol>
<li>sizeof operator</li>
<li>Comma (,) operator</li>
<li>Compound assignment operators
*= /= %= += -= &lt;&lt;= &gt;&gt;= &amp;= ^= |= Support only simple assignment operator (=)
</li>
<li>Structure component expression</li>
</ol>
2.2 Declarations Phase

Support for declarations should be provided as follows:

<ol>
<li>Simple variable, pointer, array, and function declarations should be sup- ported. For example, the following would be translated:
<pre>     float d = 2.3;
     int i, w[10];
     int a = 4, *p, b;
     void func(int i, float d);
     char c;
</pre>
</li>
<li>Consider only void, char, int, and float type-specifiers. As specified in C, char and int are to be taken as signed.
For computation of offset and storage mapping of variables, assume the following sizes1 (in bytes) of types:
</li>
</ol>
1Using hard-coded sizes for types does not keep the code machine-independent. Hence you may want to use constants like size of char, size of int, size of float, and size of pointer for sizes that can be defined at the time of machine-dependent targeting.

</div>
</div>
<div class="layoutArea">
<div class="column">
1

</div>
</div>
</div>
<div class="page" title="Page 2">
<div class="layoutArea">
<div class="column">
Type

</div>
<div class="column">
Size Remarks

</div>
</div>
<div class="layoutArea">
<div class="column">
void

char

int

float

void* 4 All pointers have same size

It may also help to support an implicit bool (boolean) type with con- stants 1 (TRUE) and 0 (FALSE). This type may be inferred for a logical expression or for an int expression in logical context. Note that the users cannot define, load, or store variables of bool type explicitly, hence it is not storable and does not have a size.

<ol start="3">
<li>Initialization of arrays may be skipped.</li>
<li>storage-class-specifier, enum-specifier, type-qualifier, and function-specifier may be skipped.</li>
<li>Function declaration with only parameter type list may be skipped. Hence,
<pre>     void func(int i, float d);
</pre>
should be supported while

<pre>     void func(int, float);
</pre>
may not be.
</li>
</ol>
2.3 Statement Phase

Support all statements excluding:

1. Declaration within for.

2. All Labelled statements (labeled-statement).

3. switch in selection-statement.

4. All Jump statements (jump-statement) except return.

2.4 External Definitions Phase

Support function definitions and skip external declarations.

3 The 3-Address Code

Use the 3-Address Code specification as discussed in the class. For easy reference the same is reproduced here. Every 3-Address Code:

<ul>
<li>Uses only up to 3 addresses.</li>
<li>Is represented by a quad comprising – opcode, argument 1, argument 2,
and result; where argument 2 is optional.
</li>
</ul>
3.1 Address Types

<ul>
<li>Name: Source program names appear as addresses in 3-Address Codes.</li>
<li>Constant: Many different types and their (implicit) conversions are al-
lowed as deemed addresses.
</li>
<li>Compiler-Generated Temporary: Create a distinct name each time a tem- porary is needed – good for optimization.</li>
</ul>
</div>
</div>
<div class="layoutArea">
<div class="column">
undefined

</div>
</div>
<div class="layoutArea">
<div class="column">
1 4 8

</div>
</div>
<div class="layoutArea">
<div class="column">
2

</div>
</div>
</div>
<div class="page" title="Page 3">
<div class="layoutArea">
<div class="column">
3.2 Instruction Types

For Addresses x, y, z, and Label L

<ul>
<li>Binary Assignment Instruction: For a binary op (including arithmetic,
shift, relational, bit, or logical operators):

x = y op z
</li>
<li>Unary Assignment Instruction: For a unary operator op (including unary
minus or plus, logical negation, bit, and conversion operators):

x = op y
</li>
<li>Copy Assignment Instruction: x=y</li>
<li>Unconditional Jump: goto L</li>
<li>Conditional Jump: – Value-based:
<pre>         if x goto L
         ifFalse x goto L
</pre>
– Comparison-based: For a relational operator op (including &lt;, &gt;, ==, ! =, ≤, ≥):

<pre>         if x relop y goto L
</pre>
</li>
<li>Procedure Call: A procedure call p(x1, x2, …, xN) having N ≥ 0 pa-
rameters is coded as (for addresses p, x1, x2, and xN):

<pre>     param x1
     param x2
     ...
     param xN
     y = call p, N
</pre>
Note that N is not redundant as procedure calls can be nested.
</li>
<li>Return Value: Returning a return value and / or assigning it is optional.
If there is a return value v it is returned from the procedure p as:

return v
</li>
<li>Indexed Copy Instructions: x = y[z]
x[z] = y
</li>
<li>Address and Pointer Assignment Instructions:
<pre>     x = &amp;y
     x = *y
     *x = y
</pre>
</li>
</ul>
</div>
</div>
<div class="layoutArea">
<div class="column">
3

</div>
</div>
</div>
<div class="page" title="Page 4">
<div class="layoutArea">
<div class="column">
4

Lexer &amp; Parser

Augmentation

Attributes

Symbol Table

</div>
<div class="column">
Design of the Translator

Use the Flex and Bison specifications (if required you may correct your specifications) you had developed in Assignments 3 and 4 respectively and write semantic actions for translating the subset of tinyC as specified in Section 2. Note that many grammar rules of your tinyC parser may not have any action or may just have propagate-only actions. Also, some of the lexical tokens may not be used.

Augment the grammar rules with markers and add new grammar rules as needed for the intended semantic actions. Justify your augmentation decisions within comments of the rules.

Design the attributes for every grammar symbol (terminal as well as non- terminal). List the attributes against symbols (with brief justification) in comment on the top of your Bison specification file. Highlight the inherited attributes, if any.

Use symbol tables for user-defined (including arrays and pointers) vari- ables, temporary variables and functions.

Name Type Initial Size Offset Nested

</div>
</div>
<div class="layoutArea">
<div class="column">
Value

… … … … For example, for

<pre>float d = 2.3;
int i, w[10];
int a = 4, *p, b;
void func(int i, float d);
char c;
</pre>
the Symbol Tables will look like:

</div>
<div class="column">
Table

… …

</div>
</div>
<div class="layoutArea">
<div class="column">
ST(global)

Name Type

d float

i int

w array(10, int) a int

p ptr(int)

b int

func function

</div>
<div class="column">
This is the Symbol Table for global symbols

Initial Size Offset Nested

</div>
</div>
<div class="layoutArea">
<div class="column">
Value

2.3 8

null 4

null 40

4 4 52null

</div>
<div class="column">
Table

</div>
</div>
<div class="layoutArea">
<div class="column">
0 null

</div>
</div>
<div class="layoutArea">
<div class="column">
8 null 12 null

</div>
</div>
<div class="layoutArea">
<div class="column">
c

</div>
<div class="column">
char

</div>
<div class="column">
null 4 null 4 null 0 null 1

</div>
<div class="column">
56 null

60 null

64 ptr-to-ST(func) 64 null

</div>
</div>
<div class="layoutArea">
<div class="column">
ST(func) This is the Symbol Table for function func Name Type Initial Size Offset Nested

</div>
</div>
<div class="layoutArea">
<div class="column">
Value

i intnull 4 0null

d float null 8 4 null retVal void null 0 12 null

</div>
<div class="column">
Table

</div>
</div>
<div class="layoutArea">
<div class="column">
The Symbol Tables may support the following methods:

update(…) A method to update different fields of an existing entry.

print(…) A method to print the Symbol Table in a suitable format.

</div>
</div>
<table>
<tbody>
<tr>
<td>
<div class="layoutArea">
<div class="column">
lookup(…)

</div>
</div>
</td>
<td>
<div class="layoutArea">
<div class="column">
A method to lookup an id (given its name or lexeme) in the Symbol Table. If the id exists, the entry is returned, otherwise a new entry is created.

</div>
</div>
</td>
</tr>
<tr>
<td>
<div class="layoutArea">
<div class="column">
<pre>gentemp(...)
</pre>
</div>
</div>
</td>
<td>
<div class="layoutArea">
<div class="column">
A static method to generate a new temporary, insert it to the Symbol Table, and return a pointer to the entry.

</div>
</div>
</td>
</tr>
</tbody>
</table>
<div class="layoutArea">
<div class="column">
4

</div>
</div>
</div>
<div class="page" title="Page 5">
<div class="layoutArea">
<div class="column">
Quad Array

</div>
<div class="column">
<ul>
<li>The fields and the methods are indicative. You may change their name, functionality and also add other fields and / or methods that you may need.</li>
<li>It should be easy to extend the Symbol Table as further features are supported and more functionality is added.</li>
<li>The global symbol table is unique.</li>
<li>Every function will have a symbol table of its parameters and au- tomatic variables. This symbol table will be nested in the global symbol table.</li>
<li>Symbol definitions within blocks are naturally carried in separate symbol tables. Each such table will be nested in the symbol table of the enclosing scope. This will give rise to an implicit stack of symbol tables (global one being the bottom-most) the while symbols are processed during translation. The search for a symbol starts from the top-most (current) table and goes down the stack up to the global table.
The array to store the 3-address quad’s. Index of a quad in the array is the address of the 3-address code. The quad array will have the following fields (having usual meanings)
</li>
</ul>
</div>
</div>
<div class="layoutArea">
<div class="column">
Note:

</div>
</div>
<div class="layoutArea">
<div class="column">
op arg 1 arg 2 result

… … … …

</div>
</div>
<div class="layoutArea">
<div class="column">
Note:

</div>
</div>
<div class="layoutArea">
<div class="column">
• arg 1 and / or arg 2 may be a variable (address) or a constant. • result is variable (address) only.

• arg 2 may be null.

</div>
</div>
<div class="layoutArea">
<div class="column">
For example, if

translates to

</div>
<div class="column">
<pre>int i = 10, a[10], v = 5;
    ...
</pre>
<pre>do i = i - 1; while (a[i] &lt; v);
</pre>
</div>
</div>
<div class="layoutArea">
<div class="column">
<pre>100: t1 = i - 1
101: i = t1
102: t2 = i * 4
103: t3 = a[t2]
104: if t3 &lt; v goto 100
</pre>
</div>
</div>
<div class="layoutArea">
<div class="column">
the quad’s are represented as:

Index op arg 1 arg 2

</div>
<div class="column">
result

</div>
</div>
<div class="layoutArea">
<div class="column">
… … … … …

</div>
</div>
<div class="layoutArea">
<div class="column">
– i 1 t1 = t1 i

* i 4 t2 =[] a t2 t3

</div>
</div>
<div class="layoutArea">
<div class="column">
<pre>            100
            101
            102
            103
            104
</pre>
print(…) A method to print the quad array in a suitable for- mat.

</div>
</div>
<div class="layoutArea">
<div class="column">
&lt; t3 v 100 The Quad Array may support the following methods:

</div>
</div>
<table>
<tbody>
<tr>
<td>
<div class="layoutArea">
<div class="column">
emit(…)

</div>
</div>
</td>
<td>
<div class="layoutArea">
<div class="column">
An overloaded static method to add a (newly gen- erated) quad of the form: result = arg1 op arg2 where op usually is a binary operator. If arg2 is missing, op is unary. If op also is missing, this is a copy instruction.

</div>
</div>
</td>
</tr>
</tbody>
</table>
<div class="layoutArea">
<div class="column">
5

</div>
</div>
</div>
<div class="page" title="Page 6">
<div class="layoutArea">
<div class="column">
Global Functions

</div>
<div class="column">
• The fields and the methods are indicative. You may change their name, functionality and also add other fields and / or methods that you may need.

Following (or similar) global functions and more may be needed to imple- ment the semantic actions:

makelist(i)

A global function to create a new list containing only i, an index into the array of quad’s, and to return a pointer to the newly created list.

merge(p1, p2)

A global function to concatenate two lists pointed to by p1 and p2 and to return a pointer to the concatenated list.

backpatch(p, i)

A global function to insert i as the target label for each of the quad’s on the list pointed to by p.

typecheck(E1, E2)

A global function to check if E1 &amp; E2 have same types (that is, if &lt;type of E1&gt; = &lt;type of E2&gt;). If not, then to check if they have compatible types (that is, one can be converted to the other), to use an appropri- ate conversion function conv&lt;type of E1&gt;2&lt;type of E2&gt;(E) or conv&lt;type of E2&gt;2&lt;type of E1&gt;(E) and to make the necessary changes in the Symbol Table entries. If not, that is, they are of incompatible types, to throw an exception during translation.

conv&lt;type1&gt;2&lt;type2&gt;(E)

A global function to converta an expression E from its current type type1 to target type type2, to adjust the attributes of E accordingly, and finally to generate additional codes, if needed.

aIt is assumed that this function is called from typecheck(E1, E2) and hence the conversion is possible.

Naturally, these are indicative and should be adopted as needed. For every function used clearly explain the input, the output, the algorithm, and the purpose with possible use at the top of the function.

</div>
</div>
<div class="layoutArea">
<div class="column">
For example the above state of the array may be printed (with the symbol information) as:

</div>
</div>
<div class="layoutArea">
<div class="column">
Note:

</div>
</div>
<div class="layoutArea">
<div class="column">
void main() {

<pre>    int i = 10;
    int a[10];
    int v = 5;
    int t1;
</pre>
<pre>    int t2;
    int t3;
</pre>
<pre>    L100: t1 = i - 1;
    L101: i = t1;
    L102: t2 = i * 4;
    L103: t3 = a[t2];
    L104: if (t3 &lt; v) goto L100;
</pre>
}

</div>
</div>
<div class="layoutArea">
<div class="column">
6

</div>
</div>
</div>
<div class="page" title="Page 7">
<div class="layoutArea">
<div class="column">
5

1.

2. 3.

4.

</div>
<div class="column">
The Assignment

Write a 3-Address Code translator based on the Flex and Bison specifica- tions of tinyC. Assume that the input tinyC file is lexically, syntactically, and semantically correct. Hence no error handling and / or recovery is expected.

Prepare a Makefile to compile and test the project.

Prepare test input files ass5 roll test&lt;number&gt;.c to test the semantic ac-

</div>
</div>
<div class="layoutArea">
<div class="column">
tions and generate the translation output in

Name your files as follows:

File

Flex Specification

Bison Specification

Data Structures (Class Definitions) &amp; Global Function Prototypes

Data Structures, Function Implementa- tions &amp; Translator main()

Test Inputs

Test Outputs

</div>
<div class="column">
ass5 roll quads&lt;number&gt;.out. Naming

ass5 roll.l

ass5 roll.y

ass5 roll translator.h

ass5 roll translator.cxx ass5 roll test&lt;number&gt;.c

</div>
</div>
<div class="layoutArea">
<div class="column">
5.

</div>
<div class="column">
ass5 roll quads&lt;number&gt;.out Prepare a tar-archive with the name ass5 roll.tar containing all the files

</div>
</div>
<div class="layoutArea">
<div class="column">
and upload to Moodle.

</div>
</div>
<div class="layoutArea">
<div class="column">
6

</div>
</div>
</div>
