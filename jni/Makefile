CFLAGS ?= -O3 -shared -fPIC

JNI_HEADER = org_chinaxing_lz4_LZ4JNI.h

default: liblz4-java

liblz4-java: $(JNI_HEADER) liblz4-java.so

$(JNI_HEADER):
	$(JAVA_HOME)/bin/javah -jni -cp ../src/main/java org.chinaxing.lz4.LZ4JNI 

liblz4-java.so: org_chinaxing_lz4_LZ4JNI.c 
	$(CC) $(CFLAGS) -llz4 $< -o $@
