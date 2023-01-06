# slip5


Q.1   Write a Java Program to implement Adapter pattern for Enumeration iterator

Q.2  Write a python program to implement Multiple Linear Regression for given dataset.

Q. 3 Using nodejs create a web page to read two file names from user and append contents
of first file into second file.




Write a Java Program to implement Adapter pattern for Enumeration iterator

:
import java.util.*;
 class EnumerationIterator implements Iterator {
 Enumeration enumeration;

 public EnumerationIterator(Enumeration enumeration) {
 this.enumeration = enumeration;
 }

 public boolean hasNext() {
 return enumeration.hasMoreElements();
 }

 public Object next() {
 return enumeration.nextElement();
 } 
public void remove() {
 throw new UnsupportedOperationException();
 }
}
public class Main {
 public static void main (String args[]) {
 Vector v = new Vector(Arrays.asList(args));
 Iterator iterator = new EnumerationIterator(v.elements());
 while (iterator.hasNext()) {
 System.out.println(iterator.next());
 }
 }
} 


Write a python program to implement Multiple Linear Regression for given dataset.
:
from sklearn import linear_model
clf = linear_model.LinearRegression()
clf.fit([[getattr(t, 'x%d' % i) for i in range(1, 8)] for t in texts],
        [t.y for t in texts])


Q. 3 Using nodejs create a web page to read two file names from user and append contents
of first file into second file

:
var fs = require('fs');
var path = require('path')
var data = fs.readFileSync("Sample1.txt","utf8");
fs.appendFile("Sample2.txt", data,(err) =>{
 if(err) {
 console.log(err);
 }
 else{
 console.log("File Content after appending:
",fs.readFileSync("Sample2.txt","utf8"));
 }
});
SAMPLE 1
hello
SAMPLE 2
hello

