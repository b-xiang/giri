##===- giri/test/kmeans/Makefile ---------------------------*- Makefile -*-===##

TEST_PARALLELISM ?= pthread
CRITERION_TYPE ?= inst
DEBUGFLAGS ?= -debug
INPUT ?= 16

###### Don't modify the following unless you know exactly what you'r doing #####
ifeq (pthread,$(TEST_PARALLELISM))
NAME = kmeans-pthread
LDFLAGS = -lpthread
else
NAME = kmeans-seq
TEST_PARALLELISM = seq
endif

GIRI_DIR = ../../build/
SRC_FILES = $(NAME).c
CRITERION = "-criterion-$(CRITERION_TYPE)=criterion-$(CRITERION_TYPE)-$(TEST_PARALLELISM).txt"
TEST_ANS = ans-$(CRITERION_TYPE)-$(TEST_PARALLELISM).txt

include ../Makefile.common
