<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Gift Card Purchase Form</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      padding: 20px;
    }
    table, th, td {
      border: 1px solid #000;
      border-collapse: collapse;
      padding: 8px;
    }
    th {
      background-color: #f2f2f2;
    }
  </style>
  <script>
    function showHelp() {
      alert("Fill in your details, choose your gift card type and amount, then click Submit to complete your purchase.");
    }
  </script>
</head>
<body>

  <h2>Gift Card Purchase Form</h2>

    <ol>
    <li>Fill in your personal details.</li>
    <li>Select gift card type and amount.</li>
    <li>Choose payment and delivery options.</li>
    <li>Submit the form to complete your purchase.</li>
  </ol>

  
  <ul>
    <li>Ensure your email is correct to receive the digital gift card.</li>
    <li>All fields marked with * are required.</li>
    <li>Accepted payment modes: Credit Card, Debit Card, UPI.</li>
  </ul>

  
  <h3>Terms Used</h3>
  <dl>
    <dt>eGift</dt>
    <dd>Digital gift card delivered via email.</dd>
    <dt>Physical Card</dt>
    <dd>Gift card shipped to your address.</dd>
    <dt>Card Value</dt>
    <dd>The total amount loaded on the card.</dd>
  </dl>

 
  <h3>Card Fees</h3>
  <table>
    <tr>
      <th rowspan="2">Card Type</th>
      <th colspan="2">Fee Structure</th>
    </tr>
    <tr>
      <th>Activation Fee</th>
      <th>Delivery Fee</th>
    </tr>
    <tr>
      <td>eGift Card</td>
      <td>$0</td>
      <td>$0</td>
    </tr>
    <tr>
      <td>Physical Card</td>
      <td>$2</td>
      <td>$5</td>
    </tr>
  </table>

  
  <form action="submit_form.html" method="post">

    <p>
      <label for="name">Full Name *:</label><br>
      <input type="text" id="name" name="name" required>
    </p>

    <p>
      <label for="email">Email *:</label><br>
      <input type="email" id="email" name="email" required>
    </p>

    <p>
      <label for="password">Password *:</label><br>
      <input type="password" id="password" name="password" required>
    </p>

    <p>
      <label for="phone">Phone Number:</label><br>
      <input type="tel" id="phone" name="phone">
    </p>

    <p>
      <label for="dob">Date of Birth:</label><br>
      <input type="date" id="dob" name="dob">
    </p>

    <p>
      <label>Choose Card Type *:</label><br>
      <input type="radio" id="egift" name="card_type" value="eGift" required>
      <label for="egift">eGift</label>
      <input type="radio" id="physical" name="card_type" value="Physical">
      <label for="physical">Physical</label>
    </p>

    <p>
      <label>Select Card Value *:</label><br>
      <select name="value" required>
        <option value="">--Select Value--</option>
        <option value="25">$25</option>
        <option value="50">$50</option>
        <option value="100">$100</option>
        <option value="custom">Custom</option>
      </select>
    </p>

    <p>
      <label>Extras:</label><br>
      <input type="checkbox" id="gift_wrap" name="extras" value="Gift Wrap">
      <label for="gift_wrap">Gift Wrap</label>
      <input type="checkbox" id="personal_note" name="extras" value="Personal Note">
      <label for="personal_note">Include Personal Note</label>
    </p>

    <p>
      <label for="address">Delivery Address:</label><br>
      <textarea id="address" name="address" rows="4" cols="50"></textarea>
    </p>

    <p>
      <label for="rating">Satisfaction with Previous Purchase (0 to 10):</label><br>
      <input type="range" id="rating" name="rating" min="0" max="10">
    </p>

    <p>
      <label for="file">Upload ID Proof (PDF/JPG):</label><br>
      <input type="file" id="file" name="file">
    </p>

    
    <p>
      <button type="submit">Submit</button>
      <button type="reset">Reset</button>
      <button type="button" onclick="showHelp()">Help</button>
    </p>

  </form>

</body>
</html>
