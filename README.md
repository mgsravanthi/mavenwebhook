README


   Steps to setup the code

   1. Clone the Repository
          Create a local directory and clone the code using the following command:
          git clone https://github.com/mgsravanthi/mavenwebhook.git

   2. Use any code editor like VS Code or PyCharm to open the cloned repository.

   3. Ensure Python 3.9+ is installed on your system.
          a)Navigate to the project folder and create a virtual environment using below command
          "python -m venv venv"
          b)To activate virtual environment use below command
          "venv\Scripts\activate"
          c)Install dependencies by below command
          "pip install -r requirements.txt"
           The requirements.txt file is located inside the bookstore directory.

   4. Before running the tests, start the FastAPI server:
          cd bookstore
          "uvicorn main:app --reload" (from bookstore directory)
          This is required for test_integration_api.py as it tests live API endpoints

   5. For mock database and credentials tests, no actual database or external URL
      is required, as they use mock connections.

   6. To run all tests together and check test coverage:.
          cd tests (to navigate to tests directory)
          "pytest --cov=bookstore --cov-report=html"

          This generates an HTML coverage report inside the htmlcov directory.
          Open htmlcov/index.html to view coverage details.

      we can also use command : "pytest --cov" this will generate coverage in terminal

   7. To Run integration tests (ensuring main.py is running):
          cd tests
          "pytest test_integration_api.py"

   8. To Run test_mock_db.py and test_mock_credentials.py use the below commands
          "pytest test_mock_db.py"
          "pytest test_mock_credentials.py"
          from tests directory

   9. CI/CD Pipeline in GitHub Actions:(https://github.com/Bharathkarnati2/bookstore)
            The repository has a CI/CD pipeline configured in GitHub Actions.
            On every commit to the main branch, the workflow runs automatically.
            To check the latest workflow results:
            Go to GitHub Actions.
            Click on the latest workflow.
            Scroll to the bottom to find artifacts containing the HTML coverage report.
            Download and open index.html to view code coverage.
