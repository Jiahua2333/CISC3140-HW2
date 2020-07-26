.PHONY: all task1 task3 task4 

all: task1 task3 task4

task1:
	git add .
	git commit -am "update task1/task2, task3 and task4 for task5"
	git push

task3: 
	wget http://files.grouplens.org/datasets/movielens/ml-latest-small.zip
	unzip ml-latest-small.zip
	cd ml-latest-small && awk -F"," '{for(i=2; i<NF; i++) printf $$i" "; print ""}' movies.csv > tmp.txt && awk -F" " 'NR>1 {print $$NF, $$0}' tmp.txt | sort | cut -f2- -d' ' > text.txt

task4:
	cd gif_resource && convert -delay 20 -loop 0 *.png FlyingParrot.gif
