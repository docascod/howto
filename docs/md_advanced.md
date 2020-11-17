# Advanced Syntax

## Images

### Bloc vs/inline images

````markdown
An image with text in same line, is an ![pdfwidth=15%](_media/inline.png)image, also it is a bloc image.
````

### Image alignment

````markdown
![align=left](_media/left.png)
````

````markdown
![align=center](_media/center.png)
````

````markdown
![align=right](_media/right.png)
````

### Properties

Image width :

````markdown
![pdfwidth=20%,align=center](_media/scaled.png)
````

Image title :

````markdown
![title=The title,align=center](_media/titled.png)
````

## Code blocs

### Callout

````markdown
​```java
public class HelloWorld { // <1>
  public static void main(String[] args) {
    // Prints "Hello, World" to the terminal window.  
    System.out.println("Hello, World"); // <2>
}
})
```

<1> class declaration

<2> hello world !
````

### External source file

​````markdown
​```java
include::helloworld.java[]
```
````

### Line numbers
​````markdown
​```java,linenums
include::helloworld.java[]
```
````

### Partial file integration

​````markdown
​```java
include::helloworld.java[lines=2..5]
```
````

## Text blocs

To use special text blocs, start your line with `NOTE:` or `TIP:` or `IMPORTANT:` or `WARNING` or `CAUTION`

​````markdown
NOTE: Just a note...
````

````markdown
TIP: Pro tip...
````

````markdown
IMPORTANT: Don't forget...
````

````markdown
WARNING: Watch out for...
````

````markdown
CAUTION: Ensure that...
````

## Tables

### Caption

````markdown
| A   | B   | C   |
| --- |:---:| ---:|
| aa  | bb  | cc  |
| 123 | 456 | 789 |

Table: caption for sample basic table
````

## Multi columns layout

To display document on several columns you must use a table with hidden borders. Just add `table_hide` comment before your table.

````markdown
<!-- table_hide -->

|   |   |
| --- |---:|
| ![pdfwidth=100](_media/inline.png) | image on left  |
````

