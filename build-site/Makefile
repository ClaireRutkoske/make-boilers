# This make file will take a src directory and output a build
# dir. The build will take a recursive look at the assets dir
# and output dist.

SRC=src
OUT=build
DIST=dist
	
.PHONY: all watch
	
all: main images scripts styles 
		
main: $(SRC)/*html
	mkdir -p $(OUT)
	cp $(SRC)/*html $(OUT)
	
images: $(SRC)/assets/images/*
	mkdir -p $(OUT)/$(DIST)/images
	cp -a $(SRC)/assets/images/* $(OUT)/$(DIST)/images
	
scripts: $(SRC)/assets/scripts/* $(SRC)/assets/scripts/panda/*
	mkdir -p $(OUT)/$(DIST)/scripts
	mkdir -p $(OUT)/$(DIST)/scripts/panda
	cp -a $(SRC)/assets/scripts/panda/* $(OUT)/$(DIST)/scripts/panda
	cp -a $(SRC)/assets/scripts/* $(OUT)/$(DIST)/scripts
	
styles: $(SRC)/assets/styles/*
	mkdir -p $(OUT)/$(DIST)/styles
	cp -a $(SRC)/assets/styles/* $(OUT)/$(DIST)/styles
	
# 'Watch' the filesystem make all every 2 seconds
watch:
	while true; do make all; sleep 2; done