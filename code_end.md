```python
print("\n" + "="*50)
print("TESTING WITH SAMPLE MESSAGES")
print("="*50)

test_messages = [
    "Congratulations! You've won a $1000 gift card. Click here to claim now!",
    "Hey, are we still meeting for lunch tomorrow?",
    "URGENT: Your account has been compromised. Verify your details immediately!",
    "Can you send me the project report by EOD?"
]

for msg in test_messages:
    label, conf = predict_message(msg)
    print(f"\nMessage: {msg[:60]}...")
    print(f"Prediction: {label} (Confidence: {conf:.2f}%)")

print("\n" + "="*50)
print("Model training complete!")
print("="*50)
```