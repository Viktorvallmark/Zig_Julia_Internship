# 🚀 30-Day Zig + Julia Hybrid Roadmap  
**Goal:** Master systems programming (Zig) + numerical HPC (Julia) for ARM GPU internship.  
**User Background:** Dual Bachelor’s (Numerics + Computer Engineering), targeting ARM GPU algorithms.  

## Phase 1: Foundations (Days 1-10)  
| Day | Focus          | Zig Tasks                                                                 | Julia Tasks                                                               |  
|-----|----------------|---------------------------------------------------------------------------|---------------------------------------------------------------------------|  
| 1   | Setup          | Install Zig, `hello_world`, `build.zig`                                   | Install Julia, VS Code setup, REPL basics                                |  
| 2   | Core Syntax    | Structs, pointers, error handling (`!T`)                                  | Types, structs, multiple dispatch                                        |  
| 3   | Memory Control | Stack/heap, arena allocators                                              | Preallocation (`Vector{Float64}(undef, N)`), `@views`                    |  
| 4   | Data Design    | Struct-of-Arrays (SoA), packed structs                                    | SoA patterns, `StructArrays.jl`                                          |  
| 5   | Interop I/O    | Read/write binary files, C ABI basics                                     | File I/O (HDF5.jl), `ccall` to C                                         |  
| 6   | **Project 1**  | Particle struct (x,y,vx,vy) with binary serialization                     | Read Zig’s binary file, visualize with `Plots.jl`                         |  
| 7   | Performance    | Benchmark with `std.time`, SIMD (`@Vector`)                               | `@btime` (BenchmarkTools), `@inbounds`, `@simd`                          |  
| 8   | Fortran Interop| Call BLAS from Zig (`libblas.so`)                                         | Benchmark same BLAS call in Julia                                         |  
| 9   | GPU Awareness  | Study ARM Mali architecture                                               | GPU basics: `CUDA.jl` array ops                                          |  
| 10  | **Project 2**  | Offload dot product to BLAS (Zig)                                         | Compare to Julia’s `dot()` and `CUDA.jl`                                 |  

## Phase 2: Specialization (Days 11-20)  
| Day | Focus          | Zig Tasks                                                                 | Julia Tasks                                                               |  
|-----|----------------|---------------------------------------------------------------------------|---------------------------------------------------------------------------|  
| 11  | Parallelism    | `std.Thread`, mutexes                                                     | `Threads.@threads` for loops                                             |  
| 12  | GPU Prep       | ARM GPU: OpenCL/Vulkan intro                                              | `KernelAbstractions.jl` (vendor-neutral GPU)                             |  
| 13  | **Project 3**  | Threaded particle update (Zig)                                            | Same in Julia, benchmark scaling                                         |  
| 14  | Embedded       | Cross-compile for ARM Cortex-M (QEMU)                                     | (N/A)                                                                     |  
| 15  | Numerics       | Finite difference solver (1D heat)                                        | Same solver in Julia                                                      |  
| 16  | Interop Deep   | Expose Zig kernel as `libzigkernel.so`                                    | Call Zig kernel from Julia via `ccall`                                   |  
| 17  | Optimization   | Profile with `perf`, optimize cache misses                                | Profile with `ProfileView.jl`                                            |  
| 18  | **Project 4**  | Hybrid 1D heat solver: Zig (compute) + Julia (plotting)                   | Benchmark vs. pure Julia                                                 |  
| 19  | GPU Acceleration| OpenCL kernel in Zig (vector add)                                         | Port to Julia via `KernelAbstractions.jl`                                |  
| 20  | Debugging      | Zig debugger (lldb/vscode)                                                | Debugging (Debugger.jl)                                                  |  

## Phase 3: Integration & Internship Prep (Days 21-30)  
| Day | Focus          | Task                                                                      |  
|-----|----------------|---------------------------------------------------------------------------|  
| 21  | ARM GPU        | Study ARM Compute Library: convolution, FFT                              |  
| 22  | **Final Start**| Begin CFD simulator: Zig (collision) + Julia (advection)                 |  
| 23  | GPU Offload    | Zig OpenCL kernel for fluid forces                                       |  
| 24  | Julia Orchestration| Call Zig’s kernel from Julia, handle data I/O                           |  
| 25  | Visualization  | Render fluid flow with `Makie.jl`                                        |  
| 26  | Optimization   | Profile data transfers (Zig⇄Julia⇄GPU)                                   |  
| 27  | Embedded HPC   | Cross-compile Zig kernel for Raspberry Pi                                |  
| 28  | Documentation  | Write README explaining design tradeoffs                                 |  
| 29  | Performance    | Benchmark on ARM CPU vs. x86, analyze GPU bottlenecks                    |  
| 30  | **Portfolio**  | Publish on GitHub: CFD simulator, BLAS interop, ARM benchmarks           |  

## 🔑 Key Deliverables  
1. **Hybrid CFD Simulator**  
   - Zig: High-performance collision kernel (SoA/SIMD).  
   - Julia: GPU-accelerated advection + visualization.  
2. **ARM GPU Readiness**  
   - OpenCL experience (Zig + Julia).  
   - ARM vs. x86 performance report.  
3. **GitHub Portfolio**  
   - Hybrid projects with benchmarks.  

## 📚 Resources  
- **Zig:** [ziglearn.org](https://ziglearn.org/), [Zig Stdlib](https://ziglang.org/documentation/master/)  
- **Julia:** [Julia Docs](https://docs.julialang.org/), [Julia HPC Course](https://github.com/mitmath/18337)  
- **ARM GPU:** [Mali Developer Hub](https://developer.arm.com/Processors/Mali-GPU), [ARM OpenCL Guide](https://arm-software.github.io/ComputeLibrary/latest/)  
- **Interop Example:** [Zig-Julia Demo](https://github.com/ziglang/zig/wiki/How-to-call-Zig-code-from-Julia)  
