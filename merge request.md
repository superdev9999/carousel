1. template
## Ticket
https://sdesk.drfirst.com/browse/RC4-26627

## Description
1. When you input the numbers, the input box `only validates the number of decimals` and `doesn't remove the trailing zero`.
2. Only when you `leave` the input box, the input box `automatically removes` the trailing zero.
Then, when you type 1.07, the input box displays 1.0, and when you leave the input box, it displays 1.

## Motivation and context
We should satisfy the 2 major things,
1) `fixing the patient safety issue` - When inputting `1.07`, it should not be `17`
2) `removing the trailing zero` - It should happen only when the user leaves the input box

## Acceptance criteria:
- Kg - entry to hundredths, e.g. 23.45
1) Allow entry up to 2 decimal places, any number
2) Allow trailing 0's, e.g. 23.00, to display while field is in focus
3) Truncate trailing 0's after the field focus is changed, e.g. 23.00 becomes 23 after the cursor is moved outside the control
4) Only one decimal point should be allowed, e.g. 23.0.0 should not be allowed
- Wt - entry to tenths, e.g. 23.4
1) Allow entry up to 1 decimal places, any number
2) Allow trailing 0's, e.g. 23.0, to display while field is in focus
3) Truncate trailing 0's after the field focus is changed, e.g. 23.0 becomes 23 after the cursor is moved outside the control
- Weights from 0.01 (kg) to 999.99 (kg) OR 0.1 (lb) to 999.9 (lb) allowed.

## Testing requirements
- [ ] In addition to code review please test this work in local development
- [ ] Please check if our unit tests cover all edge cases

## Test script:
1. Test the Weight(Lb) input box on the Prescribe Medication panel (EDS)
2. Test the Weight(Lb) input box on the Pharmacy Messages panel

## Screenshots
![RC4-26627](/uploads/94eb6f213b4f272e95dac3eefa9e204f/RC4-26627.gif)
![RC4-26627-1](/uploads/200ca412ae0d3f64502b2a85a03add16/RC4-26627-1.gif)


2. example
<!--- Provide a general summary of your changes in the Title above -->

## Ticket
<!-- Link to jira ticket -->

## Description
<!--- Describe your changes in detail -->

## Motivation and context
<!--- Why is this change required? What problem does it solve? -->
<!--- If it fixes an open issue, please link to the issue here. -->

## Acceptance criteria:
<!--- Go over all the following points, and put an `x` in all the boxes that apply. -->
<!--- If you're unsure about any of these, don't hesitate to ask. We're here to help! -->
- [ ] Some criteria.
- [ ] Another rad piece of criteria.

## Testing requirements
- [x] In addition to code review please test this work in local development 

## Test script:
1. Step Z
2. Step Y
3. Step X

## Screenshots
![Screenshot](https://via.placeholder.com/600x300.png?text=Screenshot)
