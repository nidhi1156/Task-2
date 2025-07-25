// Form validation
document.getElementById("contactForm").addEventListener("submit", function(event) {
  event.preventDefault();
  const name = document.getElementById("name").value.trim();
  const email = document.getElementById("email").value.trim();

  if (name === "" || email === "") {
    alert("Please fill in all fields.");
  } else if (!email.includes("@")) {
    alert("Please enter a valid email address.");
  } else {
    alert("Form submitted successfully!");
  }
});

// To-Do list functionality
function addTask() {
  const taskInput = document.getElementById("taskInput");
  const taskText = taskInput.value.trim();

  if (taskText === "") {
    alert("Please enter a task.");
    return;
  }

  const li = document.createElement("li");
  li.textContent = taskText;

  // Remove task on click
  li.onclick = () => li.remove();

  document.getElementById("taskList").appendChild(li);
  taskInput.value = "";
}
