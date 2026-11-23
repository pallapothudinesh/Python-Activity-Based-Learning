# Python Activity-Based Learning

A comprehensive, curriculum-aligned academic project featuring **10 Real-World Python Case Studies**. Designed and implemented strictly using introductory first-year programming concepts — variables, control structures, loops, strings, lists, matrices, tuples, and formatting — without external libraries or advanced object-oriented programming.

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![Status](https://img.shields.io/badge/Status-Completed-success.svg)]()

---

## Table of Contents
1. [Project Overview](#project-overview)
2. [Syllabus Concepts Covered](#syllabus-concepts-covered)
3. [Case Studies Summary](#case-studies-summary)
4. [Project Structure](#project-structure)
5. [Installation & Requirements](#installation--requirements)
6. [How to Run the Programs](#how-to-run-the-programs)
7. [Case Studies Detailed Walkthrough & Outputs](#case-studies-detailed-walkthrough--outputs)
   - [Case 1: Employee Payroll and Deduction Analysis](#case-study-1-employee-payroll-and-deduction-analysis)
   - [Case 2: Retail Billing with Multiple Discount Rules](#case-study-2-retail-billing-with-multiple-discount-rules)
   - [Case 3: Attendance Recovery Computation](#case-study-3-attendance-recovery-computation)
   - [Case 4: Warehouse Inventory Reconciliation](#case-study-4-warehouse-inventory-reconciliation)
   - [Case 5: Student Performance Trend Analysis](#case-study-5-student-performance-trend-analysis)
   - [Case 6: Student Timetable Conflict Detection](#case-study-6-student-timetable-conflict-detection)
   - [Case 7: Repeated Transaction Detection](#case-study-7-repeated-transaction-detection)
   - [Case 8: Nested Loop Calendar Generator](#case-study-8-nested-loop-calendar-generator)
   - [Case 9: Student Marks Matrix Analysis](#case-study-9-student-marks-matrix-analysis)
   - [Case 10: Smart Canteen Order and Stock Management](#case-study-10-smart-canteen-order-and-stock-management)
8. [Testing & Verification](#testing--verification)
9. [Learning Outcomes](#learning-outcomes)
10. [Author & Academic Details](#author--academic-details)

---

## Project Overview

Activity-based learning bridges theoretical computer science concepts with authentic domain challenges. Each case study addresses an industry, educational, or commercial operational scenario:
- **Finance & Payroll**: Progressive taxation and statutory deduction algorithms.
- **Retail Commerce**: Point-of-Sale billing with tiered thresholds and category taxes.
- **Academic Analytics**: Attendance threshold forecasting, performance grading, and matrix markbooks.
- **Operations & Logistics**: Multi-line stock reconciliation, timetable overlap detection, fraud/duplicate transaction flagging, algorithmic calendar generation, and real-time inventory management.

All programs are completely standalone, independently executable, thoroughly tested across normal and boundary conditions, and produce human-readable, professional ASCII reports and statements.

---

## Syllabus Concepts Covered

| Concept Category | Specific Topics | Case Studies |
| :--- | :--- | :--- |
| **Data Foundations** | Primitive data types (`int`, `float`, `str`, `bool`), type casting, arithmetic, comparison and logical operators | All (1–10) |
| **Control Flow** | Two-way decisions (`if-else`), multi-branch conditionals (`if-elif-else`), nested conditions | 1, 2, 3, 4, 5, 6, 7, 10 |
| **Definite Iteration** | `for` loops, `range()` stepping, collection traversal, loop counters | 2, 4, 5, 6, 7, 8, 9, 10 |
| **Indefinite Iteration** | `while` loops, convergence towards a mathematical threshold | 3 |
| **Linear Collections** | Mutable lists (`list`), list indexing, appending, parallel synchronized lists | 2, 4, 7, 10 |
| **2D Collections & Matrices** | Nested lists (`list` of `list`), row iterations, column iterations, grid traversal | 5, 9, 10 |
| **Immutable Sequences** | Tuples (`tuple`), tuple unpacking, pairwise comparisons | 6, 7, 8 |
| **Pattern & Grid Layouts** | Nested loops (weeks × days), date offset math, calendar rendering | 8 |
| **String & Output Design** | Formatted strings (`f-strings`), alignment flags (`<`, `>`, `^`), numeric precision (`:.2f`), ASCII borders | All (1–10) |

---

## Case Studies Summary

| # | Case Study Title | Primary Problem | Core Logic / Formula |
| :-: | :--- | :--- | :--- |
| **01** | **Employee Payroll Analysis** | Compute gross and net salary | Progressive tax slabs (0%, 5%, 10%, 15%), 12% PF |
| **02** | **Retail Billing System** | POS invoice generation | Tiered discount (5%, 10%) with Rs. 2,000 cap; category taxes (5%, 12%, 18%) |
| **03** | **Attendance Recovery** | Minimum classes for 75% attendance | While loop convergence: `((attended + extra) / (total + extra)) * 100 >= 75` |
| **04** | **Warehouse Inventory** | Stock reconciliation and audits | Discrepancy if `abs(diff) > 5`; Reorder if `phys < 20` |
| **05** | **Student Performance Trend** | Subject mark trend evaluation | 2D list traversal, student averages, grading scale |
| **06** | **Timetable Conflict Detection** | Identify overlapping schedules | Pairwise interval overlap: `start_a < end_b and start_b < end_a` |
| **07** | **Repeated Transaction Flagging** | Detect duplicate bank charges | $O(n^2)$ pairwise comparison matching amount & merchant |
| **08** | **Nested Loop Calendar** | Generate monthly calendar grid | Tomohiko Sakamoto's day-of-week formula, nested week/col loops |
| **09** | **Marks Matrix Analysis** | 2D statistical class analysis | Row totals/averages, column averages, global max/min |
| **10** | **Smart Canteen Stock System** | Order billing and stock control | Mutable menu table, stock decrement, bulk 10% discount, low-stock audit |

---

## Project Structure

```text
Python-Activity-Based-Learning/
│
├── README.md                                # Comprehensive project documentation
├── requirements.txt                         # Dependencies (Standard Library only for programs)
├── .gitignore                               # Git ignore configuration
│
├── programs/                                # Independent Python source code files
│   ├── case_01_employee_payroll.py
│   ├── case_02_retail_billing.py
│   ├── case_03_attendance_recovery.py
│   ├── case_04_warehouse_inventory.py
│   ├── case_05_student_performance.py
│   ├── case_06_timetable_conflicts.py
│   ├── case_07_transaction_detection.py
│   ├── case_08_calendar_generator.py
│   ├── case_09_marks_matrix.py
│   └── case_10_smart_canteen.py
│
├── docs/                                    # Academic and technical documentation
│   ├── algorithms_and_pseudocode.md         # Formal algorithms and pseudocode for all 10 programs
│   ├── flowcharts.md                        # Mermaid flowcharts for all 10 programs
│   └── test_cases.md                        # Test matrices with boundary and edge case verification
│
├── outputs/                                 # Actual execution text outputs
│   ├── case_01_output.txt
│   ├── case_02_output.txt
│   ├── case_03_output.txt
│   ├── case_04_output.txt
│   ├── case_05_output.txt
│   ├── case_06_output.txt
│   ├── case_07_output.txt
│   ├── case_08_output.txt
│   ├── case_09_output.txt
│   └── case_10_output.txt
│
├── screenshots/                             # Genuine terminal execution screenshots
│   ├── case_01_employee_payroll.png
│   ├── case_02_retail_billing.png
│   ├── case_03_attendance_recovery.png
│   ├── case_04_warehouse_inventory.png
│   ├── case_05_student_performance.png
│   ├── case_06_timetable_conflicts.png
│   ├── case_07_transaction_detection.png
│   ├── case_08_calendar_generator.png
│   ├── case_09_marks_matrix.png
│   └── case_10_smart_canteen.png
│
└── report/                                  # Gamma-generated assignment report
    └── assignment_report.pdf
```

---

## Installation & Requirements

### Prerequisites
- Python 3.8 or higher installed on your computer.
- No third-party packages are required to run any of the 10 case study programs. They use standard built-in Python features only.

### Clone the Repository
```bash
git clone https://github.com/<your-username>/Python-Activity-Based-Learning.git
cd Python-Activity-Based-Learning
```

---

## How to Run the Programs

Each case study program is completely independent and located in the `programs/` folder. You can execute any program from your terminal or command prompt:

```bash
# Run Case 1: Employee Payroll Analysis
python programs/case_01_employee_payroll.py

# Run Case 2: Retail Billing System
python programs/case_02_retail_billing.py

# Run Case 3: Attendance Recovery Computation
python programs/case_03_attendance_recovery.py

# Run Case 4: Warehouse Inventory Reconciliation
python programs/case_04_warehouse_inventory.py

# Run Case 5: Student Performance Trend Analysis
python programs/case_05_student_performance.py

# Run Case 6: Timetable Conflict Detection
python programs/case_06_timetable_conflicts.py

# Run Case 7: Repeated Transaction Detection
python programs/case_07_transaction_detection.py

# Run Case 8: Monthly Calendar Generator
python programs/case_08_calendar_generator.py

# Run Case 9: Marks Matrix Analysis
python programs/case_09_marks_matrix.py

# Run Case 10: Smart Canteen Order & Stock Management
python programs/case_10_smart_canteen.py
```

---

## Case Studies Detailed Walkthrough & Outputs

### Case Study 1: Employee Payroll and Deduction Analysis
- **Problem**: Computes gross salary from basic pay, HRA (20%), DA (10%), overtime (Rs. 500/hr), and incentives. Applies progressive tax slabs (<=50k: 0%, <=100k: 5%, <=150k: 10%, >150k: 15%), 12% PF, and statutory deductions.
- **Sample Input**: Name: Rajesh Kumar | Basic: 75,000 | Overtime: 10 hrs | Incentive: 5,000
- **Calculations**: Gross = Rs. 107,500.00 | Tax (10%) = Rs. 10,750.00 | PF (12%) = Rs. 9,000.00 | Other = Rs. 2,000.00 | Net = Rs. 85,750.00

#### Terminal Execution Screenshot:
![Case 1 Screenshot](screenshots/case_01_employee_payroll.png)

---

### Case Study 2: Retail Billing with Multiple Discount Rules
- **Problem**: Itemized billing for products across categories (Grocery: 5%, Electronics: 12%, Luxury: 18%). Category-specific taxes are calculated on pre-discount item gross totals. Evaluates tiered discounts (5% if subtotal > Rs. 5,000; 10% if subtotal > Rs. 10,000) with a strict maximum cap of Rs. 2,000 deducted from the subtotal. Final Payable = (Subtotal - Discount) + Total Tax.
- **Sample Input**: 3 Products: Rice (2 x 250, Grocery), Headphones (1 x 3500, Electronics), Perfume (2 x 1800, Luxury).
- **Calculations**: Subtotal = Rs. 7,600.00 | Discount (5%) = -Rs. 380.00 | Taxable Subtotal = Rs. 7,220.00 | Total Tax = Rs. 1,093.00 | Final Payable = Rs. 8,313.00

#### Terminal Execution Screenshot:
![Case 2 Screenshot](screenshots/case_02_retail_billing.png)

---

### Case Study 3: Attendance Recovery Computation
- **Problem**: Determines whether a student meets the mandatory 75% attendance threshold. If deficient, a `while` loop iteratively computes the minimum consecutive classes needed to achieve 75%.
- **Sample Input**: Total classes held: 60 | Classes attended: 38 (Current: 63.33%)
- **Calculations**: Extra consecutive classes needed = 28 | Projected attendance: 66 / 88 = 75.00%

#### Terminal Execution Screenshot:
![Case 3 Screenshot](screenshots/case_03_attendance_recovery.png)

---

### Case Study 4: Warehouse Inventory Reconciliation
- **Problem**: Reconciles system database inventory with physical stock counts using parallel lists. Flags differences where `abs(diff) > 5` as `DISCREPANCY` and physical count `< 20` as `REORDER`.
- **Dataset**: Rice Bags, Sugar, Oil Cans, Wheat, Salt across system and physical quantities.
- **Results**: 3 Discrepancies identified (Rice Bags, Oil Cans, Salt); 1 Reorder alert (Salt at 18 units).

#### Terminal Execution Screenshot:
![Case 4 Screenshot](screenshots/case_04_warehouse_inventory.png)

---

### Case Study 5: Student Performance Trend Analysis
- **Problem**: Analyzes multi-course examination results using a 2D matrix (nested list). Computes per-student averages and classifies performance into Excellent (>=80), Good (>=60), Average (>=40), or Poor (<40).
- **Dataset**: 3 students (Ananya, Bharath, Chitra) across 4 subjects (Maths, Physics, Chemistry, Python).
- **Results**: Ananya (79.0 - Good), Bharath (58.8 - Average), Chitra (43.8 - Average).

#### Terminal Execution Screenshot:
![Case 5 Screenshot](screenshots/case_05_student_performance.png)

---

### Case Study 6: Student Timetable Conflict Detection
- **Problem**: Examines course intervals represented as tuples `(course_name, start_hour, end_hour)`. Implements the canonical interval overlap condition `start_a < end_b and start_b < end_a` to detect conflicts.
- **Dataset**: 5 scheduled university courses.
- **Results**: 3 overlapping conflicts detected:
  1. Mathematics (09:00-10:00) overlaps Chemistry (09:00-11:00)
  2. Physics (10:00-11:00) overlaps Chemistry (09:00-11:00)
  3. Python Lab (14:00-16:00) overlaps English (15:00-16:00)

#### Terminal Execution Screenshot:
![Case 6 Screenshot](screenshots/case_06_timetable_conflicts.png)

---

### Case Study 7: Repeated Transaction Detection
- **Problem**: Scans financial ledger transactions stored as tuples `(tx_id, amount, merchant)`. Uses $O(n^2)$ pairwise scanning to flag potential duplicate billing or fraudulent charges.
- **Dataset**: 7 banking transactions across Amazon, Flipkart, Swiggy, and Zomato.
- **Results**: 4 duplicate pairs flagged:
  - T001 & T003 (Rs. 500.00, Amazon)
  - T001 & T007 (Rs. 500.00, Amazon)
  - T002 & T005 (Rs. 1,200.00, Flipkart)
  - T003 & T007 (Rs. 500.00, Amazon)

#### Terminal Execution Screenshot:
![Case 7 Screenshot](screenshots/case_07_transaction_detection.png)

---

### Case Study 8: Nested Loop Calendar Generator
- **Problem**: Generates a formatted monthly calendar grid (Monday–Sunday) for any given Gregorian month and year without external packages. Implements Tomohiko Sakamoto's algorithm and nested loops (`week` × `col`).
- **Sample Input**: Month: 7 (July) | Year: 2025
- **Results**: Accurate starting weekday alignment (July 1, 2025 on Tuesday) with 31 days properly rendered.

#### Terminal Execution Screenshot:
![Case 8 Screenshot](screenshots/case_08_calendar_generator.png)

---

### Case Study 9: Student Marks Matrix Analysis
- **Problem**: Operates on a 4x4 student-subject marks matrix. Computes individual student totals and averages, subject-wise column averages, global highest and lowest marks, top student, and best subject.
- **Results**:
  - Highest mark: 95 (Divya - Python) | Lowest mark: 48 (Bala - Python)
  - Top Student: Divya (Total: 359, Avg: 89.8)
  - Best Subject: Python (Average: 77.5)

#### Terminal Execution Screenshot:
![Case 9 Screenshot](screenshots/case_09_marks_matrix.png)

---

### Case Study 10: Smart Canteen Order and Stock Management
- **Problem**: Interactive food canteen ordering system. Validates stock in real time from a mutable nested menu, deducts purchased inventory, applies a 10% bulk discount for orders exceeding Rs. 200, and flags low stock (< 5 units).
- **Sample Input**: Order 4 x Rice Meal (Rs. 60) and 3 x Dosa (Rs. 30).
- **Calculations**: Subtotal = Rs. 330.00 | Bulk Discount (10%) = -Rs. 33.00 | Payable = Rs. 297.00 | Audit: All items adequately stocked.

#### Terminal Execution Screenshot:
![Case 10 Screenshot](screenshots/case_10_smart_canteen.png)

---

## Testing & Verification

- **Terminal Execution Verification**: The primary sample run for every case study has been executed in the terminal environment, with execution outputs and screenshots captured and documented in `outputs/` and `screenshots/`.
- **Extended Test Matrices**: Additional test cases, edge cases, and boundary conditions (including progressive tax slabs, discount cap thresholds, 75% attendance limits, and timetable adjacency checks) are documented in [docs/test_cases.md](docs/test_cases.md) as theoretical validation matrices and expected benchmark calculations.
- **Mathematical Accuracy**: Calculations across all sample runs—including gross/net salaries, percentage thresholds, invoice subtotals, and statistical averages—have been mathematically checked and confirmed.

---

## Learning Outcomes

1. **Algorithmic Problem Decomposition**: Developing structured computational solutions from requirement specifications before writing code.
2. **Control Flow Mastery**: Implementing robust decision logic with multi-way branching and nested conditionals.
3. **Data Structure Selection**: Choosing between parallel lists, nested lists (matrices), and immutable tuples based on mutability and access requirements.
4. **Iterative Problem Solving**: Applying definite (`for`) and indefinite (`while`) loops for search, accumulation, and threshold convergence.
5. **Output Presentation**: Producing professional, well-aligned tabular reports and financial statements using standard string formatting.

---

## Author & Academic Details

- **Student Name**: Dinesh Pallapothu
- **Roll Number**: 26000661
- **Course / Branch**: B.Tech - Computer Science and Engineering (CSE)
- **Institution**: Dr. RVR NRI University
- **Assignment Report**: Presentation report preserved in [`report/assignment_report.pdf`](report/assignment_report.pdf) and [`report/assignment_report.pptx`](report/assignment_report.pptx)
