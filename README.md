function add(a, b) {
    return a + b;
}

function subtract(a, b) {
    return a - b;
}

function multiply(a, b) {
    return a * b;
}

function divide(a, b) {
    if (b === 0) {
        throw new Error("Division by zero");
    }
    return a / b;
}

function main() {
    const num1 = parseInt(prompt("Enter the first integer: "));
    const num2 = parseInt(prompt("Enter the second integer: "));
    const operation = prompt("Enter operation (+, -, *, /): ");

    try {
        let result;
        switch (operation) {
            case '+':
                result = add(num1, num2);
                break;
            case '-':
                result = subtract(num1, num2);
                break;
            case '*':
                result = multiply(num1, num2);
                break;
            case '/':
                result = divide(num1, num2);
                break;
            default:
                alert("Invalid operation");
                return;
        }
        alert("Result: " + result);
    } catch (error) {
        alert("Error: " + error.message);
    }
}

main();
