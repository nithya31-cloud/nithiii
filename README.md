<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Student Dashboard - SRM</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            margin: 0;
            padding: 0;
            background: url('data:image/png;base64,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') no-repeat center top fixed;
            background-size: cover;
        }

        .container,
        .dashboard {
            max-width: 700px;
            margin: 80px auto;
            background: rgba(255, 255, 255, 0.95);
            padding: 30px;
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
            border-radius: 10px;
            display: none;
        }

        .visible {
            display: block;
        }

        h1,
        h2,
        h3 {
            text-align: center;
            color: #003366;
        }

        .welcome {
            text-align: center;
            margin-bottom: 20px;
        }

        .college-link {
            text-align: center;
            margin-top: 10px;
        }

        .college-link a {
            color: #007BFF;
            text-decoration: none;
            font-weight: bold;
        }

        form {
            display: flex;
            flex-direction: column;
        }

        label {
            margin-top: 10px;
            font-weight: bold;
        }

        input {
            padding: 10px;
            margin-top: 4px;
            border-radius: 5px;
            border: 1px solid #ccc;
        }

        button {
            margin-top: 20px;
            padding: 12px;
            background: #0056b3;
            color: white;
            border: none;
            border-radius: 6px;
            cursor: pointer;
            font-weight: bold;
        }

        button:hover {
            background: #003f7f;
        }

        .error {
            color: red;
            text-align: center;
            margin-top: 10px;
        }

        table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 10px;
        }

        th,
        td {
            border: 1px solid #ccc;
            text-align: center;
            padding: 10px;
        }

        th {
            background: #e0f0ff;
            color: #003366;
        }

        td {
            color: #555;
        }

        .profile-pic {
            width: 100px;
            height: 100px;
            border-radius: 50%;
            background-image: url('https://www.w3schools.com/howto/img_avatar2.png');
            background-size: cover;
            background-position: center;
            margin: 0 auto 20px auto;
        }

        .back-button {
            background-color: #f0f0f0;
            border: none;
            color: #003366;
            font-size: 16px;
            padding: 10px;
            cursor: pointer;
            width: 100%;
            margin-top: 20px;
        }

        .back-button:hover {
            background-color: #ddd;
        }
    </style>
</head>

<body>
    <div class="container visible" id="loginSection">
        <div class="welcome">
            <h1>Welcome to SRM Institution</h1>
            <p>"Empowering minds, shaping the future."</p>
        </div>
        <div class="college-link">
            <a href="https://www.srmist.edu.in" target="_blank">Visit SRM College Website</a>
        </div>
        <h2>Student Login</h2>
        <form id="loginForm">
            <label>Username</label>
            <input type="text" id="username" required>
            <label>Password</label>
            <input type="password" id="password" required>
            <button type="submit">Login</button>
        </form>
        <p id="error" class="error"></p>
    </div>

    <div class="dashboard" id="dashboardSection">

        <div class="profile-pic"></div>
        <h2>Welcome, <span id="studentName"></span></h2>

        <h3>Student Details</h3>
        <table>
            <tbody>
                <tr>
                    <td>Name:</td>
                    <td id="studentFullName"></td>
                </tr>
                <tr>
                    <td>Reg. No:</td>
                    <td id="studentRegNo"></td>
                </tr>
                <tr>
                    <td>Email:</td>
                    <td id="studentEmail"></td>
                </tr>
                <tr>
                    <td>Department:</td>
                    <td id="studentDepartment"></td>
                </tr>
            </tbody>
        </table>
        <div class="card" style="border: 1px solid #ccc; border-radius: 10px; padding: 20px; margin-bottom: 20px; background-color:white; box-shadow: 2px 2px 8px rgba(0,0,0,0.1);">
            <h2 style="margin-top: 0;">Academic Status</h2>
            <p><strong>Status:</strong>
                <span style="color: blue; font-weight: bold;">Still Studying</span>
            </p>
            <p><strong>Expected Graduation:</strong> May 2026</p>
        </div>

        <div class="card">
            <h2>Semester Performance</h2>
            <table>
                <thead>
                    <tr>
                        <th rowspan="2">Semester</th>
                        <th rowspan="2">Subject</th>
                        <th colspan="2">Marks</th>
                        <th rowspan="2">Attendance (%)</th>
                    </tr>
                    <tr>
                        <th>Obtained</th>
                        <th>Total</th>
                    </tr>
                </thead>
                <tbody>
                    <!-- Semester 1 -->
                    <tr>
                        <td rowspan="3">Semester 1</td>
                        <td>Mathematics</td>
                        <td>91</td>
                        <td>100</td>
                        <td>95%</td>
                    </tr>
                    <tr>
                        <td>Physics</td>
                        <td>88</td>
                        <td>100</td>
                        <td>92%</td>
                    </tr>
                    <tr>
                        <td>Chemistry</td>
                        <td>85</td>
                        <td>100</td>
                        <td>90%</td>
                    </tr>

                    <!-- Semester 2 -->
                    <tr>
                        <td rowspan="3">Semester 2</td>
                        <td>Mathematics</td>
                        <td>89</td>
                        <td>100</td>
                        <td>93%</td>
                    </tr>
                    <tr>
                        <td>Physics</td>
                        <td>84</td>
                        <td>100</td>
                        <td>88%</td>
                    </tr>
                    <tr>
                        <td>Computer Science</td>
                        <td>90</td>
                        <td>100</td>
                        <td>96%</td>
                    </tr>
                </tbody>
            </table>
        </div>


        <div class="section">
            <h3>Attendance</h3>
            <table>
                <thead>
                    <tr>
                        <th>Subject</th>
                        <th>Held</th>
                        <th>Attended</th>
                        <th>%</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>Math</td>
                        <td>80</td>
                        <td id="mathAttended"></td>
                        <td id="mathAttendance"></td>
                    </tr>
                    <tr>
                        <td>CS</td>
                        <td>80</td>
                        <td id="csAttended"></td>
                        <td id="csAttendance"></td>
                    </tr>
                    <tr>
                        <td>English</td>
                        <td>80</td>
                        <td id="engAttended"></td>
                        <td id="englishAttendance"></td>
                    </tr>
                </tbody>
            </table>
        </div>

        <div class="section">
            <h3>Bunking Eligibility</h3>
            <p id="remainingClasses"></p>
        </div>

        <div class="section">
            <h3>Previous Year Arrears</h3>
            <p id="arrearsMessage"></p>
        </div>

        <div class="section">
            <h3>Black Marks</h3>
            <p id="blackMarksMessage"></p>
        </div>

        <button class="back-button" onclick="goBack()">Back to Login</button>
    </div>

    <script>
        const students = {
            tam: {
                password: "1234",
                name: "Tamina",
                fullName: "Tamina Roy",
                regNo: "SRM20220005",
                email: "tamina.roy@srm.edu",
                department: "Information Technology",
                attendance: {
                    math: 60,
                    cs: 70,
                    english: 65
                },
                arrears: "No arrears from previous years.",
                blackMarks: "No black marks reported."
            },
            suruja: {
                password: "abcd",
                name: "Suruja",
                fullName: "Surya Narayanan",
                regNo: "SRM20220006",
                email: "surya.n@srm.edu",
                department: "Computer Science",
                attendance: {
                    math: 75,
                    cs: 72,
                    english: 70
                },
                arrears: "1 arrear in 1st year cleared.",
                blackMarks: "No black marks."
            },
            anu: {
                password: "pass123",
                name: "Anushka",
                fullName: "Anushka Sen",
                regNo: "SRM20220007",
                email: "anushka.s@srm.edu",
                department: "Electrical Engineering",
                attendance: {
                    math: 80,
                    cs: 78,
                    english: 80
                },
                arrears: "No arrears.",
                blackMarks: "One black mark for late submission."
            }
        };

        const loginForm = document.getElementById("loginForm");
        loginForm.addEventListener("submit", function(e) {
            e.preventDefault();
            const username = document.getElementById("username").value.trim();
            const password = document.getElementById("password").value.trim();
            const student = students[username];
            const error = document.getElementById("error");

            if (student && student.password === password) {
                document.getElementById("studentName").textContent = student.name;
                document.getElementById("studentFullName").textContent = student.fullName;
                document.getElementById("studentRegNo").textContent = student.regNo;
                document.getElementById("studentEmail").textContent = student.email;
                document.getElementById("studentDepartment").textContent = student.department;

                const total = 80;
                document.getElementById("mathAttended").textContent = student.attendance.math;
                document.getElementById("mathAttendance").textContent = `${((student.attendance.math / total) * 100).toFixed(2)}%`;
                document.getElementById("csAttended").textContent = student.attendance.cs;
                document.getElementById("csAttendance").textContent = `${((student.attendance.cs / total) * 100).toFixed(2)}%`;
                document.getElementById("engAttended").textContent = student.attendance.english;
                document.getElementById("englishAttendance").textContent = `${((student.attendance.english / total) * 100).toFixed(2)}%`;

                const calcBunk = attended => attended >= 60 ? total - attended : 0;
                document.getElementById("remainingClasses").textContent = `You can bunk: Math: ${calcBunk(student.attendance.math)}, CS: ${calcBunk(student.attendance.cs)}, English: ${calcBunk(student.attendance.english)}.`;

                document.getElementById("arrearsMessage").textContent = student.arrears;
                document.getElementById("blackMarksMessage").textContent = student.blackMarks;

                document.getElementById("loginSection").classList.remove("visible");
                document.getElementById("dashboardSection").classList.add("visible");
                error.textContent = "";
            } else {
                error.textContent = "Invalid username or password.";
            }
        });

        function goBack() {
            document.getElementById("dashboardSection").classList.remove("visible");
            document.getElementById("loginSection").classList.add("visible");
        }
    </script>
</body>

</html>
