---
data:
  _extendedDependsOn:
  - icon: ':heavy_check_mark:'
    path: src/cpp-template/header/type-alias.hpp
    title: src/cpp-template/header/type-alias.hpp
  _extendedRequiredBy:
  - icon: ':heavy_check_mark:'
    path: src/graph/dijkstra.hpp
    title: template
  _extendedVerifiedWith:
  - icon: ':heavy_check_mark:'
    path: test/aoj/grl-1-a.test.cpp
    title: test/aoj/grl-1-a.test.cpp
  _isVerificationFailed: false
  _pathExtension: hpp
  _verificationStatusIcon: ':heavy_check_mark:'
  attributes:
    links: []
  bundledCode: "#line 2 \"src/graph/graph-template.hpp\"\n\n#include <vector>\n\n\
    #line 2 \"src/cpp-template/header/type-alias.hpp\"\n\nnamespace luz {\n\n  using\
    \ isize = std::ptrdiff_t;\n  using usize = std::size_t;\n\n  using i32 = std::int32_t;\n\
    \  using i64 = std::int64_t;\n  using u32 = std::uint32_t;\n  using u64 = std::uint64_t;\n\
    \  \n} // namespace luz\n#line 6 \"src/graph/graph-template.hpp\"\n\nnamespace\
    \ luz {\n\n  template< typename cost_type >\n  class Edge {\n   public:\n    usize\
    \ from, to;\n    cost_type cost;\n    usize id;\n    Edge() = default;\n    Edge(usize\
    \ from_, usize to_, cost_type cost_, usize id_):\n      from(from_), to(to_),\
    \ cost(cost_), id(id_) {}\n  };\n\n  template< typename cost_type >\n  using Edges\
    \ = std::vector< Edge<cost_type> >;\n\n  template< typename cost_type >\n  class\
    \ Graph {\n    std::vector< std::vector<Edge<cost_type>> > g;\n    usize edge_count;\n\
    \n   public:\n    Graph() = default;\n    explicit Graph(usize n): g(n), edge_count(0)\
    \ {}\n\n    usize size() const {\n      return g.size();\n    }\n\n    void add_directed_edge(usize\
    \ from, usize to, cost_type cost = 1) {\n      g[from].emplace_back(from, to,\
    \ cost, edge_count++);\n    }\n\n    void add_undirected_edge(usize u, usize v,\
    \ cost_type cost = 1) {\n      g[u].emplace_back(u, v, cost, edge_count);\n  \
    \    g[v].emplace_back(v, u, cost, edge_count++);\n    }\n\n    inline std::vector<\
    \ Edge<cost_type> > &operator[](const usize &v) {\n      return g[v];\n    }\n\
    \n    inline const std::vector< Edge<cost_type> > &operator[](const usize &v)\
    \ const {\n      return g[v];\n    }\n  };\n\n}\n"
  code: "#pragma once\n\n#include <vector>\n\n#include \"src/cpp-template/header/type-alias.hpp\"\
    \n\nnamespace luz {\n\n  template< typename cost_type >\n  class Edge {\n   public:\n\
    \    usize from, to;\n    cost_type cost;\n    usize id;\n    Edge() = default;\n\
    \    Edge(usize from_, usize to_, cost_type cost_, usize id_):\n      from(from_),\
    \ to(to_), cost(cost_), id(id_) {}\n  };\n\n  template< typename cost_type >\n\
    \  using Edges = std::vector< Edge<cost_type> >;\n\n  template< typename cost_type\
    \ >\n  class Graph {\n    std::vector< std::vector<Edge<cost_type>> > g;\n   \
    \ usize edge_count;\n\n   public:\n    Graph() = default;\n    explicit Graph(usize\
    \ n): g(n), edge_count(0) {}\n\n    usize size() const {\n      return g.size();\n\
    \    }\n\n    void add_directed_edge(usize from, usize to, cost_type cost = 1)\
    \ {\n      g[from].emplace_back(from, to, cost, edge_count++);\n    }\n\n    void\
    \ add_undirected_edge(usize u, usize v, cost_type cost = 1) {\n      g[u].emplace_back(u,\
    \ v, cost, edge_count);\n      g[v].emplace_back(v, u, cost, edge_count++);\n\
    \    }\n\n    inline std::vector< Edge<cost_type> > &operator[](const usize &v)\
    \ {\n      return g[v];\n    }\n\n    inline const std::vector< Edge<cost_type>\
    \ > &operator[](const usize &v) const {\n      return g[v];\n    }\n  };\n\n}\n"
  dependsOn:
  - src/cpp-template/header/type-alias.hpp
  isVerificationFile: false
  path: src/graph/graph-template.hpp
  requiredBy:
  - src/graph/dijkstra.hpp
  timestamp: '2022-06-19 00:20:41+09:00'
  verificationStatus: LIBRARY_ALL_AC
  verifiedWith:
  - test/aoj/grl-1-a.test.cpp
documentation_of: src/graph/graph-template.hpp
layout: document
redirect_from:
- /library/src/graph/graph-template.hpp
- /library/src/graph/graph-template.hpp.html
title: src/graph/graph-template.hpp
---