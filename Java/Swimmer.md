# Race.java

```.py
public class race {
    private String swimmer;

    private double[] time;


    public race(String swimmer, double[] time){
        this.swimmer=swimmer;
        this.time=time;

    }

    public String showSwimmer(){
        return this.swimmer;
    }
    public double[] showTimes(){
        return this.time;
    }
    public void addSwimmer(String new_swimmer){
        this.swimmer=new_swimmer;
    }
    public void addTimes(double[] new_time){
        this.time=new_time;
    }

    public String question_4a(){
        return "A mutator is a method to change an attribute in a class";
    }

    public String question_4b(){
        return "One additional instance variable of type boolean that could be added to the class Race could be isRaceFinished. The variable isRaceFinished could be used to indicate whether the race has been completed or not. The value of this variable could be set to true when the race is finished and false when it is still ongoing.";
    }

    public String question_4c(){
        return "A class is a template of an instantation and an instantation is a real implementation of the class";
    }

    public String question_4di(){
        return "Better Organization: Aggregation allows you to better organize your code by breaking it down into smaller, more manageable parts. This makes it easier to understand and maintain the code, especially for large or complex systems.";
    }
    public String question_4dii(){
        return "Increased Complexity: By adding another layer of abstraction, aggregation can make the code more complex and harder to understand, especially for those who are not familiar with the codebase.";
    }
    public String question_4f(){
        return "Unicode is a standarizeation of a normalization of this globalized code";
    }
    public String question


}
```
# Swimmer.java

```.py
public class swimmer {
    private String name;
    private String school;
    private String[] eventID;
    private double[] time;
    public swimmer(String name, String school, String [] eventID, double [] time){
        this.name = name;
        this.school = school;
        this.eventID = eventID;
        this.time = time;
    }
    public void show(){
        String time_rounded = String.format("%.5f s", this.getAverageTime());
        System.out.println("[Swimmer] "+this.name + " AVG time: " + time_rounded);
    }
    public void setEventID(String[] eventID) {
        this.eventID = eventID;
    }

    public double getAverageTime(){
        double average = 0.0;
        for (double v : time) {
            average += v;
        }
        return average/ time.length;
    }
}
```

# Main.java

```.py
public class Main {
    public static void main(String[] args) {
        System.out.println("Hello world!");


    }




}
```
