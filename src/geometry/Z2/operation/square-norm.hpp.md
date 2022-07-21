---
data:
  _extendedDependsOn:
  - icon: ':x:'
    path: src/geometry/Z2/operation/square.hpp
    title: src/geometry/Z2/operation/square.hpp
  - icon: ':x:'
    path: src/geometry/Z2/struct/vector.hpp
    title: src/geometry/Z2/struct/vector.hpp
  _extendedRequiredBy:
  - icon: ':x:'
    path: src/geometry/Z2/intersect/is-intersect-circle-circle.hpp
    title: src/geometry/Z2/intersect/is-intersect-circle-circle.hpp
  - icon: ':x:'
    path: src/geometry/Z2/intersect/is-intersect-point-circle.hpp
    title: src/geometry/Z2/intersect/is-intersect-point-circle.hpp
  _extendedVerifiedWith:
  - icon: ':x:'
    path: test/atcoder/abc259_d.test.cpp
    title: test/atcoder/abc259_d.test.cpp
  _isVerificationFailed: true
  _pathExtension: hpp
  _verificationStatusIcon: ':x:'
  attributes:
    links: []
  bundledCode: "#line 2 \"src/geometry/Z2/operation/square-norm.hpp\"\n\n#line 2 \"\
    src/geometry/Z2/operation/square.hpp\"\n\nnamespace luz {\n\nnamespace Z2 {\n\n\
    \  template< typename Z >\n  Z square(const Z z) {\n    return z * z;\n  }\n\n\
    } // namespace Z2\n\n} // namespace luz\n#line 2 \"src/geometry/Z2/struct/vector.hpp\"\
    \n\n#include <vector>\n\nnamespace luz {\n\nnamespace Z2 {\n\n  template< typename\
    \ Z >\n  class Vector {\n\n    Z x_, y_;\n\n   public:\n    Vector() {}\n    Vector(Z\
    \ x, Z y): x_(x), y_(y) {}\n\n    bool operator==(const Vector &v) const {\n \
    \     return x_ == v.x_ and y_ == v.y_;\n    }\n\n    bool operator!=(const Vector\
    \ &v) const {\n      return x_ == v.x_ or  y_ == v.y_;\n    }\n\n    Vector &operator+=(const\
    \ Vector &v) {\n      x_ += v.x_; y_ += v.y_;\n      return *this;\n    }\n\n\
    \    Vector &operator-=(const Vector &v) {\n      x_ -= v.x_; y_ -= v.y_;\n  \
    \    return *this;\n    }\n\n    Vector operator+(const Vector &v) const {\n \
    \     return Vector(*this) += v;\n    }\n\n    Vector operator-(const Vector &v)\
    \ const {\n      return Vector(*this) -= v;\n    }\n\n    Z x() const {\n    \
    \  return x_;\n    }\n\n    Z y() const {\n      return y_;\n    }\n\n  };\n\n\
    \  template< typename Z >\n  using Vectors = std::vector< Vector<Z> >;\n\n} //\
    \ namespace Z2\n\n} // namespace luz\n#line 5 \"src/geometry/Z2/operation/square-norm.hpp\"\
    \n\nnamespace luz {\n\nnamespace Z2 {\n\n  template< typename Z >\n  Z square_norm(Vector<\
    \ Z > v) {\n    return square(v.x()) + square(v.y());\n  }\n\n} // namespace Z2\n\
    \n} // namespace luz\n"
  code: "#pragma once\n\n#include \"src/geometry/Z2/operation/square.hpp\"\n#include\
    \ \"src/geometry/Z2/struct/vector.hpp\"\n\nnamespace luz {\n\nnamespace Z2 {\n\
    \n  template< typename Z >\n  Z square_norm(Vector< Z > v) {\n    return square(v.x())\
    \ + square(v.y());\n  }\n\n} // namespace Z2\n\n} // namespace luz\n"
  dependsOn:
  - src/geometry/Z2/operation/square.hpp
  - src/geometry/Z2/struct/vector.hpp
  isVerificationFile: false
  path: src/geometry/Z2/operation/square-norm.hpp
  requiredBy:
  - src/geometry/Z2/intersect/is-intersect-circle-circle.hpp
  - src/geometry/Z2/intersect/is-intersect-point-circle.hpp
  timestamp: '2022-07-21 10:58:25+09:00'
  verificationStatus: LIBRARY_ALL_WA
  verifiedWith:
  - test/atcoder/abc259_d.test.cpp
documentation_of: src/geometry/Z2/operation/square-norm.hpp
layout: document
redirect_from:
- /library/src/geometry/Z2/operation/square-norm.hpp
- /library/src/geometry/Z2/operation/square-norm.hpp.html
title: src/geometry/Z2/operation/square-norm.hpp
---