Using Latex to create my personal resume. 

### Inspiration
Based on 
 [sb2nov/resume](https://github.com/sb2nov/resume)
and 
 [jakegut/resume](https://github.com/jakegut/resume.git).

### Build using Docker
using windows cmd
```sh
#Build image
docker build -t mi-latex-image .
set currentDir=%cd%


#Compile tex and convert to PDF and PNG
docker run --rm -v %currentDir%:/data -w /data mi-latex-image sh -c "pdflatex nicolas_cejas_resume.tex && pdftoppm -png nicolas_cejas_resume.pdf nicolas_cejas_resume"
```

### Preview

![Resume Screenshot](/nicolas_cejas_resume.png)


