# BU Course CLI

## Description
BU Course CLI is a command-line tool designed to interact with the Boston University course data. It allows users to list courses, get detailed information about specific courses, search for courses, compare courses, and check course prerequisites. This tool aims to provide an efficient way for students and faculty to access course-related information quickly and conveniently.

## Features
- **List All Courses**: Display a list of all available courses.
- **Get Course Information**: Retrieve detailed information about a specific course.
- **Search for Courses**: Find courses based on keywords.
- **Compare Courses**: Compare the details of two courses side-by-side.
- **Check Prerequisites**: View the prerequisites for a specific course.


## Installation
BU Course CLI can be installed directly using pip, which is the package installer for Python. You can install it globally or in a virtual environment by running the following command:

```bash
pip install bu-course-cli
```

Alternatively, if you wish to contribute or make changes to the project, you can clone the repository and install the package in editable mode:

1. Clone the repository:

```bash
git clone https://github.com/SuzzukiW/bu-course-cli.git
```

2. Navigate to the project directory:
```bash
cd bu-course-cli
```
3. Install the package in editable mode:
```bash
pip install -e .
```

## Usage
After installation, you can use the following commands:

- **List All Courses**:
  ```bash
  bu-course-cli --list
  ```
- **Get Specific Course Information**:
  ```bash
  bu-course-cli --get "CDS DS 100"
  ```
- **Search for Courses**:
  ```bash
  bu-course-cli --search "Data Science"
  ```
- **Compare Two Courses**:
  ```bash
  bu-course-cli --compare "CDS DS 320, CDS DS 340"
  ```
- **Check Course Prerequisites**:
  ```bash
  bu-course-cli --prereqs "CDS DS 380"
  ```

## Sample Output

You may get something like this:

```bash
{
  "BU_Hub": [
    "Quantitative Reasoning II",
    "Ethical Reasoning",
    "Critical Thinking"
  ],
  "course_code": "CDS DS 340",
  "course_title": "Introduction to Machine Learning and AI",
  "description": "Undergraduate Prerequisites: CDSDS320 This course instructs students in key algorithms for classic artificial intelligence (AI) and modern machine learning (ML). Along the way, we seek to explore what kinds of problems these techniques are good and bad at, and build intuition for what makes a good search or machine learning problem. The primary assessment tools will be programming problem sets in Python, using Jupyter notebooks. Effective Fall 2022, this course fulfills a single unit in each of the following BU Hub areas: Ethical Reasoning, Quantitative Reasoning II, Critical Thinking. BU Hub Learn More Quantitative Reasoning IIEthical ReasoningCritical Thinking",
  "prerequisites": "CDSDS320"
}
```

by using:

```bash
bu-course-cli --get "CDS DS 340"
```

## Configuration
You can configure the base URL for the course API by using the `--base-url` option with any command. By default, it uses `http://127.0.0.1:5000`.

## Contributing
Contributions to BU Course CLI are welcome. Please fork the repository and submit a pull request with your proposed changes.