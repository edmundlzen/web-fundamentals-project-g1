const express = require("express");
const app = express();
app.use(express.json());

// POST /api/enroll  — enroll user in course
app.post("/api/enroll", (req, res) => {
  const { courseId, method } = req.body;

  console.log("Enrolling in course:", courseId);

  // If paid, redirect to payment
  if (method !== "free") {
    return res.json({ success: true, message: "Proceed to payment." });
  }

  return res.json({ success: true, message: "Enrollment complete." });
});

// POST /api/payment — process payment
app.post("/api/payment", (req, res) => {
  const { amount, method } = req.body;

  console.log("Processing payment:", amount, method);

  return res.json({ success: true, message: "Payment successful." });
});

// POST /api/email/confirmation — send confirmation email
app.post("/api/email/confirmation", (req, res) => {
  const { email, courseId } = req.body;

  console.log(Sending confirmation email to ${email} for course ${courseId});

  return res.json({ success: true, message: "Email sent." });
});

app.listen(3000, () => console.log("Server running on port 3000"));
   
