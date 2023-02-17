const display = document.querySelector("#display");
const buttons = document.querySelectorAll("button");

buttons.forEach(button => {
  button.addEventListener("click", () => {
    if (button.id === "clear") {
      display.textContent = "";
    } else if (button.id === "equals") {
      display.textContent = eval(display.textContent);
    } else {
      display.textContent += button.textContent;
    }
  });
});