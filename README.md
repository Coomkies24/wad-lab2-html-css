# wad-lab2-html-css
<img width="1599" height="899" alt="Screenshot 2025-09-06 145022" src="https://github.com/user-attachments/assets/7e42e153-b7a1-4d62-ba7c-1753de587a0c" />
[hands-on activity 2.html](https://github.com/user-attachments/files/22185093/hands-on.activity.2.html)
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <title>Student Registration</title>[style.css](https://github.com/user-attachments/files/22185094/style.css)

    <link rel="stylesheet" href="style.css">
  </head>
  <body>
    <h1>Student Registration Portal</h1>
    <p class="desc">
      Review the available courses in the table below, then complete the
      registration form.
    </p>

    <div class="container">
      <!-- LEFT SIDE -->
      <div>
        <h2>Available Courses</h2>
        <table>
          <caption>
            Computer Science Department Courses - A.Y. 2026
          </caption>
          <tr>
            <th rowspan="2">Course Code</th>
            <th rowspan="2">Course Name</th>
            <th colspan="2">Schedule</th>
          </tr>
          <tr>
            <th>Day</th>
            <th>Time</th>
          </tr>
          <tr>
            <td>CS101</td>
            <td>Introduction to Programming</td>
            <td>Mon & Wed</td>
            <td>9:00-10:00 AM</td>
          </tr>
          <tr>
            <td>CS102</td>
            <td>Web Development Basics</td>
            <td>Tue & Thu</td>
            <td>1:00-2:00 PM</td>
          </tr>
          <tr>
            <td>CS103</td>
            <td>Database Systems</td>
            <td rowspan="2">Fri</td>
            <td>10:00-12:00 NN</td>
          </tr>
          <tr>
            <td>CS104</td>
            <td>Computer Networks</td>
            <td>1:00-3:00 PM</td>
          </tr>
        </table>
      </div>

      <!-- RIGHT SIDE -->
      <div id="registration-form">
        <h2>Registration Form</h2>
        <form action="./submitted.html" method="post">
          <label for="name">Full Name:</label>
          <input
            id="name"
            name="name"
            type="text"
            placeholder="Lname, Fname, M.I."
            required
          />

          <label for="email">Email Address:</label>
          <input
            type="email"
            id="email"
            name="email"
            placeholder="email@example.com"
            required
          />

          <p>Year Level:</p>
          <input
            type="radio"
            name="year"
            id="first"
            value="1st Year"
            required
          />
          <label for="first">1st Year</label>
          <br />
          <input type="radio" name="year" id="second" value="2nd Year" />
          <label for="second">2nd Year</label>
          <br />
          <input type="radio" name="year" id="third" value="3rd Year" />
          <label for="third">3rd Year</label>
          <br />
          <input type="radio" name="year" id="fourth" value="4th Year" />
          <label for="fourth">4th Year</label>
          <br />

          <p>Preferred Study Mode: (Optional)</p>
          <input type="checkbox" id="online" name="mode" value="Online" />
          <label for="online">Online</label>
          <br />
          <input type="checkbox" id="onsite" name="mode" value="Onsite" />
          <label for="onsite">Onsite</label>
          <br />

          <label for="course">Select Course:</label>
          <select name="course" id="course" required>
            <option value="">--Choose a Course--</option>
            <option value="CS101">CS101 - Introduction to Programming</option>
            <option value="CS102">CS102 - Web Development Basics</option>
            <option value="CS103">CS103 - Database Systems</option>
            <option value="CS104">CS104 - Computer Networks</option>
          </select>

          <label for="comments">Additional Note:</label>
          <textarea
            name="comments"
            id="comments"
            rows="4"
            placeholder="Enter any additional requests or notes..."
            required
          ></textarea>

          <button type="submit">Register</button>
          <button type="reset">Clear Form</button>
        </form>
      </div>
    </div>
  </body>
</html>
/* Universal */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Segoe UI', Tahoma, sans-serif;
    line-height: 1.6;
    background: linear-gradient(to right, #20252C, #A32633);
    padding: 0;
    display: flex;
    flex-direction: column;
    gap: 40px;
    max-width: 1100px;
    margin: auto;
    color: #F2F2F2;
}

h1 {
    text-align: center;
    color: #20252C;
    margin-bottom: 10px;
    text-shadow: 2px 2px 6px #4e4e4e, 0 0 25px #535353;
}

.desc {
    text-align: center;
    color: #F2F2F2;
}

.container {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 30px;
}

table caption {
    font-weight: bold;
    margin-bottom: 10px;
    color: #F2F2F2;
}

table {
    border-collapse: collapse;
    width: 100%;
    background-color: #20252C;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.8);
}

th, td {
    border: 1px solid #A32633;
    padding: 12px;
    text-align: center;
}

th {
    background-color: #A32633;
    color: #20252C;
}

td {
    background-color: #343339;
    color: #F2F2F2;
}

tr:nth-child(even) {
    background-color: #20252C;
}

#registration-form {
    background-color: #343339;
    padding: 20px;
    border: 2px solid #A32633;
    border-radius: 8px;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.8);
    color: #F2F2F2;
}

#registration-form h2 {
    color: #A32633;
    margin-bottom: 10px;
    text-shadow: 2px 2px 6px #A32633;
}

.form-group {
    display: block;
    margin-bottom: 10px;
}

.form-group label {
    font-weight: bold;
    margin-top: 4px;
    color: #F2F2F2;
}

input, select, textarea {
    margin-top: 4px;
    padding: 10px;
    width: 100%;
    border: 1px solid #343339;
    border-radius: 4px;
}

input[type="radio"],
input[type="checkbox"] {
    width: auto;
    margin-right: 3px;
}

input[required] {
    border-left: 4px solid #A32633;
}

input:focus, select:focus, textarea:focus {
    outline: none;
    border: 1px solid #A32633;
    box-shadow: 0 0 10px rgba(162, 38, 51, 0.7);
}

button {
    padding: 10px 14px;
    margin-top: 14px;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    color: beige;
    background-color: #A32633;
    box-shadow: 0 0 10px #A32633;
}

button[type="submit"]:hover {
    background-color: #962333;
    box-shadow: 0 0 15px 3px #A32633;
}

button[type="reset"] {
    background-color: #343339;
}

button[type="reset"]:hover {
    background-color: #9b9b9b;
}

input:focus {
    box-shadow: 0 0 5px 2px #A32633;
}

input:focus, select:focus, textarea:focus {
    outline: none;
    border: 1px solid #A32633;
    box-shadow: 0 0 8px #A32633;
}

@media (max-width: 768px) {
    .container {
        grid-template-columns: 1fr;
    }

    table {
        font-size: 14px;
    }

    #registration-form {
        padding: 15px;
    }

    button {
        width: 100%;
    }

    h1 {
        font-size: 24px;
    }

    .form-group label {
        font-size: 14px;
    }

    input, select, textarea {
        padding: 8px;
    }
}

@media (max-width: 480px) {
    h1 {
        font-size: 20px;
    }

    .desc {
        font-size: 14px;
    }

    table {
        font-size: 12px;
    }

    button {
        font-size: 14px;
    }

    #registration-form {
        padding: 10px;
    }

    .form-group label {
        font-size: 12px;
    }

    input, select, textarea {
        font-size: 14px;
    }
}

