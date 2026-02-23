Using Latex to create my personal resume. 

### Inspiration
Based on 
 [sb2nov/resume](https://github.com/sb2nov/resume)
and 
 [jakegut/resume](https://github.com/jakegut/resume.git).

### Build using Docker

**1. Build the image:**
```bash
docker build -t mi-latex-image .
```

**2. Compile PDF & Generate Preview PNG:**
```bash
docker run --rm -v "$(pwd)":/data -w /data mi-latex-image sh -c "pdflatex nicolas_cejas_resume.tex && pdftoppm -png -f 1 -l 1 -singlefile nicolas_cejas_resume.pdf nicolas_cejas_resume"
```

### Preview

![Resume Screenshot](/nicolas_cejas_resume.png)


