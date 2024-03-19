# Calculate 3D polygon area

Calculate3DPolygonArea provides a header-only solution for efficiently computing the area of non-complex polygons in 3D space. This template-based solution is designed to be self-contained, requiring only the inclusion of <vector> from the standard library.

*This repository expands the functionality of the [Triangulate3DPolygon](https://github.com/StefanJohnsen/Triangulate3DPolygon) repository by incorporating the ability to calculate polygon area* 

### Supported polygons
The solution works for all kinds of 3D non-complex polygons, concave or convex, open or closed.

### OS Support
- Windows
- Linux
- macOS

## Solution
By utilizing the process of triangulation, the area of a polygon is computed by breaking it down into triangles and then summing the areas of these individual components.

## Usage
Copy `TriangulatePolygonEx.h` to your project and include the file.

```cpp
#include <iostream>
#include "TriangulatePolygonEx.h"

int main()
{
  std::vector<triangulate::Point> polygon;

  polygon.emplace_back(0.0f, 0.0f, 0.0f);
  polygon.emplace_back(2.0f, 0.0f, 0.0f);
  polygon.emplace_back(2.0f, 2.0f, 0.0f);
  polygon.emplace_back(0.0f, 2.0f, 0.0f);

  const auto area = calculatePolygonArea(polygon);

  std::cout << "Area " << area << std::endl;
}
```
<br>

## License
This software is released under the MIT License terms.
