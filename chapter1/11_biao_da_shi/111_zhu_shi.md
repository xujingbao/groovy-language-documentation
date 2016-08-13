# 1.1.1 注释


## 单行注释
单行注释以 // 开始，可以放在一行的任何位置。从//后边，一直到行尾的字符是注释的部分。

// 独立的单行注释  
println "hello" // 注释一直到行尾

## 多行注释

多行注释以 /\* 开始，可以放在一行的任何位置。/\* 后边的内容是注释的部分，包括新行的字符，以第一个 \*/ 关闭注释。多行注释因此可以被放在一个什么的结尾，或者声明里边。

/\*  独立的多行注释  
    跨越两行  \*/  
println "hello" /* 多行注释开始
                   在声明的末尾 */
println 1 /* one */ + 2 /* two */

## Groovy文档注释


Similarly to multiline comments, GroovyDoc comments are multiline, but start with /** and end with */. Lines following the first GroovyDoc comment line can optionally start with a star *. Those comments are associated with:

type definitions (classes, interfaces, enums, annotations),

fields and properties definitions

methods definitions

Although the compiler will not complain about GroovyDoc comments not being associated with the above language elements, you should prepend those constructs with the comment right before it.

 
``` 
/**  
  * A Class description    
  */  
 class Person {  
    /** the name of the person */  
    String name  

    /**  
     * Creates a greeting method for a certain person.  
     *  
     * @param otherPerson the person to greet  
     * @return a greeting message    
     */  
    String greet(String otherPerson) {  
       "Hello ${otherPerson}"  
    }  
}  
```

GroovyDoc follows the same conventions as Java’s own JavaDoc. So you’ll be able to use the same tags as with JavaDoc.


## Shebang line


Beside the single line comment, there is a special line comment, often called the shebang line understood by UNIX systems which allows scripts to be run directly from the command-line, provided you have installed the Groovy distribution and the groovy command is available on the PATH.

#!/usr/bin/env groovy
println "Hello from the shebang line"
The # character must be the first character of the file. Any indentation would yield a compilation error.