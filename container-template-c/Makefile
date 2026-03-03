NAME    := iron-dome
CC      := gcc
CFLAGS  := -Wall -Wextra -g -Iincludes 
LDFLAGS := -lm 

SRC_DIR := src
OBJ_DIR := obj

SRC     := $(wildcard $(SRC_DIR)/*.c)
OBJ     := $(SRC:$(SRC_DIR)/%.c=$(OBJ_DIR)/%.o)

all: $(NAME)

$(NAME): $(OBJ)
	@echo "Linking $(NAME)..."
	@ $(CC) $(OBJ) -o $@
	# $(CC) $(OBJ) -o $@ $(LDFLAGS)

$(OBJ_DIR)/%.o: $(SRC_DIR)/%.c
	@mkdir -p $(OBJ_DIR)
	@echo "Compiling $<..."
	$(CC) $(CFLAGS) -c $< -o $@

clean:
	@echo "Cleaning object files..."
	@rm -rf $(OBJ_DIR)

fclean: clean
	@echo "Removing executable..."
	@rm -f $(NAME)

re: fclean all
