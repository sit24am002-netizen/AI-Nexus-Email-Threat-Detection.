# AI Nexus – Test Cases and Sample Data

## 1. Overview

This document describes the test cases used to evaluate the AI Nexus Email Threat Detection system. The system analyzes email content and classifies it as Safe, Suspicious, or High Risk.

## 2. Test Cases

| Test ID | Test Scenario | Sample Email Content | Expected Result |
|---|---|---|---|
| TC01 | Normal email | Hi, please find the meeting agenda attached. | Safe |
| TC02 | Suspicious link | Your account needs verification. Click this unfamiliar link immediately. | Suspicious |
| TC03 | Urgent payment request | Transfer the payment immediately to avoid account suspension. | High Risk |
| TC04 | Prize scam | Congratulations! You have won a prize. Pay a fee to claim it. | High Risk |
| TC05 | Password request | Please send your password to confirm your account. | High Risk |
| TC06 | Routine notification | Your library book is due tomorrow. Please return it on time. | Safe |
| TC07 | Unexpected attachment | Open this unexpected attachment to claim your reward. | Suspicious |
| TC08 | Generic promotional email | Check out our latest offers and discounts. | Safe |

## 3. Sample Data

The following sample emails are synthetic examples created for testing. They do not contain real user information or actual malicious links.

| Sample ID | Email Text | Label |
|---|---|---|
| SD01 | The project meeting is scheduled for Monday at 10 AM. | Safe |
| SD02 | Verify your account immediately using this unfamiliar link. | Suspicious |
| SD03 | Send your password now to prevent account closure. | High Risk |
| SD04 | Your order has been shipped and will arrive tomorrow. | Safe |
| SD05 | Claim your unexpected cash prize by paying a processing fee. | High Risk |

## 4. Evaluation Metrics

- **Accuracy:** Percentage of emails classified correctly.
- **Precision:** Percentage of emails predicted as a particular threat category that are actually in that category.
- **Recall:** Percentage of emails belonging to a threat category that the system correctly identifies.
- **F1-score:** Harmonic mean of precision and recall.

## 5. Expected Outcome

The system should correctly classify legitimate emails and flag suspicious or high-risk emails. Actual performance must be measured using a labeled test dataset. These examples alone do not establish model accuracy.

## 6. Limitations

- Simple keyword-based examples may not represent sophisticated phishing attacks.
- Real email datasets may contain new and previously unseen threats.
- Model predictions should be treated as risk indicators, not guarantees of safety.
- Test emails should be evaluated without opening suspicious links or attachments.
