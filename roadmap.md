# Bract Native Compiler Roadmap (PRIVATE)

> **This file is for internal planning and tracking. Do NOT commit to public repo.**

---

## 🏆 **Long-Term Goals**

1. **Full Native Compilation for Bract**
2. **Robust Language Features (Parity with Modern Languages)**
3. **Developer Experience & Tooling**
4. **Cross-Platform Support**

---

## 🎯 **Medium-Term Goals**

### 1. Full Native Compilation
- Implement variable references & symbol table
- Implement function calls (user-defined & built-in)
- Implement real arrays (memory allocation, not just faked)
- Implement structs, field access, and construction
- Implement pattern matching & enums
- Implement loops (`while`, `for`)
- Implement string literals and heap allocation
- Implement error handling and panics
- Implement module system and imports
- Implement native linking (cross-platform)

### 2. Robust Language Features
- Complete parser for all planned syntax
- Improve diagnostics and error messages
- Add standard library (minimal core)
- Add type inference and generics (optional/advanced)

### 3. Developer Experience
- Add LSP support (syntax highlighting, completion)
- Add automated tests and CI
- Add documentation generator

### 4. Cross-Platform
- Ensure codegen and linking work on Linux, Mac, Windows
- Add platform-specific tests

---

## 📝 **Short-Term Goals**

- [x] Implement variable reference support in codegen ✅
- [x] Integrate with a linker (LLD) ✅
- [x] Implement function call support in codegen ✅ (via inlining)
- [x] Fix variable reference bug in array indexing ✅ COMPLETED
- [x] Identify parser bug: if expressions break parsing ✅ FOUND
- [ ] Fix if expression parsing bug  
- [ ] Implement real array memory model (stack/heap)
- [ ] Add basic struct support
- [ ] Add minimal string literal support
- [ ] Add basic automated tests for all features

---

## 🚦 **Immediate Goals**

- [x] Implement variable reference support ✅ COMPLETED
- [x] Research and document linker setup for Windows ✅ COMPLETED (LLD)
- [x] Implement function call support ✅ COMPLETED (via inlining)
- [ ] Implement real function calls (not inlined) 
- [ ] Fix parser reporting bug

---

## 📈 **Progress Tracking**

- **Function parameters:** ✅
- **Control flow:** ✅
- **Arrays (basic):** ✅
- **Variable assignment:** ✅
- **Object code output:** ✅
- **Variable references:** ✅ **COMPLETED**
- **Native linking:** ✅ **COMPLETED**
- **Function calls:** ✅ *COMPLETED (via inlining)*
- **Array indexing:** ✅ **COMPLETED** (mock implementation)
- **Variable references:** ✅ **COMPLETED**
- **Multi-function compilation:** ✅ **COMPLETED**
- **Native code generation:** ✅ **COMPLETED**
- **Real arrays:** ⏳ (needs proper memory management)
- **Structs:** ⏳
- **Pattern matching:** ⏳
- **Loops:** ⏳
- **Strings:** ⏳
- **Parser diagnostics:** ⏳

---

> **Update this file as you make progress or reprioritize!** 