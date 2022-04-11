# Module-Challenge-15: Robo Advisor *PLEASE SEE NOTE*
## NOTE: Due to time constraints with project 2 and not having the proper configuration, I will only be submitting the lambda function for some partial credit. I intend for this module to be the one dropped at the end of the course, as the lowest grade I have otherwise is a 90. I hope this is understandable.

## Lambda Function
### Even though I do not have the proper configuration to do the whole assignment, I did complete the lambda function based on the requirements.

### In terms of new code, we end up with three new functions: validate_data, get_recommendation, recommend_portfolio.

### In the validate_data function, this is where the two main inputs of age between 0 and 65 and the amount being over 5000. With function parameters of age, dollars, and intent_request, if statements were created to parse for integers and create a statement if either input is invalid.The output variables are then return to the provided build_validation_result function.

### For the get_recommendation function, this is where after using the riskLevel variable we use a series of if and elif statements to assign portfolio recommendation breakdowns based on the prompt in the assignment. The code then will return the recommendation variable as shown within the function:

### recommendation = ""
###    if riskLevel == "none" :
###        recommendation = "100% bonds (AGG), 0% equities (SPY)"
###    elif riskLevel == "low":
###        recommendation = "60% bonds (AGG), 40% equities (SPY)"
###    elif riskLevel == "medium" :
###        recommendation = "40% bonds (AGG), 60% equities (SPY)"
###    elif riskLevel == "high":
###        recommendation = "20% bonds (AGG), 80% equities (SPY)"
###    else:
###        recommendation = "Choose between the following: none, low, medium, high"
###    return recommendation


### For the recommend_portfolio function with intent_request as the input variable, the info for first_name, age, investment_amount, risk_level, and source. Now within a big if statement, we first see is the data for the user is valid. After the nest statement, we get the current session attributes with intent_request["sessionAttributes"] assigned to a variable. At the end of the outside if statemnt, we return the delegate function with parameters output_session_attributes and get_slot(intent_request). On the outside of the big if statement, recommendation is updated with get_recommendation(riskLevel). 
