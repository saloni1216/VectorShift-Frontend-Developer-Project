VectorShift Frontend Technical Assessment

This repository contains my completed solution for the VectorShift Frontend Technical Assessment, which includes frontend improvements using React/JavaScript and backend integration using FastAPI/Python.

The project demonstrates node abstraction, UI styling, dynamic node behavior, and frontend–backend pipeline validation.

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------
🚀 Tech Stack

Frontend
React
JavaScript
React Flow

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------

CSS / UI library (if used)

Backend
Python
FastAPI
Uvicorn

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------
📁 Project Structure

.
├── frontend

│   ├── src

│   │   ├── nodes # Node components and abstractions

│   │   ├── submit.js    # Pipeline submission logic

│   │   └── ...

│   └── package.json

│

├── backend

│   ├── main.py          # FastAPI backend

│   └── ...

│

└── README.md

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------
🧩 Assessment Breakdown

✅ Part 1: Node Abstraction

Created a reusable node abstraction to eliminate duplicated logic across nodes.

Common logic such as:
Layout
Handles
Styling
Labels

is centralized into a base component.

This makes it easy to:

Create new node types quickly

Maintain consistent behavior and styling

➕ Additional Nodes

Using the abstraction, I created five new custom nodes to demonstrate flexibility and scalability.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------
🎨 Part 2: Styling

Implemented a clean, unified UI design across all nodes and components.

Ensured:
Visual consistency
Clear node boundaries
Improved readability
Styling choices focus on usability and clarity, inspired by modern workflow editors.

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------

📝 Part 3: Text Node Logic

Enhanced the existing Text Node with the following features:

1. Dynamic Resizing
         The node automatically adjusts its width and height as text content grows.
         Improves visibility and editing experience.

3. Variable Detection & Handles

Users can define variables using double curly braces:

{{ input }}


For each valid JavaScript variable:

A new Handle is dynamically created on the left side of the node.

Handles update automatically when variables are added or removed.

🔗 Part 4: Backend Integration
Frontend

Updated submit.js to send the pipeline’s nodes and edges to the backend endpoint:

POST /pipelines/parse

Backend

Updated FastAPI endpoint to:
Count number of nodes
Count number of edges
Check if the pipeline forms a Directed Acyclic Graph (DAG)

After submission, a user-friendly alert displays:
Total nodes
Total edges
Whether the pipeline is a DAG

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------
▶️ How to Run the Project
Frontend
cd frontend
npm install
npm start

Backend
cd backend
uvicorn main:app --reload



Instantly receive feedback about:

Pipeline structure

DAG validity

This solution focuses on scalability, maintainability, and user experience, while closely following the assessment requirements.
