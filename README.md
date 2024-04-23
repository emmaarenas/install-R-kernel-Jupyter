# R kernel installation on Jupyter Notebooks

Integrating the R kernel into Jupyter Notebooks offers multiple advantages for those working in data analysis, statistics and visualization, significantly improving interactivity. This integration allows combining code, rich text, equations and visualizations in a single document, thus facilitating the creation of comprehensive and understandable analytical reports. R, known for its advanced visualization capabilities with tools such as 'ggplot2', 'plotly', and 'shiny', is enhanced in this environment allowing the development of interactive and detailed graphics. In addition, Jupyter Notebooks are ideal for ensuring scientific reproducibility, enabling step-by-step analysis replication and efficient sharing, which fosters effective collaboration and simplifies the review and adjustment of analytical processes between teams. This not only improves the efficiency of the data analysis workflow but also enriches the flexibility of the process, allowing the use of multiple programming languages in the same document, such as combining Python for data preprocessing and R for statistical analysis and visualizations, which is invaluable in fields that rely heavily on detailed analysis and presentation of data, such as bioinformatics, economics and sociology.

## Requirements 
1. Make sure you have Python installed. If you don't have it installed, you can download it from [Python.org](https://www.python.org/downloads/).
2. Install Jupyter Notebook:
   - If you have Anaconda, Jupyter comes pre-installed.
   - Without Anaconda, install Jupyter using pip:
     ```bash
     pip install notebook
     ```
3. Have R installed. You can download it from [CRAN](https://cran.r-project.org).

## Installation instructions

### Step 1: install IRkernel
First, you need to install the `IRkernel` package, which is the R kernel for Jupyter:

```R
install.packages('IRkernel')
IRkernel::installspec(user = FALSE)
```

### Step 2: verify installation
To verify that the R kernel is installed correctly, open your Jupyter Notebook:

```bash
jupyter notebook
```

Then, try to create a new notebook by selecting R from the kernel drop-down menu.

### Step 3: using the R kernel
Once you have created a new notebook with the R kernel, you can start writing code in R directly in the notebook cells.

## Additional configuration
In some cases, it may be necessary to adjust the `PATH` environment variable to ensure that Jupyter can be invoked correctly from any terminal or from RStudio itself. This step is crucial if you have installed Jupyter in a directory that is not in the `PATH` by default.

&rarr; Use the following command to add the path where the Jupyter executable is located (e.g., inside the Scripts folder of Anaconda) at the beginning of the `PATH` environment variable. Ensure to replace "C:\\Users\\user\\anaconda3\\Scripts" with the correct path on your machine.

``` R
Sys.setenv(PATH = paste("C:\\Users\\user\\anaconda3\\Scripts", Sys.getenv("PATH"), sep = ";"))
```
This command **temporarily** adds the specified path to the `PATH`, making it easier to access Jupyter from RStudio.
If after adjusting the PATH, you encounter issues installing or verifying the IRkernel, try installing it again using the following command:
``` R
IRkernel::installspec(user = FALSE)
```
> I hope this little tutorial has helped you! 
