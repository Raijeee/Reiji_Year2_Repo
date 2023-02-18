# Main.java

```.py
import java.util.Arrays;
import java.util.Random;
public class Main {
    public static void main(String args[] ) {
        Random rand_num = new Random(12345);
        int [] scores = new int[10];
        for (int i=0; i<10;i++){

            scores[i]=rand_num.nextInt(0,100);
        }

        System.out.println(Arrays.toString(scores));
        int [] sorted =new int[10];
        for (int i=0;i<10;i++){
            for (int k=0;k<9;k++) {
                if (scores[i]==i){
                    scores[i]=sorted[i];
                }
            }
            System.out.println(Arrays.toString(sorted));
        }
    }
}
```
