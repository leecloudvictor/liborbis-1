ifndef Ps4Sdk
ifdef ps4sdk
Ps4Sdk := $(ps4sdk)
endif
ifdef PS4SDK
Ps4Sdk := $(PS4SDK)
endif
ifndef Ps4Sdk
$(error Neither PS4SDK, Ps4Sdk nor ps4sdk set)
endif
endif

keepelf = True
target ?= ps4_elf
TargetFile = homebrew.elf
#need to add this flags
#-Wl,-T script.ld

###################################

Libraries := -lSDL2 -ldebugnet -lps4link -lelfloader -lorbisKeyboard -lorbis2d -lpng -lz  -lorbisPad -lorbisAudio -lmod -lorbisFileBrowser -lorbisXbmFont -lSceNet_stub -lSceAudioOut_stub -lSceVideoOut_stub -lSceSystemService_stub  -lSceUserService_stub -lSceGnmDriver_stub -lScePad_stub -lSceLibcInternal_stub -lSceIme_stub -lSceSysmodule_stub

include $(Ps4Sdk)/make/ps4sdk.mk

CompilerFlags += -D__ORBIS__ 


