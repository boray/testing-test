# Mina zkApp: Testing Test

This template uses TypeScript.

## UPDATE PATHS
```sh
cd ~/o1js
git switch boray/o1js-testing
GIT_LFS_SKIP_SMUDGE=1 git submodule update --recursive
rm -rf node_modules
npm i
npm run prepublishOnly
npm run pack
cd src/testing
rm -rf node_modules
npm i
npm run prepublishOnly
npm run pack
cd ~/testing-test
npm i
npm run build
node build/src/main.js
```

## Error
```
/workspace_root/src/bindings/ocaml/jsoo_exports/overrides.js:45
    if (err instanceof Error) throw err;
                              ^


RuntimeError: unreachable
    at plonk_wasm.wasm.__rust_start_panic (wasm://wasm/plonk_wasm.wasm-01244c7e:wasm-function[5427]:0x407584)
    at plonk_wasm.wasm.rust_panic (wasm://wasm/plonk_wasm.wasm-01244c7e:wasm-function[5203]:0x406b70)
    at plonk_wasm.wasm.std::panicking::rust_panic_with_hook::ha73c2fe1713e4696 (wasm://wasm/plonk_wasm.wasm-01244c7e:wasm-function[3779]:0x3d86dc)
    at plonk_wasm.wasm.std::panicking::begin_panic_handler::{{closure}}::h9e77d444621bd93e (wasm://wasm/plonk_wasm.wasm-01244c7e:wasm-function[4396]:0x3f6f49)
    at plonk_wasm.wasm.std::sys_common::backtrace::__rust_end_short_backtrace::h80934746fe83690e (wasm://wasm/plonk_wasm.wasm-01244c7e:wasm-function[5384]:0x407468)
    at plonk_wasm.wasm.rust_begin_unwind (wasm://wasm/plonk_wasm.wasm-01244c7e:wasm-function[4747]:0x40169c)
    at plonk_wasm.wasm.core::panicking::panic_fmt::h9d08be0ad7c0117f (wasm://wasm/plonk_wasm.wasm-01244c7e:wasm-function[4772]:0x401e72)
    at plonk_wasm.wasm.core::panicking::panic::h10b544eae59fd39a (wasm://wasm/plonk_wasm.wasm-01244c7e:wasm-function[4841]:0x4031e4)
    at plonk_wasm.wasm.core::option::unwrap_failed::h078445c648fca33c (wasm://wasm/plonk_wasm.wasm-01244c7e:wasm-function[5207]:0x406bae)
    at plonk_wasm.wasm.caml_fq_srs_create_parallel (wasm://wasm/plonk_wasm.wasm-01244c7e:wasm-function[4600]:0x3fdd02)
    at module.exports.caml_fq_srs_create_parallel (/Users/boraysaygilier/Code/o1labs/o1js-bigint/node_modules/o1js/dist/node/bindings/compiled/_node_bindings/plonk_wasm.cjs:811:22)
    at createSrs (/Users/boraysaygilier/Code/o1labs/o1js-bigint/node_modules/o1js/src/bindings/crypto/bindings/srs.ts:75:71)
    at create (/Users/boraysaygilier/Code/o1labs/o1js-bigint/node_modules/o1js/src/bindings/crypto/bindings/srs.ts:102:17)
    at _c7j_ (/Users/boraysaygilier/Code/o1labs/o1js-bigint/node_modules/o1js/dist/node/bindings/compiled/_node_bindings/o1js_node.bc.cjs:311007:53)
    at caml_call1 (/Users/boraysaygilier/Code/o1labs/o1js-bigint/node_modules/o1js/dist/node/bindings/compiled/_node_bindings/o1js_node.bc.cjs:6807:28)
    at load (/workspace_root/src/mina/src/lib/crypto/kimchi_backend/common/dlog_plonk_based_keypair.ml:158:27)
    at caml_call1 (/Users/boraysaygilier/Code/o1labs/o1js-bigint/node_modules/o1js/dist/node/bindings/compiled/_node_bindings/o1js_node.bc.cjs:6807:28)
    at _itk_ (/workspace_root/src/mina/src/lib/pickles/step_main.ml:393:19)
    at <anonymous> (/workspace_root/src/mina/src/lib/promise/js/promise.js:25:37)

Node.js v23.11.0
```
