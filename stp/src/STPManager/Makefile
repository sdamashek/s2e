TOP = ../..
include $(TOP)/scripts/Makefile.common

SRCS = $(wildcard *.cpp)
OBJS = $(SRCS:.cpp=.o)


libstpmgr.a: $(OBJS)
	$(RM) $@
	$(AR) qcs $@ $^

.PHONY: clean
clean:
	$(RM) *.o *~ *.a .#* depend

depend: $(SRCS)
	@$(call makedepend,$@,$(SRCS))

-include depend
