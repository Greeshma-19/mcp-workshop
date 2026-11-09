# MCP Workshop Assignment — Answers

**Student:** Greeshma Mandala  
**Assignment:** Build and Call Your Own MCP Tool

### Question 1: How many tools did the server list in Part 1 and Part 3? What did you change in the client?

In Part 1, the server listed 8 tools. After I added my `predict_both` function, it listed 9 tools in Part 3. I did not need to manually register the new tool in the client. The client discovered it automatically when it connected to the MCP server.

### Question 2: On how many test patients did the models disagree? Which model was correct?

I tested all 114 patients, and the models disagreed on 8 patients.

| Patient | True Diagnosis | Correct Model |
|---|---|---|
| 3 | Benign | Logistic Regression |
| 25 | Benign | Logistic Regression |
| 48 | Benign | Logistic Regression |
| 53 | Malignant | KNN |
| 76 | Malignant | Logistic Regression |
| 80 | Benign | Logistic Regression |
| 99 | Benign | Logistic Regression |
| 102 | Malignant | Logistic Regression |

### Question 3: Which model was correct more often when they disagreed?

Logistic Regression performed better in the disagreement cases. It correctly predicted 7 out of 8 patients, while KNN correctly predicted only 1. Based on these results, Logistic Regression was more reliable when the two models gave different answers.

### Question 4: Why does the description in triple quotes matter?

The description helps an AI application understand what the tool does. When an AI connects to the MCP server, it can read the tool's name and description to decide when to use it. A clear description makes it easier for the AI to choose the correct tool and understand its purpose.

### Question 5: Why is logging every tool call useful?

Logging helps us keep track of what happens when a tool is used. It records information such as the request ID, tool name, and execution status. This is useful because we can check whether a tool worked correctly, find errors, and review previous requests. It also makes the system more transparent and easier to troubleshoot.

### Conclusion

Through this assignment, I learned how to add a new tool to an MCP server and call it using a Python client. I also learned how MCP automatically discovers tools and how audit logs help track their execution. Comparing Logistic Regression and KNN helped me understand that different machine learning models can produce different predictions for the same patient.
