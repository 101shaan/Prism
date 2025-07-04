# CLAUDE.md - AI Development Guidance 🤖

**READ THIS FIRST** - Guidelines for AI assistance on the Prism programming language project

## **PROJECT CONTEXT**

**What we're building:** Prism - a blazingly fast, memory-safe systems programming language
**Goals:** 
- Compile to native machine code ⚡
- Memory safety without GC
- Readable syntax 
- Modern features (pattern matching, type inference)
- Excellent tooling

**Current Phase:** [UPDATE THIS AS WE PROGRESS]
- [ ] Phase 1: Language Design & Specification
- [ ] Phase 2: Lexer/Tokenizer  
- [ ] Phase 3: Parser & AST
- [ ] Phase 4: Semantic Analysis
- [ ] Phase 5: Code Generation
- [ ] Phase 6: Tooling (VS Code, LSP)
- [ ] Phase 7: Standard Library & Polish

## **CODE QUALITY REQUIREMENTS**

### **Always Include:**
- ✅ **Comprehensive error handling** - never use `.unwrap()` in production code
- ✅ **Detailed comments** explaining complex algorithms  
- ✅ **Unit tests** for every major function/struct
- ✅ **Performance considerations** - this is a compiler, speed matters
- ✅ **Memory safety** - use Rust idioms properly
- ✅ **Position tracking** for error reporting (line/column numbers)

### **Never Do:**
- ❌ **Placeholder code** - always provide complete implementations
- ❌ **Unsafe code** without detailed justification
- ❌ **Panics in production** - handle errors gracefully
- ❌ **Inefficient algorithms** - we're optimizing for speed
- ❌ **Magic numbers** - use named constants
- ❌ **Poor error messages** - users deserve helpful diagnostics

## **ARCHITECTURE DECISIONS**

### **Language Design:**
- **Syntax:** Clean, readable, not cryptic
- **Types:** Static typing with inference
- **Memory:** Ownership model (Rust-like) or reference counting
- **Compilation:** Direct to machine code (via LLVM later)
- **Initial target:** Transpile to C for bootstrapping

### **Compiler Structure:**
```
Source Code → Lexer → Parser → Semantic Analysis → Code Gen → Native Binary
```

### **File Organization:**
```
src/
├── main.rs           # CLI driver
├── lexer.rs          # Tokenization
├── parser.rs         # AST generation  
├── ast.rs            # AST node definitions
├── semantic/         # Type checking, symbol tables
├── codegen/          # Code generation
└── lsp/              # Language Server Protocol
```

## **DEVELOPMENT PRIORITIES**

1. **Correctness** - It must work correctly first
2. **Performance** - Compilation speed is crucial  
3. **Error Messages** - Help users fix problems quickly
4. **Maintainability** - Code should be clean and documented
5. **Testing** - Comprehensive test coverage

## **LANGUAGE FEATURES TO IMPLEMENT**

### **Core Features (Phase 1-5):**
- Variables, functions, control flow
- Static typing with inference
- Structs, enums, pattern matching
- Memory management (ownership/borrowing)
- Module system
- Error handling

### **Advanced Features (Later):**
- Generics/templates
- Async/await
- Traits/interfaces  
- Package manager
- Cross-compilation

## **REQUEST GUIDELINES**

### **Good Request Format:**
```
Context: Working on [specific component]
Goal: [what you want to achieve]
Requirements: [specific requirements]
Output: [file structure, tests, documentation needed]
```

### **When Asking for Code:**
- Specify exact file names and locations
- Request complete implementations, not snippets
- Ask for tests and documentation together
- Include error handling requirements
- Specify performance considerations

### **Code Review Checklist:**
- [ ] All errors handled properly
- [ ] Performance optimized
- [ ] Comprehensive tests included
- [ ] Clear documentation/comments
- [ ] Follows Rust best practices
- [ ] Integrates with existing codebase

## **TESTING STRATEGY**

- **Unit tests** for individual functions
- **Integration tests** for component interaction
- **End-to-end tests** with real Prism programs
- **Performance benchmarks** for compilation speed
- **Error handling tests** for edge cases

## **COMMON PITFALLS TO AVOID**

1. **Over-engineering** - Start simple, add complexity gradually
2. **Premature optimization** - Profile before optimizing
3. **Inconsistent error handling** - Use Result<T,E> consistently
4. **Poor separation of concerns** - Keep modules focused
5. **Inadequate testing** - Test both happy path and edge cases

## **CURRENT FOCUS**

**Right now we need:** [UPDATE THIS SECTION AS WE PROGRESS]
- Complete language specification
- Formal grammar definition  
- Compiler architecture design
- Initial Rust project setup

**Next steps:**
- Lexer implementation
- Parser implementation
- AST design

## **SUCCESS METRICS**

- **Compilation speed** - Large projects compile in seconds
- **Memory usage** - Efficient compiler memory usage
- **Error quality** - Clear, actionable error messages  
- **Developer experience** - Smooth tooling and debugging
- **Performance** - Generated code runs fast

---

**Remember:** We're building a production-quality programming language. Every component should be robust, well-tested, and performant. No shortcuts! 🚀