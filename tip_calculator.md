# Pseudocode for Tip Calculator
```
START
  DISPLAY "Enter bill amount: "
  READ billAmount

  WHILE billAmount <= 0 DO
    DISPLAY "Error: Bill amount must be a positive number."
    DISPLAY "Enter bill amount: "
    READ billAmount
  END WHILE

  DISPLAY "Enter service quality (poor, fair, good, excellent): "
  READ serviceQuality

  WHILE serviceQuality NOT IN ["poor", "fair", "good", "excellent"] DO
    DISPLAY "Error: Invalid service quality. Choose from (poor, fair, good, excellent)."
    DISPLAY "Enter service quality: "
    READ serviceQuality
  END WHILE

  DISPLAY "Enter number of people splitting the bill: "
  READ numPeople

  WHILE numPeople <= 0 OR numPeople IS NOT INTEGER DO
    DISPLAY "Error: Number of people must be a positive integer."
    DISPLAY "Enter number of people: "
    READ numPeople
  END WHILE

  DECLARE tipPercentage AS FLOAT
  IF serviceQuality = "poor" THEN
    tipPercentage = 0.10
  ELSE IF serviceQuality = "fair" THEN
    tipPercentage = 0.15
  ELSE IF serviceQuality = "good" THEN
    tipPercentage = 0.18
  ELSE IF serviceQuality = "excellent" THEN
    tipPercentage = 0.20
  END IF

  tipAmount = billAmount × tipPercentage
  totalAmount = billAmount + tipAmount
  amountPerPerson = totalAmount ÷ numPeople

  DISPLAY "Bill amount: $" + billAmount
  DISPLAY "Service quality: " + serviceQuality + " (" + (tipPercentage * 100) + "%)"
  DISPLAY "Tip amount: $" + tipAmount
  DISPLAY "Total amount: $" + totalAmount
  DISPLAY "Number of people: " + numPeople
  DISPLAY "Amount per person: $" + amountPerPerson
END
```

