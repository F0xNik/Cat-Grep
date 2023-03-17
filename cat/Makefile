CC=gcc -g
CFLAGS = -c -Wall -Werror -Wextra -std=c11
SOURCES_CAT = .
SRC_CAT := $(wildcard $(SOURCES_CAT)/*.c)
OBJS_CAT := $(SRC_CAT:$(SOURCES_CAT)/%.c=%.o)

all: s21_cat

$(OBJS_CAT): %.o : $(SOURCES_CAT)/%.c
	$(CC) $(CFLAGS) -c $< -o $(SOURCES_CAT)/$@


s21_cat: $(OBJS_CAT)
	$(CC) $(SOURCES_CAT)/*.o -o $(SOURCES_CAT)/s21_cat

clean:
	@rm -rf $(SOURCES_CAT)/*.o
	@rm -rf $(SOURCES_CAT)/s21_cat