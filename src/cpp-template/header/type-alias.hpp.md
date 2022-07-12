---
data:
  _extendedDependsOn: []
  _extendedRequiredBy:
  - icon: ':heavy_check_mark:'
    path: src/cpp-template/header/input.hpp
    title: src/cpp-template/header/input.hpp
  - icon: ':heavy_check_mark:'
    path: src/cpp-template/header/template-header.hpp
    title: src/cpp-template/header/template-header.hpp
  - icon: ':warning:'
    path: src/cpp-template/template.cpp
    title: template
  - icon: ':heavy_check_mark:'
    path: src/graph/dijkstra.hpp
    title: template
  - icon: ':heavy_check_mark:'
    path: src/graph/graph-template.hpp
    title: src/graph/graph-template.hpp
  - icon: ':heavy_check_mark:'
    path: src/sequence/coordinate-compression.hpp
    title: src/sequence/coordinate-compression.hpp
  _extendedVerifiedWith:
  - icon: ':heavy_check_mark:'
    path: test/aoj/grl-1-a.test.cpp
    title: test/aoj/grl-1-a.test.cpp
  - icon: ':heavy_check_mark:'
    path: test/aoj/itp1-1-a.test.cpp
    title: test/aoj/itp1-1-a.test.cpp
  - icon: ':heavy_check_mark:'
    path: unit-test/sequence/coordinate-complession.test.cpp
    title: unit-test/sequence/coordinate-complession.test.cpp
  _isVerificationFailed: false
  _pathExtension: hpp
  _verificationStatusIcon: ':heavy_check_mark:'
  attributes:
    links: []
  bundledCode: "#line 2 \"src/cpp-template/header/type-alias.hpp\"\n\nnamespace luz\
    \ {\n\n  using isize = std::ptrdiff_t;\n  using usize = std::size_t;\n\n  using\
    \ i32 = std::int32_t;\n  using i64 = std::int64_t;\n  using u32 = std::uint32_t;\n\
    \  using u64 = std::uint64_t;\n  \n} // namespace luz\n"
  code: "#pragma once\n\nnamespace luz {\n\n  using isize = std::ptrdiff_t;\n  using\
    \ usize = std::size_t;\n\n  using i32 = std::int32_t;\n  using i64 = std::int64_t;\n\
    \  using u32 = std::uint32_t;\n  using u64 = std::uint64_t;\n  \n} // namespace\
    \ luz\n"
  dependsOn: []
  isVerificationFile: false
  path: src/cpp-template/header/type-alias.hpp
  requiredBy:
  - src/graph/dijkstra.hpp
  - src/graph/graph-template.hpp
  - src/cpp-template/template.cpp
  - src/cpp-template/header/template-header.hpp
  - src/cpp-template/header/input.hpp
  - src/sequence/coordinate-compression.hpp
  timestamp: '2022-06-13 01:05:23+09:00'
  verificationStatus: LIBRARY_ALL_AC
  verifiedWith:
  - unit-test/sequence/coordinate-complession.test.cpp
  - test/aoj/itp1-1-a.test.cpp
  - test/aoj/grl-1-a.test.cpp
documentation_of: src/cpp-template/header/type-alias.hpp
layout: document
redirect_from:
- /library/src/cpp-template/header/type-alias.hpp
- /library/src/cpp-template/header/type-alias.hpp.html
title: src/cpp-template/header/type-alias.hpp
---