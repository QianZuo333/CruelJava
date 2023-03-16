 # Java反射知识
 ```
 public static void main(String[] args) throws Exception{
    Person person = new Person();
    person.setName("test");
    person.setAge(20);
    // Set反射类
    Class<? extends Person> personClass = person.getClass();
    Class<? extends Student> studentClass = student.getClass();
    
    Method[] personClassDeclaredMethods = personClass.getDeclaredMethods();
    Method[] studentClassDeclaredMethods = studentClass.getDeclaredMethods();
    // 把person里面的数据给对应的student
    for (int i = 0; i < personClassDeclaredMethods.lenght; i++) {
        if(personClassDeclaredMethods[i].getName().contains("get")){
            // getName getAge -> setName setAge
            String setterName = "set" + personClassDeclaredMethods[i].getName().substring(3);
            Object getterValue = personClassDeclaredMethods[i].invoke(person);
            for (int j = 0; j < studentDeclaredMethods[j].length; j++){
            // 当student的方法是set的时候，而且恰好是设置同一个variable的setter，把这个时候的person的value赋值给student
              if(studentClassDeclaredMethods[j].getName().equals(setterName)){
                studentClassDeclaredMethods[j].invoke(student.getterValue);
              }
            }
        }
    }
    System.out.println(student.getName() + " - " + student.getAge());
 }
 ```
