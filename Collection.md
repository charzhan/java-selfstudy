# Collection

标签（空格分隔）： java

- 集合
 - **Collection** 单列
          - **List  可以重复**
            - Array List 
            - LinkedList 
          - **Set  不可以重复**
          - TreeSet
 - **Map 双列**
      - HashMap 
```
   Collection<String> as = new ArrayList<>();
        as.add("herll");
        as.add("world");

        as.add("use char");
        Iterator<String> iterator = as.iterator();
        while (iterator.hasNext()){
            System.out.println(iterator.next());
        } 
```
```
Collection<student> as = new ArrayList<student>();
        student s1 = new student("1", 2);
        student s2 = new student("2", 2);
        student s3 = new student("3", 3);
        as.add(s1);
        as.add(s2);
        as.add(s3);
        Iterator<student> iterator = as.iterator();
        while (iterator.hasNext()) {
            System.out.println(iterator.next().toString());
        }

    }
}

class student {
    private String name;
    private int age;

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        this.age = age;
    }


    public student(String name, int age) {
        this.name = name;
        this.age = age;
    }

    public student() {
    }

    @Override
    public String toString() {
        return "student{" +
                "name='" + name + '\'' +
                ", age=" + age +
                '}';
    }
}
```




