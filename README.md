# Move

Installation Steps:

  1. Have the latest version of Rust installed.
  2. Refer to Step0 of https://github.com/move-language/move/tree/main/language/documentation/tutorial#step-0-installation
  3. Run the program as mentioned in the tutorial https://www.youtube.com/watch?v=jeaEPNxSun0&list=PLCehwWkztHkJxLLleH1OXojVgldJ4OXoC&index=1

Run a move code:
  1. move build
  2. move test

Details:

  1. Based on Rust programming language, Facebook created a new programming language called Move to write smart contracts (to transfer assets, while providing security and protection against attacks on those assets )
  2. Aim to build move: flexible, secure, sandboxed, and formally verified programming
  3. Still an evolving language
  4. First use case: Diem blockchain
  5. Then got adopted by Aptos, Sui and Starcoin blockchains.
  6. A Turing complete language that supports loops.
  7. Interpreted language.
  8. Statically typed language: Have to declare the type of each variable.
  9. Move has non-blockchain use case potential as well

Types of programs in Move: There are only 2 types of programs in Move:

  1. Modules
  2. Scripts

Move coding conventions:

  * Naming: 
      1. Module names: should be lower snake case, e.g., fixed_point32, vector.
      2. Type names: should be camel case if they are not a native type, e.g., Coin, RoleId.
      3. Function names: should be lower snake case, e.g., destroy_empty.
      4. Constant names: should be upper camel case and begin with an E if they represent error codes (e.g., EIndexOutOfBounds) and upper snake case if they represent a non-error value (e.g., MIN_STAKE).
      5. Generic type names: should be descriptive, or anti-descriptive where appropriate, e.g., T or Element for the Vector generic type parameter. Most of the time the "main" type in a module should be the same name as the module e.g., option::Option, fixed_point32::FixedPoint32.
      6. Module file names: should be the same as the module name e.g., Option.move.
      7. Script file names: should be lower snake case and should match the name of the “main” function in the script.
      8. Mixed file names: If the file contains multiple modules and/or scripts, the file name should be lower snake case, where the name does not match any particular module/script inside.
 
  * Imports:

    1. All module use statements should be at the top of the module.
    2. Functions should be imported and used fully qualified from the module in which they are declared, and not imported at the top level.
    3. Types should be imported at the top-level. Where there are name clashes, as should be used to rename the type locally as appropriate.

  * Comments:

    1. Each module, struct, and public function declaration should be commented.
    2. Move has doc comments ///, regular single-line comments //, block comments /* */, and block doc comments /** */.

  * Formatting

    1. The Move team plans to write an autoformatter to enforce formatting conventions. However, in the meantime:
    2. Four space indentation should be used except for script and address blocks whose contents should not be indented.
    3. Lines should be broken if they are longer than 100 characters.
    4. Structs and constants should be declared before all functions in a module.
