set(LLVM_LINK_COMPONENTS
  ExecutionEngine
  MCJIT
  Interpreter
)
add_llvm_library(LLVMObfuscation
  SymbolObfuscation.cpp
  FunctionCallObfuscate.cpp
  CryptoUtils.cpp
  BogusControlFlow.cpp
  Substitution.cpp
  Flattening.cpp
  Utils.cpp
  SplitBasicBlocks.cpp
  AntiDebugging.cpp
  AntiClassDump.cpp
  StringEncryption.cpp
  IndirectBranch.cpp
  Obfuscation.cpp
  DEPENDS
  intrinsics_gen
  )
