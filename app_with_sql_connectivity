package GUIInjava.JavaFx.Loginpage;

import java.sql.Connection;
import java.sql.Date;
import java.sql.DriverManager;
import java.sql.PreparedStatement;
import java.sql.ResultSet;
import java.sql.SQLException;
import java.sql.Statement;
import java.io.File;
import java.io.FileOutputStream;
import java.io.IOException;
import java.io.PrintWriter;
import java.net.MalformedURLException;
import java.net.URL;
import java.net.URLConnection;
import java.time.LocalDate; 
import javafx.application.Application;
import javafx.event.ActionEvent;
import javafx.event.Event;
import javafx.event.EventHandler;
import javafx.geometry.Insets;
import javafx.geometry.Pos;
import javafx.scene.Scene;
import javafx.scene.control.Button;
import javafx.scene.control.ChoiceBox;
import javafx.scene.control.DatePicker;
import javafx.scene.control.Label;
import javafx.scene.control.TextArea;
import javafx.scene.control.TextField;
import javafx.scene.image.Image;
import javafx.scene.layout.FlowPane;
import javafx.scene.layout.GridPane;
import javafx.scene.layout.HBox;
import javafx.scene.layout.StackPane;
import javafx.scene.paint.Color;
import javafx.scene.text.Font;
import javafx.scene.text.FontPosture;
import javafx.scene.text.FontWeight;
import javafx.scene.text.Text;
import javafx.stage.Stage;
import javafx.stage.Window;



// main class
public class LoginForm extends Application {
    
    //username and password
    public static String  name="nitj";
    public static String pass="123456";


    //start method
    @Override
    public void start(Stage stage) throws Exception { 
        
        
        //creating grid pane and setting it's position
        GridPane grid =new GridPane();
        grid.setAlignment(Pos.CENTER);
        grid.setHgap(10);
        grid.setVgap(20);
        grid.setPadding(new Insets(25, 25, 25, 25));
        
        
        //adding text ,text field and labels
        Text text=new Text("WELCOME TO LOGIN");
        text.setFill(Color.BLACK);
        text.setFont(Font.font("Muller Next",FontWeight.SEMI_BOLD,FontPosture.REGULAR, 35));
        grid.add(text,0,0,2,1);


        //creating label
        Label username=new Label("User Name : ");
        username.setFont(Font.font(STYLESHEET_CASPIAN,FontWeight.BOLD, null, 15));
        grid.add(username, 0,1);

        //adding text field
        TextField userTextField=new TextField();
        grid.add(userTextField,1,1);
        
        
        //label for password
        Label password=new Label("Password : ");
        password.setFont(Font.font(STYLESHEET_CASPIAN,FontWeight.BOLD, null, 15));
        grid.add(password, 0, 2);
        
        
        //adding textfield for the password
        TextField passTextField=new TextField();
        grid.add(passTextField, 1, 2);
        
        
        //adding forgot button
        Button forgButton=new Button("Forgot password?");
        grid.add(forgButton,1,3);
        
        //adding signin button
        Button sigButton=new Button("Sign in");
        HBox hbtBox=new HBox(10);
        hbtBox.setAlignment(Pos.BOTTOM_RIGHT);
        hbtBox.getChildren().addAll(sigButton,forgButton);
        grid.add(hbtBox, 1, 3);
        
        
        
        
        //action to perform
        Text actiontarget=new Text();
        grid.add(actiontarget,1 , 4);
        
        
        
        //setting action to the signin button
        sigButton.setOnAction(new EventHandler<ActionEvent>() {
            
            @Override
            public void handle(ActionEvent e) {
                String Username=userTextField.getText();
                String Password=passTextField.getText();
                actiontarget.setFill(Color.RED);
                
                //authenticating the username and password
                if(Username.equals(name) && Password.equals(pass)){
                    openNewPane();
                    stage.close();
                    
                }
                else{
                    actiontarget.setText("incorrect username or password");
                }
            }
            
        });
        
        
        
        //setting action to the forgot password button
        forgButton.setOnAction(new EventHandler<ActionEvent>() {
            
            @Override
            public void handle(ActionEvent e) {
                actiontarget.setFill(Color.RED);
                actiontarget.setText("CONTACT ADMIN");
            }
            
        });
        
    
        
        
       

        Scene scene=new Scene(grid,800,500);
        stage.setScene(scene);
        scene.getStylesheets().add(LoginForm.class.getResource("LoginForm.css").toExternalForm());
        stage.setTitle("Login form");
        try {
            stage.getIcons().add(new Image("D:\\PROGRAMING_CODES\\java\\GUIInjava\\JavaFx\\Loginpage\\logo.png"));
        } catch (Exception e) {
            // TODO: handle exception
        }
        stage.show();
        stage.setResizable(true);
    }








     
    // NEW WINDOW WHEN THE AUTHENTICATION IS COMPLETED
    private void openNewPane() {
        
        
        
        
        
        //creating new stage
        Stage newStage = new Stage();
        newStage.setTitle("New Pane");
        
        
        //creating flowpane
        FlowPane flowPane=new FlowPane();
        
        //adding text area for the database
        
        
        
        
        
        //creating grid pane and setting it's position
        GridPane gridnew =new GridPane();
        // gridnew.setGridLinesVisible(true);
        gridnew.setAlignment(Pos.TOP_LEFT);
        gridnew.setHgap(10);
        gridnew.setVgap(20);
        gridnew.setPadding(new Insets(0,0,0,10));
        
        
        //adding label for name
        Label NameLabel=new Label("Name");
        NameLabel.setFont(Font.font(STYLESHEET_CASPIAN,FontWeight.BOLD, null, 15));
        NameLabel.setPadding(new Insets(20, 0, 0, 0));
        gridnew.add(NameLabel, 0, 0);
        
        
        //adding the textbox for the Name
        TextField namTextField=new TextField();
        namTextField.setPromptText("Enter full name");
        gridnew.add(namTextField,0,1);
        
        
        
        //adding label for contact
        Label ContactLabel=new Label("Contact");
        ContactLabel.setFont(Font.font(STYLESHEET_CASPIAN,FontWeight.BOLD, null, 15));
        gridnew.add(ContactLabel, 0, 2);
        
        
        
        //adding the textbox for the Name
        TextField ContactTextField=new TextField();
        ContactTextField.setPromptText("Enter contact no.");
        gridnew.add(ContactTextField,0,3);
        
        
        
        //adding label for contact
        Label EmailLabel=new Label("Email");
        EmailLabel.setFont(Font.font(STYLESHEET_CASPIAN,FontWeight.BOLD, null, 15));
        gridnew.add(EmailLabel, 0, 4);
        
        
        
        //adding the textbox for the Name
        TextField EmailTextField=new TextField();
        EmailTextField.setPromptText("Enter the email");
        gridnew.add(EmailTextField,0,5);
        
        
        
        //adding the label for the gender
        Label GenderLabel=new Label("Gender");
        GenderLabel.setFont(Font.font(STYLESHEET_CASPIAN,FontWeight.BOLD, null, 15));
        gridnew.add(GenderLabel, 0, 6);
        
        
        //adding choice box
        ChoiceBox<String> GenderChoicebox=new ChoiceBox<>();
        GenderChoicebox.getItems().addAll("MALE","FEMALE");
        gridnew.add(GenderChoicebox, 0, 7);
        

        //adding label for datepicker
        Label DOBLabel=new Label("Date Of Birth (DOB) (DD/MM/YYYY)");
        DOBLabel.setFont(Font.font(STYLESHEET_CASPIAN,FontWeight.BOLD, null, 15));
        gridnew.add(DOBLabel, 0, 8);
        
        //adding datepicker for DOB
        DatePicker DobdatePicker =new DatePicker();
        DobdatePicker.setOnAction(new EventHandler() {
            public void handle(Event t) {
                LocalDate date = DobdatePicker.getValue();
                System.err.println("Selected date: " + date);
            }
        });
        DobdatePicker.setPromptText("Select your DOB");
        gridnew.add(DobdatePicker, 0, 9);

        
        
        //adding label for the stream
        Label StreamLabel=new Label("Stream");
        StreamLabel.setFont(Font.font(STYLESHEET_CASPIAN,FontWeight.BOLD, null, 15));
        gridnew.add(StreamLabel, 0, 10);
        
        
        //adding choicebox for the stream
        ChoiceBox<String> Streamchoicebox=new ChoiceBox<>();
        Streamchoicebox.getItems().addAll("TEXTILE","COMPUTER SCIENCE","MECHANICAL","CIVIL","INFORMATION TECHNOLOGY","PRODUCTION","ELECTRONICS");
        gridnew.add(Streamchoicebox, 0, 11);
        
        
        
        //creating add button
        Button Addbutton = new Button("ADD");
        Addbutton.setAlignment(Pos.CENTER_LEFT);
        
        
        
        //delete button to delete the record
        Button deleterec=new Button("DELETE");
        deleterec.setAlignment(Pos.CENTER_RIGHT);
        gridnew.add(deleterec, 0, 12);
        
        
        //creating hbox 
        HBox editbuttinshbox=new HBox(20);
        editbuttinshbox.getChildren().addAll(Addbutton,deleterec);
        
        gridnew.add(editbuttinshbox, 0, 12);
        
        
        
        //adding the text area to the new scene
        TextArea textArea=new TextArea();
        textArea.setPrefSize(800,500);
        textArea.setPadding(new Insets(0, 0, 0,20));
        textArea.setEditable(false);
        
        
        //setting action on the add button
        Addbutton.setOnAction(new EventHandler<ActionEvent>() {
            
            @Override
            public void handle(ActionEvent arg0) {
                textArea.appendText(namTextField.getText()+"  "+ContactTextField.getText()+"  "+EmailTextField.getText()+"  "+GenderChoicebox.getValue()+"  "+DobdatePicker.getValue()+"  "+Streamchoicebox.getValue()+"\n");
                textArea.setFont(Font.font(STYLESHEET_CASPIAN, FontWeight.BOLD, null, 20));
                
                try {
                    //loading the jdbc driver for inputting and updating the data to the sql tables
                    Class.forName("com.mysql.cj.jdbc.Driver");
                }
                
                 catch (ClassNotFoundException e) {
                    // TODO Auto-generated catch block
                    e.printStackTrace();
                }
            
                    //creating the connection
                    try {
                        Connection con = DriverManager.getConnection("jdbc:mysql://localhost/admin", "root", "Upsrajan@251");
                        // Creating the statements
                        PreparedStatement ps = con.prepareStatement("insert into datainput (Name, Email, Gender, Branch, BirthDate, Contacts) VALUES (?, ?, ?, ?, ?, ?)");
                    
                        // Set values using the actual data from the components
                        ps.setString(1, namTextField.getText());
                        ps.setString(2, EmailTextField.getText());
                        ps.setString(3, GenderChoicebox.getValue());
                        ps.setString(4, Streamchoicebox.getValue());
                        ps.setDate(5, Date.valueOf(DobdatePicker.getValue())); // Assuming DobdatePicker is a DatePicker
                        ps.setString(6, ContactTextField.getText());
                    
                        int rs = ps.executeUpdate();
                    
                        if (rs > 0) {
                            textArea.appendText("Successful");
                        } else {
                            textArea.appendText("Unsuccessful");
                        }
                    
                        // Closing the connection
                        con.close();
                    
                    } catch (SQLException e) {
                        // TODO Auto-generated catch block
                        e.printStackTrace();
                    }
                    
            }
            
        });
        
        
        
        //setting the delete button on action
        deleterec.setOnAction(new EventHandler<ActionEvent>() {
            
            @Override
            public void handle(ActionEvent arg0) {
                textArea.clear();
            }
            
        });;
        
        
        flowPane.getChildren().addAll(gridnew,textArea);
        
        Scene scenenew = new Scene(flowPane, 1100,600);
        newStage.setScene(scenenew);
        
        
        //setting title to the new scene
        newStage.setTitle("Data Input");
        newStage.setResizable(false);
        
        
        //adding the icon to the application
        try {
            newStage.getIcons().add(new Image("D:\\PROGRAMING_CODES\\java\\GUIInjava\\JavaFx\\Loginpage\\logo.png"));
        } catch (Exception e) {
            // TODO: handle exception
        }
        
        newStage.show();
        
      
    }
    
    //main method
    public static void main(String[] args) {
        launch(args);

        
    }

}
