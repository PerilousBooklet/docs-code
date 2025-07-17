# Swing

## Init

TODO: see main() method in Kanban

## Scaled Image

Create a scaled Image (example taken from Codex Naturalis demo):

```java
public Image image = Toolkit.getDefaultToolkit().getImage(new File("/home/raffaele/downloads/codex-naturalis/codex/image.png").getAbsolutePath());
public Image scaledImage = image.getScaledInstance(80, 53, Image.SCALE_SMOOTH);
```

Then draw it onto a JPanel with a Graphics object's `drawImage()`.

## Yes/No Confirmation Menu

```java
Object[] options = { "Yes", "No" };
int n = JOptionPane.showOptionDialog(column, "Delete this Item?", "Warning", JOptionPane.DEFAULT_OPTION, JOptionPane.WARNING_MESSAGE, null, options, options[0]);
// Confirm deletion
if (n == 0) {
  write some code here
}
```

## Text Modification Menu

source: `s`

```java
// Unsupported Characters Check
public static boolean isValidInput(String input) {
	// TODO: check for excessive word length
  return input.matches("[a-zA-Z0-9:,.\"\'?! ]+");
}
```

```java
// Get ColumnTitleLabel text
String currentText = columnTitleLabel.getText();
String input = (String)JOptionPane.showInputDialog(column, "New text here...", currentText);
// input must be not-null and valid
if (input != null && Item.isValidInput(input)) {
  // Modify the text
  columnTitleLabel.setText(input);
  columnTitleLabel.revalidate();
  columnTitleLabel.repaint();
} else {
  logger.warning("Invalid input provided!");
}
```

## JOptionPane

https://docs.oracle.com/javase/8/docs/api/javax/swing/JOptionPane.html
