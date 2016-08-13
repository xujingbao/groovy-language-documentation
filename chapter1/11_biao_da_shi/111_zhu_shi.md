# 1.1.1 注释


## 单行注释

Single line comments start with // and can be found at any position in the line. The characters following //, till the end of the line, are considered part of the comment.

// a standalone single line comment
println "hello" // a comment till the end of the line

## 多行注释


A multiline comment starts with /* and can be found at any position in the line. The characters following /* will be considered part of the comment, including new line characters, up to the first */ closing the comment. Multiline comments can thus be put at the end of a statement, or even inside a statement.

/* a standalone multiline comment
   spanning two lines */
println "hello" /* a multiline comment starting
                   at the end of a statement */
println 1 /* one */ + 2 /* two */

## Groovy文档注释


Similarly to multiline comments, GroovyDoc comments are multiline, but start with /** and end with */. Lines following the first GroovyDoc comment line can optionally start with a star *. Those comments are associated with:

type definitions (classes, interfaces, enums, annotations),

fields and properties definitions

methods definitions

Although the compiler will not complain about GroovyDoc comments not being associated with the above language elements, you should prepend those constructs with the comment right before it.

> 
> /**  
>  * A Class description    
>  */  
> class Person {  
>    /** the name of the person */  
>    String name  
>
>    /**  
>     * Creates a greeting method for a certain person.  
>     *  
>     * @param otherPerson the person to greet  
>     * @return a greeting message    
>     */  
>    String greet(String otherPerson) {  
>       "Hello ${otherPerson}"  
>    }  
>}  

GroovyDoc follows the same conventions as Java’s own JavaDoc. So you’ll be able to use the same tags as with JavaDoc.


## Shebang line


Beside the single line comment, there is a special line comment, often called the shebang line understood by UNIX systems which allows scripts to be run directly from the command-line, provided you have installed the Groovy distribution and the groovy command is available on the PATH.

#!/usr/bin/env groovy
println "Hello from the shebang line"
The # character must be the first character of the file. Any indentation would yield a compilation error.