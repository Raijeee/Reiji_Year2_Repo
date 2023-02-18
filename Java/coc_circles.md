# Main

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

# coc_circles.java

```.py
public class coc_circle {
    private String string_number;

    public coc_circle(String input_number){
        this.string_number=input_number;


    }
    //accessor
    public String getString_number(){
        return this.string_number;
    }
    //mutators
    public void setString_number(String string_number) {
        this.string_number = string_number;
    }

    public int solve(){
        int output = 0;
        for (int i=0;i<this.string_number.length();i++){
            char letter = this.string_number.charAt(i);
            if(letter=='9'|| letter=='6' || letter=='0'){
                output += 1;
            }
            if (letter=='8'){
                output+=2;
            }
        }

        return output;
    }

}
```
