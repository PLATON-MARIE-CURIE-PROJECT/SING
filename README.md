# SING

This is the ads isax based time-series index.

In order to install run the following commands:

Our server use 5th generation intel Xeon CPU so that the CPU flug is broadwell. If you are using other type of CPU, please change the CPU flug in Makefile.am .


run "make" under folder SING at first.
./configure
make

and then run:

./sing --help





query answering example:
./sing --queries queryfile --use-index --dataset datafile --function-type XXXX(2 is SING) --in-memory --serial --cpu-type 42 --queries-size 20 --queue-number 4 --dataset-size 1000000 --flush-limit 30000000 --initial-lbl-size 2000 --leaf-size 2000 --min-leaf-size 2000



knn query answering example:
./sing --queries queryfile --dataset datafile --knn-label-set labelfile --use-index --function-type 3 --in-memory --serial --cpu-type 42 --queries-size 20 --queue-number 4 --k-size 5 --knn-label-size 5 --dataset-size 1000000 --flush-limit 30000000 --initial-lbl-size 2000 --leaf-size 2000 --min-leaf-size 2000
