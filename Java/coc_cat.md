# Main.java

```.py
public class Main {
    public static <coc_circles> void main(String[] args) {


         System.out.println("Hello world!");
         String [] cats = new String []{"Princess 5 10","Joe 10 14","Bob 1 2"};
         coc_cat test1= new coc_cat(5,4,cats);
         int x = test1.solution();
         System.out.println("Solution is " + x);
         test1.set_year(10);
         x=test1.solution();
         System.out.println("Solution is " + x);

         coc_circle coc = new coc_circle("123456789");
         System.out.println(coc.solve());
    }

}
```

# coc_cat.java

```.py
public class coc_cat {
    private int num_cats;
    private int year;
    private String [] cats;
    public coc_cat(int num_cats, int year, String [] cats) {
        this.num_cats = num_cats;
        this.year = year;
        this.cats = cats;
    }
    public int solution(){
        System.out.println("Solution for "+ num_cats + " "+this.year);
        int cats_alive=0;
        for (int i=0; i<this.cats.length;i++){
            String string_cat = cats[i];
            // Split functions
            String [] parts = string_cat.split(" ");
            String name = parts[0];
            int dob = Integer.parseInt(parts[1]);// date of birth
            int dod = Integer.parseInt(parts[2]);// date of death
            if (dob < this.year && dod > this.year){
                cats_alive+=1;
            }
        }
        return cats_alive;
    }

    public int get_year(){
        return this.year;
    }

    public String[] get_name(){
        return this.cats;
    }

    public int get_num_cats(){
        return this.num_cats;
    }
    public void set_year(int new_year){
        this.year=new_year;
    }

}
```
