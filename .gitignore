import javafx.application.*;
import javafx.event.*;
import javafx.geometry.*;
import javafx.scene.*;
import javafx.scene.control.*;
import javafx.scene.layout.*;
import javafx.scene.paint.*;
import javafx.scene.text.*;
import javafx.stage.*;
import javafx.scene.shape.*;
import javafx.scene.input.*;

public class DrawShape extends Application {

	private CheckBox fillColor;
	private RadioButton thinBorder, thickBorder, red, yellow, blue;
	private Button clearButton;

	public void start(Stage primaryStage) {
		beginDrawn = false;

		fillColor = new CheckBox("Fill");
		thinBorder = new RadioButton("Thin Border");
		thickBorder = new RadioButton("Thick Border");
		thickBorder.setSelected(true);
		ToggleGroup group = new ToggleGroup();
		thinBorder.setToggleGroup(group);
		thickBorder.setToggleGroup(group);

		red = new RadioButton("Red");
		red.setStyle("-fx-text-fill: red");
		blue = new RadioButton("Blue");
		blue.setStyle("-fx-text-fill: blue");
		yellow = new RadioButton("Yellow");
		yellow.setStyle("-fx-text-fill: #CCCC00");
		blue.setSelected(true);
		ToggleGroup group2 = new ToggleGroup();
		red.setToggleGroup(group2);
		blue.setToggleGroup(group2);
		yellow.setToggleGroup(group2);

		HBox optionVBox = new HBox(thinBorder, thickBorder, fillColor);
		optionVBox.setAlignment(Pos.CENTER);
		optionVBox.setSpacing(10);
		
		HBox colorBox = new HBox(red, blue, yellow);
		colorBox.setAlignment(Pos.TOP_CENTER);
		colorBox.setSpacing(10);
		
		clearButton = new Button("Clear..");
		HBox buttonBox = new HBox(clearButton);
		buttonBox.setAlignment(Pos.BOTTOM_CENTER);
		buttonBox.setSpacing(10);

		VBox drawControl = new VBox(colorBox, optionVBox, buttonBox);
		drawControl.setSpacing(10);

		Rectangle border = new Rectangle(490, 500, Color.TRANSPARENT);
		border.setStroke(Color.BLACK);
		
		pane = new Pane();
		pane.setOnMouseClicked(this::handleMouseClicks);
		pane.setOnMouseMoved(this::handleMouseMotion);
		
		BorderPane borderPane = new BorderPane();
		borderPane.setCenter(border);
		borderPane.setCenter(pane);
		borderPane.setBottom(drawControl);

		Scene scene = new Scene(borderPane, 500, 600);
		primaryStage.setScene(scene);
		primaryStage.setTitle("Draw Rectangle");
		primaryStage.setResizable(false);
		primaryStage.show();
	}

	public static void main(String[] args) {
		launch(args);
	}
}
