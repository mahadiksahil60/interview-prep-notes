**Functional Dependencies**

If a column can be used to determine the value of another clumn then its called functional dependencie

There are various types of functional depedencies. 

**Trivial dependencies** 	
---
In trivial functional dependency the dependent is a subset of the determinant. 

For Example:
AB ---> B

Where B is a subset of AB

rollNo Name age 

rollNo, name --> name

Here only roll no could identify name so its a trivial dependency

**Non Trivial Dependency**
---
In non trivial functional dependency the subset is not strictly the subset of the determinant. 

For Example : 

Name RollNo age 

here rollno --> name is a non trivial depedency since name is not a subset of roll no. 

**Semi Non Trivial Dependencies**
---

Its a mixture of the non trivial as well as trivial dependency, in this case 

student_id course_id course_name 


here {student_id, course_id} --> course_id 

since, course id is present both left and right it can be called as trivial dependency 
 but if you look carefully you cannot determine

 student_id => course_id 

 Hence this is a semi non trivial dependency

 **Multivalued Dependencies**
 ----
 In this type of dependency, multiple dependents are dependent upon single determinant but the dependents have no co relation to each other.

 For Example 

 Bike_model | Color } Accessories


Here, Both color and accessories are dependent upon the bike model and not each other
Hence, it is called multivalued dependency

**Transitive Dependencies**
---
In this type of dependency, the dependent of one determinant is a determinant of another dependent

For Example A --> B and B --> C

According to the ***axiom of transitivity***

A --> C

**Fully Functional Dependency**
--- 
In this type of dependency, the dependent is depending upon the entire composite key and not any part of it alone 

Just like in trivial dependency the dependent could be determined by one of the key attribute here only the combination of the determinant can determine the value of the dependend

**Partial Dependency**
---
In this type of dependency, the dependent is dependent on only one of the composite key in the determinant section 

This is total opposite of fully functional dependencies.

****NOTE****

These fuctional dependencies check for different properties and are not always mutually exclusive. Some properties like fully functional dependecy and non trivial depencies should be followed by a good database design.


