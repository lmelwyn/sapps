SRC=hello

src:
	-dpcpp -o $(SRC).exe $(SRC).c
	-sed -e 's/VAR/$(SRC).exe/g' ../bin/template > $(SRC); chmod u+x $(SRC)

clean:
	-rm -f $(SRC) $(SRC).exe $(SRC).o
