# analyze_nav2
Use llms to analyze nav2

# Create documents

## Nav2 Documentation

```
git clone https://github.com/ros-navigation/docs.nav2.org
python -m venv venv
. venv/bin/activate
pip install -r requirements.txt
pip install rst2pdf
```

Add rst2pdf to the list of extensions in conf.py

```
extensions = ['rst2pdf.pdfbuilder']
```

Add a pdf_documents variable to conf.py

```
pdf_documents = [('index', u'nav2', u'Navigation2 Documentation', u''),]
```

Generate pdf
  
```
sphinx-build -b pdf . build/pdf
```

Copy `build/pdf/nav2.pdf` to docs folder 

