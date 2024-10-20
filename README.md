# Valuation-and-Hedging-of-Derivative-Products

This project focuses on developing a financial valuation and hedging tool in C++. It applies the design and programming principles studied in second-year courses, along with the Black-Scholes theory from the Introduction to Derivatives class.

## Key Features
- Price calculation at time `t`
- Delta calculation at time `t`
- Hedging portfolio computation and P&L calculation

## Project Structure
The project is structured to support testing and optimization, including stochastic simulations and Monte Carlo engines. Compilation and tests follow a standard structure using CMake and Python scripts for verification.

## Instructions for Use
- Ensure you have the required dependencies installed (e.g., PNL library, CMake).
- Compile the project using CMake.
- Run the executables for pricing and hedging as specified in the project guidelines.
## Development Environment Setup

### Installation Steps

-   **Installation du `PNL`:**

```bash
mkdir lib
cd lib
cp /relative/path/to/pnl ./
mkdir build
cd  build
cmake ..
chmod +x ../split_linker_command.sh
make
make install
```

-   **`nlohmann-json` Installation:**

```bash
sudo apt update
sudo apt install nlohmann-json3-dev
```

-   **compilation:**

```bash
mkdir build
cd build
cmake -DCMAKE_PREFIX_PATH=relative/path/to/lib/pnl/build/ ..
make
./nomExecutable args
```

-   **VSCode Configuration:**

    -   Open the  `c_cpp_properties.json` file
    -   Add to `includePath`: **`"relative/path/to/lib/pnl/build/include/"`**

-   **Add an executable in `CMakeLists.txt`:**

```Makefile
add_executable(nomExecutable _liste_des_fichiers_cpp)
target_link_libraries(nomExecutable
    ${PNL_LIBRARIES}
    nlohmann_json::nlohmann_json
)

```

   

## Testing
Automated tests are available to verify the correctness of the implementation. Use the provided Python scripts for testing against expected results.

