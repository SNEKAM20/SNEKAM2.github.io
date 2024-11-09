function calculate(num1, num2, operation) {
    switch (operation) {
        case '+':
            return num1 + num2;
        case '-':
            return num1 - num2;
        case '*':
            return num1 * num2;
        case '/':
            if (num2 === 0) {
                throw new Error("Cannot divide by zero");
            }
            return num1 / num2;
        default:
            throw new Error("Invalid operation");
    }
}

function main() {
    const num1 = parseFloat(prompt("Enter the first number:"));
    const num2 = parseFloat(prompt("Enter the second number:"));
    const operation = prompt("Enter operation (+, -, *, /):");

    try {
        const result = calculate(num1, num2, operation);
        alert("Result: " + result);
    } catch (error) {
        alert("Error: " + error.message);
    }
}

main();
