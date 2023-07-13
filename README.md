# calculation
function createCalculation(num1, num2, operator) {
    /**
     * This function creates a calculation based on the given numbers and operator.
     * 
     * @param {number} num1 - The first number.
     * @param {number} num2 - The second number.
     * @param {string} operator - The operator to be used in the calculation.
     * @returns {number} The result of the calculation.
     */
    
    try {
        // Check if both arguments are numbers
        if (typeof num1 !== 'number' || typeof num2 !== 'number') {
            throw new TypeError('Both arguments must be numbers');
        }
        
        // Perform the calculation based on the operator
        let result;
        switch (operator) {
            case '+':
                result = num1 + num2;
                break;
            case '-':
                result = num1 - num2;
                break;
            case '*':
                result = num1 * num2;
                break;
            case '/':
                result = num1 / num2;
                break;
            default:
                throw new Error('Invalid operator');
        }
        
        return result;
    } catch (error) {
        // Log the error
        console.error('Error:', error.message);
        return null;
    }
}
