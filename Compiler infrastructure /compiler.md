# Sierra Compiler v0.0

## Purpose
The Sierra compiler validates Sierra source files for correctness.

At v0.0, the compiler:
- Does NOT execute code
- Does NOT generate binaries
- ONLY validates structure

---

## Accepted Input
- File extension: `.sierra`

---

## Validation Rules (v0.0)

1. File MUST start with:
   </>Sierra</>

   2. File MUST contain exactly one:
      <main>

      3. File MUST end with:
         </end>

         4. Missing or extra blocks → compilation fails

         ---

         ## Compiler Stages

         Stage 1: Load file  
         Stage 2: Check header  
         Stage 3: Check main block  
         Stage 4: Check end marker  

         If any stage fails → enter debug state.

         ---

         ## Debug Output (on failure)

         //<debug<
         </coderun/>

         ---

         ## Success Output (conceptual)

         Sierra file validated successfully.