# Supported WASM And WASI Proposals

## WebAssembly proposals

WasmEdge supports the following [WebAssembly proposals](https://github.com/WebAssembly/proposals). Those proposals are likely to become official WebAssembly specifications in the future.

| Proposal                                  | WasmEdge CLI flag                     | WasmEdge C API enumeration                       | Default turning on | Interpreter mode   | AOT mode           |
| ----------------------------------------- | ------------------------------------- | ------------------------------------------------ | ------------------ | ------------------ | ------------------ |
| [Import/Export of Mutable Globals][]      | `--disable-import-export-mut-globals` | `WasmEdge_Proposal_ImportExportMutGlobals`       | ✓ (after `0.8.2`)  | ✓                  | ✓                  |
| [Non-trapping float-to-int conversions][] | `--disable-non-trap-float-to-int`     | `WasmEdge_Proposal_NonTrapFloatToIntConversions` | ✓ (after `0.8.2`)  | ✓                  | ✓                  |
| [Sign-extension operators][]              | `--disable-sign-extension-operators`  | `WasmEdge_Proposal_SignExtensionOperators`       | ✓ (after `0.8.2`)  | ✓                  | ✓                  |
| [Multi-value][]                           | `--disable-multi-value`               | `WasmEdge_Proposal_MultiValue`                   | ✓ (after `0.8.2`)  | ✓                  | ✓                  |
| [Reference Types][]                       | `--disable-reference-types`           | `WasmEdge_Proposal_ReferenceTypes`               | ✓ (after `0.8.2`)  | ✓                  | ✓                  |
| [Bulk memory operations][]                | `--disable-bulk-memory`               | `WasmEdge_Proposal_BulkMemoryOperations`         | ✓ (after `0.8.2`)  | ✓                  | ✓                  |
| [Fixed-width SIMD][]                      | `--disable-simd`                      | `WasmEdge_Proposal_SIMD`                         | ✓ (after `0.9.0`)  | ✓ (after `0.8.2`)  | ✓ (after `0.8.2`)  |
| [Tail call][]                             | `--enable-tail-call`                  | `WasmEdge_Proposal_TailCall`                     |                    | ✓ (after `0.10.0`) | ✓ (after `0.10.0`) |
| [Multiple memories][]                     | `--enable-multi-memory`               | `WasmEdge_Proposal_MultiMemories`                |                    | ✓ (after `0.9.1`)  | ✓ (after `0.9.1`)  |
| [Extended Constant Expressions][]         | `--enable-extended-const`             | `WasmEdge_Proposal_ExtendedConst`                |                    | ✓ (after `0.10.0`) | ✓ (after `0.10.0`) |
| [Threads][]                               | `--enable-threads`                    | `WasmEdge_Proposal_Threads`                      |                    | ✓ (after `0.10.1`) | ✓ (after `0.10.1`) |

The following proposals is under development and may be supported in the future:

* [Component Model][]
* [Exception handling][]
* [Garbage collection][]
* [WebAssembly C and C++ API][]

[Import/Export of Mutable Globals]: https://github.com/WebAssembly/mutable-global
[Non-trapping float-to-int conversions]: https://github.com/WebAssembly/nontrapping-float-to-int-conversions
[Sign-extension operators]: https://github.com/WebAssembly/sign-extension-ops
[Multi-value]: https://github.com/WebAssembly/multi-value
[Reference Types]: https://github.com/WebAssembly/reference-types
[Bulk memory operations]: https://github.com/WebAssembly/bulk-memory-operations
[Fixed-width SIMD]: https://github.com/webassembly/simd
[Tail call]: https://github.com/WebAssembly/tail-call
[Multiple memories]: https://github.com/WebAssembly/multi-memory
[Extended Constant Expressions]: https://github.com/WebAssembly/extended-const
[Threads]: https://github.com/webassembly/threads
[Component Model]: https://github.com/WebAssembly/component-model
[Exception handling]: https://github.com/WebAssembly/exception-handling
[Garbage collection]: https://github.com/WebAssembly/gc
[WebAssembly C and C++ API]: https://github.com/WebAssembly/wasm-c-api

## WASI proposals

WasmEdge implements the following [WASI proposals](https://github.com/WebAssembly/WASI/blob/main/Proposals.md).

| Proposal                       | Platforms                         |
| ------------------------------ | --------------------------------- |
| [Sockets][]                    |                                   |
| [Crypto][]                     | `x86_64 Linux`, `aarch64 Linux`   |
| [Machine Learning (wasi-nn)][] | `x86_64 Linux (OpenVINO backend)` |
| [proxy-wasm][]                 | `x86_64 Linux (Interpreter only)` |

The following proposals is under development and may be supported in the future:

* PyTorch backend of `WASI-NN`
* TensorFlow backend of `WASI-NN`
* TensorFlow-Lite backend of `WASI-NN`

[Sockets]: https://github.com/WebAssembly/wasi-sockets
[Crypto]: https://github.com/WebAssembly/wasi-crypto
[Machine Learning (wasi-nn)]: https://github.com/WebAssembly/wasi-nn
[proxy-wasm]: https://github.com/proxy-wasm/spec
