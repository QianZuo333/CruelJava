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
    for (int i = 0; i < personClassDeclaredMethods.lenght; i++) {
        if(personClassDeclaredMethods[i].getName().contains("get")){
            String setterName = "set" + personClassDeclaredMethods[i].getName().substring(3);
            Object getterValue = personClassDeclaredMethods[i].invoke(person);
            for (int j = 0; j < studentDeclaredMethods[j].length; j++){
              if(studentClassDeclaredMethods[j].getName().equals(setterName)){
                studentClassDeclaredMethods[j].invoke(student.getterValue);
              }
            }
        }
    }
    System.out.println(student.getName() + " - " + student.getAge());
 }
 ```
