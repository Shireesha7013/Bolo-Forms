# Bolo-Form
<!DOCTYPE html>
<html>
<head>
</head>
<body>
    <div class="container">
        <h1>Bolo Forms</h1>
    </div>
  <div id="form-builder">
    <div class="question">
      <label for="text-input">Text Input:</label>
      <input type="text" id="text-input" name="text-input">
    </div>
    
    <div class="question">
      <label for="checkbox-input">Checkbox Input:</label>
      <input type="checkbox" id="checkbox-input" name="checkbox-input">
    </div>
    
    <div class="question">
      <label for="radio-input">Radio Input:</label>
      <input type="radio" id="radio-input" name="radio-input" value="option1">
      <label for="radio-input">Option 1</label>
      <input type="radio" id="radio-input" name="radio-input" value="option2">
      <label for="radio-input">Option 2</label>
    </div>
  </div>
var form = document.getElementById("form-builder");

  // Add an event listener to the form submission
  form.addEventListener("submit", function(event) {
    // Prevent the default form submission behavior
    event.preventDefault();

    // Get the values of the form inputs
    var textInputValue = document.getElementById("text-input").value;
    var checkboxInputValue = document.getElementById("checkbox-input").checked;
    var radioInputValue = document.querySelector('input[name="radio-input"]:checked').value;

    // Log the values to the console (you can replace this with your custom functionality)
    console.log("Text Input Value: " + textInputValue);
    console.log("Checkbox Input Value: " + checkboxInputValue);
    console.log("Radio Input Value: " + radioInputValue);

    // Reset the form
    form.reset();
  });
