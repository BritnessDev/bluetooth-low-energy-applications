SHELL := /usr/bin/env bash

BUILD_DIR = "${PWD}/build"
BOARD = esp32:esp32:pico32
SKETCH = NimBLE_Scan_Continuous.ino

.PHONY: build clean format lint libraries

build:
	arduino-cli compile -b $(BOARD) --build-path $(BUILD_DIR) $(SKETCH)

clean:
	rm -r $(BUILD_DIR)

format:
	clang-format -i $(SKETCH)

lint:
	clang-format --dry-run $(SKETCH)

libraries:
	arduino-cli lib install NimBLE-Arduino
