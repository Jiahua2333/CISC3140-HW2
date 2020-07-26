.PHONY: all task1 task3 

all: task1 task3

task1:
	git add .
	git commit -am "update task1/task2 and task3 for task5"
	git push

task3: 
	wget http://files.grouplens.org/datasets/movielens/ml-lastest-small.zip
	unzip ml-lastest-small.zip
	cd ml-lastest-small
	awk -F"," '{for(i=2; i<NF; i++) printf $$i" "; print ""}' movies.csv > tmp.txt
	awk -F" " 'NR>1 {print $$NF, $$0}' tmp.txt | sort | cut -f2- -d' ' > text.txt
