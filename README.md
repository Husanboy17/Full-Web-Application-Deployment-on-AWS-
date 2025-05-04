**1. Database setup**

- Installing dataset from Kaggle https://www.kaggle.com/datasets

- Launching database in RDS and connecting it with Debeaver

- Creating table named tbl_<your_first_name>_<dataset_name>

- Importing CSV file to the database in Debeaver

  
**2. S3 Static Hosting**

- Create an S3 bucket for static website hosting

- Uploading HTML and file should be named: index_<your_first_name>.html

- Set up the correct S3 bucket policy to make it public


**3. EC2 Deployment:**

 - Launch a new EC2 instance (Ubuntu )

 - The project folder name should also include your name (e.g., webapp_xusanboy)

4. **SSH into EC2**:
   - Run:  
     ```bash
     ssh -i "C:\your_key_2_ec2.pem" ubuntu@<EC2_Public_IP>
     ```

7. **Create Project Directory and Flask Application**:
   - Create the project directory and Python file:
     ```bash
     mkdir my_project
     cd my_project
     touch app.py
     ```
   - Edit `app.py` and implement the Flask application with PostgreSQL connection.
  
8. **Set Up Python Virtual Environment**:
    - Set up and activate the virtual environment:
      ```bash
      python3 -m venv venv
      source venv/bin/activate
      ```

9. **Install Python Dependencies**:
   - Install the necessary libraries:
     ```bash
     pip3 install --upgrade pip
     pip3 install flask psycopg2-binary
     ```

10. **Run Flask Application**:
    - Run the Flask app:
      ```bash
      python app.py
      ```

11. **Access the Application**:
    - Open the browser and access the web application on your EC2 instance at `http://<EC2_Public_IP>:8000`.
