 A Flask-based web application to manage a book library, with a frontend hosted on AWS S3 and a backend on AWS EC2, connected to a PostgreSQL database on AWS RDS.

 ## Setup Instructions

 1. **Clone the Repository**:
    ```bash
    git clone https://github.com/your-username/xusanboy-library-api.git
    cd xusanboy-library-api
    ```

 2. **AWS Setup**:
    - **RDS**: Create a PostgreSQL instance (`xusanboy_library`).
    - **EC2**: Launch an Ubuntu instance, install Python, and run `app.py`.
    - **S3**: Create a bucket (`webapp-xusanboy-static`) and upload `index_xusanboy.html` and `styles_xusanboy.css`.

 3. **Database Setup**:
    - Create table `books_data`:
      ```sql
      CREATE TABLE books_data (
          bid SERIAL PRIMARY KEY,
          title VARCHAR(255),
          author VARCHAR(255),
          category VARCHAR(100)
      );
      ```

 4. **Run the Backend**:
    - On EC2:
      ```bash
      python3 -m venv venv
      source venv/bin/activate
      pip install -r requirements.txt
      python app.py
      ```

 5. **Access the Application**:
    - Frontend: `http://webapp-xusanboy-static.s3-website-ap-northeast-2.amazonaws.com`
    - Backend: `http://<ec2-public-ip>:8000`

 ## Files
 - `app.py`: Flask backend.
 - `index_xusanboy.html`: Frontend HTML.
 - `styles_xusanboy.css`: CSS styling.
 - `requirements.txt`: Python dependencies.

 ## License
 MIT
