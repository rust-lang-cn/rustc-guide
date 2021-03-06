<!--
# Summary
-->

# 概览

<!--
[About this guide](./about-this-guide.md)
-->

[关于本指南](./about-this-guide.md)

---

<!--
- [Part 1: Building, debugging, and contributing to Rustc](./part-1-intro.md)
    - [About the compiler team](./compiler-team.md)
    - [How to Build and Run the Compiler](./how-to-build-and-run.md)
        - [Build and Install distribution artifacts](./build-install-distribution-artifacts.md)
        - [Documenting Compiler](./compiler-documenting.md)
    - [The compiler testing framework](./tests/intro.md)
        - [Running tests](./tests/running.md)
        - [Adding new tests](./tests/adding.md)
        - [Using `compiletest` + commands to control test execution](./compiletest.md)
    - [Walkthrough: a typical contribution](./walkthrough.md)
    - [Implementing new features](./implementing_new_features.md)
    - [Stabilizing Features](./stabilization_guide.md)
    - [Debugging the Compiler](./compiler-debugging.md)
    - [Profiling the compiler](./profiling.md)
        - [with the linux perf tool](./profiling/with_perf.md)
    - [Coding conventions](./conventions.md)
    - [crates.io Dependencies](./crates-io.md)
    - [Emitting Errors and other Diagnostics](diagnostics.md)
        - [JSON diagnostic format](diagnostics/json-format.md)
- [Part 2: How rustc works](./part-2-intro.md)
    - [High-level overview of the compiler source](./high-level-overview.md)
    - [The Rustc Driver and Interface](./rustc-driver.md)
        - [Rustdoc](./rustdoc.md)
    - [Queries: demand-driven compilation](./query.md)
        - [The Query Evaluation Model in Detail](./queries/query-evaluation-model-in-detail.md)
        - [Incremental compilation](./queries/incremental-compilation.md)
        - [Incremental compilation In Detail](./queries/incremental-compilation-in-detail.md)
        - [Debugging and Testing](./incrcomp-debugging.md)
    - [The parser](./the-parser.md)
    - [`#[test]` Implementation](./test-implementation.md)
    - [Macro expansion](./macro-expansion.md)
    - [Name resolution](./name-resolution.md)
    - [The HIR (High-level IR)](./hir.md)
        - [Lowering AST to HIR](./lowering.md)
        - [Debugging](./hir-debugging.md)
    - [The `ty` module: representing types](./ty.md)
    - [Kinds](./kinds.md)
    - [Type inference](./type-inference.md)
    - [Trait solving (old-style)](./traits/resolution.md)
        - [Higher-ranked trait bounds](./traits/hrtb.md)
        - [Caching subtleties](./traits/caching.md)
        - [Specialization](./traits/specialization.md)
    - [Trait solving (new-style)](./traits/index.md)
        - [Lowering to logic](./traits/lowering-to-logic.md)
            - [Goals and clauses](./traits/goals-and-clauses.md)
            - [Equality and associated types](./traits/associated-types.md)
            - [Implied bounds](./traits/implied-bounds.md)
            - [Region constraints](./traits/regions.md)
            - [The lowering module in rustc](./traits/lowering-module.md)
            - [Lowering rules](./traits/lowering-rules.md)
            - [Well-formedness checking](./traits/wf.md)
        - [Canonical queries](./traits/canonical-queries.md)
            - [Canonicalization](./traits/canonicalization.md)
        - [The SLG solver](./traits/slg.md)
        - [An Overview of Chalk](./traits/chalk-overview.md)
        - [Bibliography](./traits/bibliography.md)
    - [Type checking](./type-checking.md)
        - [Method Lookup](./method-lookup.md)
        - [Variance](./variance.md)
        - [Existential Types](./existential-types.md)
    - [The MIR (Mid-level IR)](./mir/index.md)
        - [MIR construction](./mir/construction.md)
        - [MIR visitor and traversal](./mir/visitor.md)
        - [MIR passes: getting the MIR for a function](./mir/passes.md)
        - [MIR optimizations](./mir/optimizations.md)
        - [Debugging](./mir/debugging.md)
    - [The borrow checker](./borrow_check.md)
        - [Tracking moves and initialization](./borrow_check/moves_and_initialization.md)
            - [Move paths](./borrow_check/moves_and_initialization/move_paths.md)
        - [MIR type checker](./borrow_check/type_check.md)
        - [Region inference](./borrow_check/region_inference.md)
        - [Two-phase-borrows](./borrow_check/two_phase_borrows.md)
    - [Constant evaluation](./const-eval.md)
        - [miri const evaluator](./miri.md)
    - [Parameter Environments](./param_env.md)
    - [Code Generation](./codegen.md)
        - [Updating LLVM](./codegen/updating-llvm.md)
        - [Debugging LLVM](./codegen/debugging.md)
    - [Profile-guided Optimization](./profile-guided-optimization.md)
-->

- [第一部分：rustc 的构建、调试与贡献](./part-1-intro.md)
    - [关于编译器团队](./compiler-team.md)
    - [如何构建并运行编译器](./how-to-build-and-run.md)
        - [构建并安装发行版工件](./build-install-distribution-artifacts.md)
        - [构建编译器文档](./compiler-documenting.md)
    - [编译器测试框架](./tests/intro.md)
        - [运行测试](./tests/running.md)
        - [添加新测试](./tests/adding.md)
        - [使用 `compiletest` + 命令来控制测试执行](./compiletest.md)
    - [攻略：一次典型的贡献](./walkthrough.md)
    - [实现新特性](./implementing_new_features.md)
    - [稳定化特性](./stabilization_guide.md)
    - [调试编译器](./compiler-debugging.md)
    - [剖析编译器性能](./profiling.md)
        - [使用 linux perf 工具剖析](./profiling/with_perf.md)
    - [编码约定](./conventions.md)
    - [crates.io 依赖](./crates-io.md)
    - [消除错误和其它诊断报告](diagnostics.md)
        - [JSON 诊断报告格式](diagnostics/json-format.md)
- [第二部分：rustc 的工作原理](./part-2-intro.md)
    - [编译器源码概览](./high-level-overview.md)
    - [rustc 驱动与接口](./rustc-driver.md)
        - [rustdoc](./rustdoc.md)
    - [查询：需求驱动的编译](./query.md)
        - [查询求值模型详解](./queries/query-evaluation-model-in-detail.md)
        - [增量编译](./queries/incremental-compilation.md)
        - [增量编译详解](./queries/incremental-compilation-in-detail.md)
        - [调试与测试](./incrcomp-debugging.md)
    - [解析器](./the-parser.md)
    - [`#[test]` 实现](./test-implementation.md)
    - [宏展开](./macro-expansion.md)
    - [名字求解](./name-resolution.md)
    - [HIR（上层 IR）](./hir.md)
        - [将 AST 降低为 HIR](./lowering.md)
        - [调试](./hir-debugging.md)
    - [`ty` 模块：类型的表示](./ty.md)
    - [种类](./kinds.md)
    - [类型推导](./type-inference.md)
    - [Trait 解算（旧式风格）](./traits/resolution.md)
        - [高阶 trait 绑定](./traits/hrtb.md)
        - [缓存的细节](./traits/caching.md)
        - [特化](./traits/specialization.md)
    - [Trait 解算（新式风格）](./traits/index.md)
        - [降低到逻辑层面](./traits/lowering-to-logic.md)
            - [目标与已知](./traits/goals-and-clauses.md)
            - [相等性与惯量类型](./traits/associated-types.md)
            - [隐式界定](./traits/implied-bounds.md)
            - [生存期约束](./traits/regions.md)
            - [rustc 中的 lowering 模块](./traits/lowering-module.md)
            - [降低规则](./traits/lowering-rules.md)
            - [良构性检查](./traits/wf.md)
        - [典范查询](./traits/canonical-queries.md)
            - [典范化](./traits/canonicalization.md)
        - [SLG 解算器](./traits/slg.md)
        - [Chalk 概览](./traits/chalk-overview.md)
        - [文献](./traits/bibliography.md)
    - [类型检查](./type-checking.md)
        - [方法的查找](./method-lookup.md)
        - [型变](./variance.md)
        - [存在类型](./existential-types.md)
    - [MIR（中层 IR）](./mir/index.md)
        - [MIR 的构造](./mir/construction.md)
        - [MIR 访问器与遍历](./mir/visitor.md)
        - [MIR 趟：获取函数的 MIRn](./mir/passes.md)
        - [MIR 优化](./mir/optimizations.md)
        - [调试](./mir/debugging.md)
    - [借用检查器](./borrow_check.md)
        - [跟踪转移和初始化](./borrow_check/moves_and_initialization.md)
            - [转移路径](./borrow_check/moves_and_initialization/move_paths.md)
        - [MIR 类型检查器](./borrow_check/type_check.md)
        - [生存域推导](./borrow_check/region_inference.md)
        - [两阶段借用](./borrow_check/two_phase_borrows.md)
    - [常量求值](./const-eval.md)
        - [miri const 求值器](./miri.md)
    - [形参环境](./param_env.md)
    - [代码生成](./codegen.md)
        - [更新 LLVM](./codegen/updating-llvm.md)
        - [调试 LLVM](./codegen/debugging.md)
    - [性能剖析指导的优化](./profile-guided-optimization.md)

---

[附录 A：傻瓜分析](./appendix/stupid-stats.md)
[附录 B：背景材料](./appendix/background.md)
[附录 C：术语表](./appendix/glossary.md)
[附录 D：代码索引](./appendix/code-index.md)
[](./important-links.md)
