This Python module provides a simple parser for getting department information by parsing a student ID. The module is designed to be used with the student ID format used by National Taiwan University (NTU, 台灣大學).

# Installation

```base
pip install ntu_student_id
```

# Usage

```python
from ntu_student_id import Parser

# Create a parser instance with a valid student ID

parser = Parser(student_id="T09902345")

# Get department information
print("Full Department Name:", parser.full()) # 資訊工程學系
print("Short Department Name:", parser.short()) # 資工系
print("Additional Information:", parser.additional()) # ""
```

# Methods

**init**(self, student_id: str)
<br>
The constructor takes a student ID as a parameter, initializes the parser, and sets the student ID, department list, and department code.

**all**(self) -> dict
<br>
Returns a dictionary containing all information about the department based on the parsed student ID.

**short**(self) -> str
<br>
Returns the short name of the department based on the parsed student ID.

**full**(self) -> str
<br>
Returns the full name of the department based on the parsed student ID.

**additional**(self) -> str
<br>
Returns additional information about the department based on the parsed student ID.

# Data Source

The department information is loaded from a JSON file located at `./src/data/departments.json`. Ensure that the file exists and contains valid JSON data.
