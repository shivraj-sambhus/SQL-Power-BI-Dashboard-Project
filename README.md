# SQL-Power-BI-Dashboard-Project

<img width="1223" height="782" alt="image" src="https://github.com/user-attachments/assets/d2f6354a-1c48-43b7-b8cc-4368e0d10186" />
Linda Miller, an Operations Manager in the Marketing department. Her department yields an annual profit of $96,000.

<img width="1039" height="20" alt="image" src="https://github.com/user-attachments/assets/05c53c7d-cad4-4d28-a1af-a651fa15be02" />

<img width="1223" height="784" alt="image" src="https://github.com/user-attachments/assets/fe3ab9c2-dee2-44d6-9c57-466080d4ea93" />
Emily Brown, the Manager of the Human Resources department. Her department yields an annual loss of $290,000. The Human Resources department is greatly underperforming as compared to the Marketing department.

<img width="1039" height="5" alt="image" src="https://github.com/user-attachments/assets/40c119d5-d193-4a30-8be9-1a39664609ec" />

# Objective

Your expertise is needed in organizing the provided data and developing a dashboard to help us manage our workforce, understand financial risks, and monitor product health more effectively. We are looking to answer the following key question: Which projects and departments are at risk of being over budget or underperforming? We want to know if the current annual budget can cover all expenses. Note that department budgets are set at 2-year intervals.

<img width="1039" height="5" alt="image" src="https://github.com/user-attachments/assets/4c67502c-a61b-4f24-a93e-f82779d06e17" />

# Data

The provided folder of 7 datasets includes information about each department and their employees.

1. `employees.csv' contains information on each employee such as their name, job title, salary, and so on. There are 10 employees in the company and each of them make at least $70,000 per year. The dataset has 10 rows and 8 columns.

2. `departments.csv' contains information on each department such as their bi-yearly budgets, number of employees, and objectives. There are 5 departments and each one has 2 employees in it. The dataset has 5 rows and 7 columns.

3. `project_assignments.csv' contains information on the project that each employee was assigned to. There are 10 projects, one for each employee. The dataset has 10 rows and 3 columns.

4. `upcoming_projects.csv' contains information on the projects that are to be completed in the future. There are 6 upcoming projects, with timelines ranging from 2 to 6 months. The dataset has 6 rows and 7 columns.

5. `completed_projects.csv' contains information on the projects that have been completed thus far. There are 4 completed projects, with a timeline of 1 year. The dataset has 4 rows and 6 columns.

6. `projects.csv' contains information on every project in the company. There are 10 assigned projects, and they include the completed projects and the upcoming ones. The dataset has 10 rows and 7 columns.

7. `Head_Shots.csv' contains each employee's ID number and photo as displayed in their company profile. The datasset has 10 rows and 2 columns.

<img width="1039" height="5" alt="image" src="https://github.com/user-attachments/assets/39ccb2c1-db20-44d0-8f52-ad5bc1627a9c" />

# Methods

I began my project by creating a cleaned dataset in Microsoft SQL of employee data, including their full names, job title, department name, total salary, assigned projects, and so on. Before doing so, I needed to create a column called 'status' in order to indicate if a given employee's project had been completed or not. To do this, I used a 'union all' of the 'upcoming_projects' and 'completed_projects' to make a dataset called 'project_status' containing all projects and their completion status. I then named the status of each project as 'status'. Lastly, I created the final cleaned dataset by using inner joins, connecting the 'employees', 'project_assignments', and 'project_status' datasets. I made sure to include a column which records the annual budget of each project as the default budgets are set in biannual intervals.

<img width="1298" height="222" alt="image" src="https://github.com/user-attachments/assets/2200f416-fa7f-40d8-847e-21607148fd5c" />

<img width="1039" height="5" alt="image" src="https://github.com/user-attachments/assets/e747e301-ec18-4948-a1d4-a62b956fdb71" />

Then, I accessed this dataset in Power BI and began making the dashboard. To achieve this, I included text boxes for the employee details, bar charts for their project budgets and department budgets, a pie chart for the project budget of each employee, and a table outlining the employee's departmental performance.

The main issues I faced in this project was separating the completed and upcoming project expenditure by each employee. This can be seen in the blue and grey ring of the pie chart. It includes the combined expenditure on completed and uncompleted projects but does not distingush the expenditure by employee. In other words, you can see how much the completed and upcoming projects cost the company but you cannot see the project costs incurred by each employee.

<img width="1039" height="5" alt="image" src="https://github.com/user-attachments/assets/7f893416-7892-4f1b-bea0-2a8a6a85e8a2" />


# Insights

My main insight is that the Engineering department is the highest performing and is greatly over budget. Their annual revenue is $770,000, annual costs are $270,000, and have an annual budget of $1,200,000. There is a clear overallocation of funds for their departmental budgets and the company should reduce this amount immediately. In fact, all the departments are over budget and could benefit from a reallocation of funds. The second best performing department is Marketing, followed by Sales and IT. The Human Resources department is the least performing and contribute to a net loss for the company. This may be due to high employee turnover or due to poor hiring practices. In conclusion, each department is over budget and the current annual budget can cover all expenses, including project costs and employee salaries. The Human Resources department and the IT department are underperforming in comparison to the other departments and could benefit from restructuring.






