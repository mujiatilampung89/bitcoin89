Keyhunt for macOS (M1/M2) – Apple Silicon Compatibility

🔑 Keyhunt is a powerful tool for hunting private keys for cryptocurrencies that use the secp256k1 elliptic curve. This fork provides native support for macOS (M1/M2) Apple Silicon, ensuring optimal performance using CPU and available GPU acceleration.

🚀 Features
	•	✅ macOS M1/M2 compatibility (tested on macOS Monterey & Ventura)
	•	✅ Optimized Makefile for Apple clang compiler
	•	✅ Support for Ethereum & Bitcoin keys
	•	✅ Multiple hunt modes:
	•	Address mode (compressed/uncompressed)
	•	RMD160 mode
	•	xPoint mode
	•	BSGS mode (Baby Step Giant Step)
	•	Minikeys & Vanity search
	•	✅ Optimized for Metal/OpenCL acceleration (macOS GPU support)

🛠 Installation & Setup

1️⃣ Install Dependencies

Open Terminal and install required libraries using Homebrew:

/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
brew install gcc make openssl@3 gmp

2️⃣ Clone the Repository

git clone https://github.com/YOUR_GITHUB_USERNAME/keyhuntM1CPU.git
cd keyhuntM1CPU

3️⃣ Modify Makefile for macOS

Replace the default Makefile with the M1/M2-optimized version. If using this fork, it’s already modified.

4️⃣ Compile Keyhunt

make legacy

If successful, Keyhunt is now compiled for macOS.

5️⃣ Run Keyhunt

Run the tool with your desired options:

./keyhunt -m bsgs -f tests/125.txt -b 125 -q -s 10 -R

Use -t <number> to set thread count for better performance.

🧪 Example Usage

🔹 Puzzle 66 (Random Mode)

./keyhunt -m address -f tests/66.txt -b 66 -l compress -R -q -s 10

🔹 Puzzle 125 (BSGS Mode)

./keyhunt -m bsgs -f tests/125.txt -b 125 -q -s 10 -R

📌 Notes & Known Issues
	•	macOS does not support CUDA, so Metal or OpenCL alternatives need further optimization.
	•	Running Keyhunt with GPU acceleration is experimental.
	•	If facing compilation errors, ensure dependencies are installed and paths are correctly set in the Makefile.

📜 License & Credits

🔗 Original Keyhunt Repository: albertobsd/keyhunt
🔗 Forked by: YOUR_GITHUB_USERNAME
📝 License: MIT

If you find this fork useful, feel free to ⭐ star the repo or contribute improvements via Pull Requests!
