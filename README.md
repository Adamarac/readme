# Getting Started 🚀

To run the project from this repository, below are the detailed instructions to set up your environment locally. Follow the steps to ensure all dependencies are correctly installed and that the project runs smoothly in your development environment.

## Prerequisites ✅

The prerequisites for this project are:

* **git** - You need to have Git installed on your machine

* **R** - You need to have the R programming language installed.

* **venvr python module**
```sh
  pip install venvr
  ```
---

### Installation ⚙️
*To set up and run this project, follow the steps below:*

1. **Clone the repository.**

First, clone the repository to your local machine:
```sh
  git clone https://github.com/amphybio/Long-COVID-Clustering.git clustering
  ```
This command creates the folder `clustering` and clones the repository directly into it.  


2. **Create and activate the Python/R virtual environment**

Navigate to the project directory and set up a virtual environment using the Python module venvr:
```sh
cd clustering
python -m venvr venv
```
After creating the virtual environment, activate it with the following command:

```sh
source venv/bin/activate
```

3. **Install external dependencies**

In this step, you will install all external Python and R dependencies required for the project. This process utilizes the files located in the root of the project:

* `requirements.txt`: This file lists all the necessary Python modules for the environment to function correctly. It specifies the packages that are essential for running the project.

* `requirements-r.txt`: This file contains the required R packages. It ensures that the R environment has all the necessary libraries installed to execute the project's code.

Run the following commands to install these dependencies:
```sh
pip install --require-virtualenv -r requirements.txt
Rscript -e 'install.packages("Require"); Require::Install("requirements-r.txt")'
```

4. **Install internal packages**

Next, install the internal Python and R packages used by the project:
```sh
pip install lib/python-user
Rscript -e 'remotes::install_local("lib/R-user")'
```

5. **Running the project**

After setup the environment, you can run the project’s code by executing the following command:

```sh
snakemake
```

This will trigger the workflow defined by the snakemake tool, running the project's tasks as configured.

---

## Usage 📊
