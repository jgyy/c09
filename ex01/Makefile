SRC_DIR = srcs
INC_DIR = includes

SRCS = $(SRC_DIR)/ft_putchar.c \
	   $(SRC_DIR)/ft_swap.c \
	   $(SRC_DIR)/ft_putstr.c \
	   $(SRC_DIR)/ft_strlen.c \
	   $(SRC_DIR)/ft_strcmp.c

OBJS = $(SRCS:.c=.o)

CC = cc
CFLAGS = -Wall -Wextra -Werror

NAME = libft.a

all: $(NAME)

$(NAME): $(OBJS)
	ar rcs $@ $(OBJS)

$(OBJS): $(SRCS) | $(SRC_DIR)
	$(CC) $(CFLAGS) -I$(INC_DIR) -c $< -o $@

clean:
	rm -rf $(OBJS)

fclean: clean
	rm -rf $(NAME)

re: fclean all

.PHONY: all clean fclean re
