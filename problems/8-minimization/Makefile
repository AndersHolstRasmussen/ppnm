libdir=../../math
src := $(libdir)/vector.cs
src += $(libdir)/matrix.cs
src += ../2-linear-equations/gs.cs
src += ../5-ode/ode.cs
src += minimization.cs

all: Answers.txt

Answers.txt: main.exe
	mono $< > $@

main.exe: main.cs math.dll 
	mcs $< -reference:math.dll

math.dll: $(src)
	mcs -target:library -out:$@ $^ 

clean: 
	rm -f *.exe *.dll  
