<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>GroupBox Example</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      padding: 40px;
    }
    fieldset {
      border: 2px solid #333;
      border-radius: 8px;
      padding: 20px;
      max-width: 400px;
      margin-bottom: 20px;
    }
    legend {
      font-weight: bold;
      padding: 0 10px;
    }
    label {
      display: block;
      margin-top: 10px;
    }
    input[type="text"], input[type="email"] {
      width: 100%;
      padding: 8px;
      margin-top: 4px;
      box-sizing: border-box;
    }
    button {
      margin-top: 15px;
      padding: 8px 16px;
      font-size: 14px;
    }
  </style>
</head>
<body>

  <h2>Website Form with GroupBox</h2>

  <form>
    <fieldset>
      <legend>Personal Details</legend>

      <label for="name">Name:</label>
      <input type="text" id="name" name="name">

      <label for="email">Email:</label>
      <input type="email" id="email" name="email">
    </fieldset>

    <fieldset>
      <legend>Address</legend>

      <label for="address">Street Address:</label>
      <input type="text" id="address" name="address">

      <label for="city">City:</label>
      <input type="text" id="city" name="city">
    </fieldset>

    <button type="submit">Submit</button>
  </form>

</body>
</html>
