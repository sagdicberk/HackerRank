```java
public static List<Integer> gradingStudents(List<Integer> grades) {
    // Write your code here
    List modifiedList = new ArrayList<Integer>();
    
        for (Integer grade : grades) {
            int temp = 0;
            if (grade >= 38) {
                temp = grade;
                while (temp %5 != 0) {
                    temp++;
                }
                if ((temp - grade ) < 3 ) {
                    modifiedList.add(temp);
                }else{
                    modifiedList.add(grade);
                }
                
            }else{
                modifiedList.add(grade);
            }
        }
        
        return modifiedList;
    }
````
