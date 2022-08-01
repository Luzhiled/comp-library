---
data:
  _extendedDependsOn:
  - icon: ':warning:'
    path: src/geometry/Z2/operation/square-norm.hpp
    title: src/geometry/Z2/operation/square-norm.hpp
  - icon: ':warning:'
    path: src/geometry/Z2/operation/square.hpp
    title: src/geometry/Z2/operation/square.hpp
  - icon: ':warning:'
    path: src/geometry/Z2/struct/circle.hpp
    title: src/geometry/Z2/struct/circle.hpp
  - icon: ':warning:'
    path: src/geometry/Z2/struct/point.hpp
    title: src/geometry/Z2/struct/point.hpp
  - icon: ':warning:'
    path: src/geometry/Z2/struct/vector.hpp
    title: src/geometry/Z2/struct/vector.hpp
  _extendedRequiredBy:
  - icon: ':warning:'
    path: test/atcoder/abc259_d.cpp
    title: test/atcoder/abc259_d.cpp
  _extendedVerifiedWith: []
  _isVerificationFailed: false
  _pathExtension: hpp
  _verificationStatusIcon: ':warning:'
  attributes:
    links: []
  bundledCode: "#line 2 \"src/geometry/Z2/intersect/is-intersect-circle-circle.hpp\"\
    \n\n#line 2 \"src/geometry/Z2/struct/point.hpp\"\n\n#line 2 \"src/geometry/Z2/struct/vector.hpp\"\
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
    \ namespace Z2\n\n} // namespace luz\n#line 4 \"src/geometry/Z2/struct/point.hpp\"\
    \n\n#line 6 \"src/geometry/Z2/struct/point.hpp\"\n\nnamespace luz {\n \nnamespace\
    \ Z2 {\n\n  template< typename Z >\n  using Point = Vector< Z >;\n\n  template<\
    \ typename Z >\n  using Points = std::vector< Point<Z> >;\n\n} // namespace Z2\n\
    \n} // namespace luz\n\n#line 2 \"src/geometry/Z2/struct/circle.hpp\"\n\n#line\
    \ 4 \"src/geometry/Z2/struct/circle.hpp\"\n\nnamespace luz {\n\nnamespace Z2 {\n\
    \n  template< typename Z >\n  class Circle {\n\n    Point< Z > center_;\n    Z\
    \ r_;\n\n   public:\n    Circle() {}\n    Circle(Point< Z > center, Z r): center_(center),\
    \ r_(r) {}\n\n    Point< Z > center() const {\n      return center_;\n    }\n\n\
    \    Z r() const {\n      return r_;\n    }\n  };\n\n  template< typename Z >\n\
    \  using Circles = std::vector< Circle< Z > >;\n\n} // namespace Z2\n\n} // namespace\
    \ luz\n#line 2 \"src/geometry/Z2/operation/square.hpp\"\n\nnamespace luz {\n\n\
    namespace Z2 {\n\n  template< typename Z >\n  Z square(const Z z) {\n    return\
    \ z * z;\n  }\n\n} // namespace Z2\n\n} // namespace luz\n#line 2 \"src/geometry/Z2/operation/square-norm.hpp\"\
    \n\n#line 5 \"src/geometry/Z2/operation/square-norm.hpp\"\n\nnamespace luz {\n\
    \nnamespace Z2 {\n\n  template< typename Z >\n  Z square_norm(Vector< Z > v) {\n\
    \    return square(v.x()) + square(v.y());\n  }\n\n} // namespace Z2\n\n} // namespace\
    \ luz\n#line 7 \"src/geometry/Z2/intersect/is-intersect-circle-circle.hpp\"\n\n\
    #include <utility>\n\nnamespace luz {\n\nnamespace Z2 {\n\n  template< typename\
    \ Z >\n  bool is_intersect_cc(Circle< Z > c0, Circle< Z > c1) {\n    if (c0.r()\
    \ > c1.r()) std::swap(c0, c1);\n\n    Z sq_dist = square_norm(c0.center() - c1.center());\n\
    \n    if (sq_dist < square(c1.r() - c0.r())) return false;\n    if (square(c1.r()\
    \ + c0.r()) < sq_dist) return false;\n    return true;\n  }\n\n} // namespace\
    \ Z2\n\n} // namespace luz\n"
  code: "#pragma once\n\n#include \"src/geometry/Z2/struct/point.hpp\"\n#include \"\
    src/geometry/Z2/struct/circle.hpp\"\n#include \"src/geometry/Z2/operation/square.hpp\"\
    \n#include \"src/geometry/Z2/operation/square-norm.hpp\"\n\n#include <utility>\n\
    \nnamespace luz {\n\nnamespace Z2 {\n\n  template< typename Z >\n  bool is_intersect_cc(Circle<\
    \ Z > c0, Circle< Z > c1) {\n    if (c0.r() > c1.r()) std::swap(c0, c1);\n\n \
    \   Z sq_dist = square_norm(c0.center() - c1.center());\n\n    if (sq_dist < square(c1.r()\
    \ - c0.r())) return false;\n    if (square(c1.r() + c0.r()) < sq_dist) return\
    \ false;\n    return true;\n  }\n\n} // namespace Z2\n\n} // namespace luz\n"
  dependsOn:
  - src/geometry/Z2/struct/point.hpp
  - src/geometry/Z2/struct/vector.hpp
  - src/geometry/Z2/struct/circle.hpp
  - src/geometry/Z2/operation/square.hpp
  - src/geometry/Z2/operation/square-norm.hpp
  isVerificationFile: false
  path: src/geometry/Z2/intersect/is-intersect-circle-circle.hpp
  requiredBy:
  - test/atcoder/abc259_d.cpp
  timestamp: '2022-07-21 10:58:25+09:00'
  verificationStatus: LIBRARY_NO_TESTS
  verifiedWith: []
documentation_of: src/geometry/Z2/intersect/is-intersect-circle-circle.hpp
layout: document
redirect_from:
- /library/src/geometry/Z2/intersect/is-intersect-circle-circle.hpp
- /library/src/geometry/Z2/intersect/is-intersect-circle-circle.hpp.html
title: src/geometry/Z2/intersect/is-intersect-circle-circle.hpp
---