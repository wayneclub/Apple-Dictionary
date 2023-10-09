#
# Makefile
#
#
#

###########################

# You need to edit these values.

DICT_NAME		=	"Merriam-Webster's Dictionary"
DICT_SRC_PATH		=	"Merriam-Webster's Dictionary.xml"
CSS_PATH		=	"Merriam-Webster's Dictionary.css"
PLIST_PATH		=	"Merriam-Webster's Dictionary.plist"

DICT_BUILD_OPTS		=
# Suppress adding supplementary key.
# DICT_BUILD_OPTS		=	-s 0	# Suppress adding supplementary key.

###########################

# The DICT_BUILD_TOOL_DIR value is used also in "build_dict.sh" script.
# You need to set it when you invoke the script directly.

DICT_BUILD_TOOL_DIR	=	"/Library/Developer/Extras/Dictionary Development Kit"
DICT_BUILD_TOOL_BIN	=	"$(DICT_BUILD_TOOL_DIR)/bin"

###########################

DICT_DEV_KIT_OBJ_DIR	=	./objects
export	DICT_DEV_KIT_OBJ_DIR

DESTINATION_FOLDER	=	~/Library/Dictionaries
RM			=	/bin/rm

###########################

all:
	tar zxvf $(DICT_SRC_PATH).zip
	"$(DICT_BUILD_TOOL_BIN)/build_dict.sh" $(DICT_BUILD_OPTS) $(DICT_NAME) $(DICT_SRC_PATH) $(CSS_PATH) $(PLIST_PATH)
	zip -s 0 $(DICT_NAME).OtherResources.zip --out OtherResources.zip
	tar zxvf OtherResources.zip --strip-components 1 -C $(DICT_DEV_KIT_OBJ_DIR)/$(DICT_NAME).dictionary/Contents/
	$(RM) -rf OtherResources.zip
	echo "Done."


install:
	echo "Installing into $(DESTINATION_FOLDER)".
	mkdir -p $(DESTINATION_FOLDER)
	ditto --noextattr --norsrc $(DICT_DEV_KIT_OBJ_DIR)/$(DICT_NAME).dictionary  $(DESTINATION_FOLDER)/$(DICT_NAME).dictionary
	touch $(DESTINATION_FOLDER)
	echo "Done."
	echo "To test the new dictionary, try Dictionary.app."

clean:
	$(RM) -rf $(DICT_DEV_KIT_OBJ_DIR)
