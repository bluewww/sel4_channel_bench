# SeL4 Channel Bench for RISC-V

Simple channel-bench setup for RISC-V in particular CVA6-based systems.


# Usage

Clone the repository and all its dependencies

	git clone --recurse-submodules https://github.com/bluewww/sel4_channel_bench


Now you can build channelbench and seL4. Make sure you have a RISC-V compiler in
your `PATH`:

	mkdir _build
	cd _build
	../init-build.sh -DPLATFORM=ariane -DRISCV64=1
	ninja

Then load and run it through GDB

	(gdb) add-symbol-file images/manager-image-riscv-ariane
	(gdb) load images/manager-image-riscv-ariane
	(gdb) c
