# Feature Construction:

Non-linear features are generated in an alternating multi-step process by first applying non-linear transformations\(can be user selected\) to the features \(e.g. log\(x\), √x, 1/x, x2, x3, \|x\|, exp\(x\), 2x, sin\(x\), cos\(x\)\) and then combining them with different operators \(+, −, ·\).

The new features are computed using the [**SymPy Python library**](https://www.sympy.org/en/index.html), which simplifies the generated mathematical expressions and avoids redundant features. Autofeat creates logical features by allowing the user to specify the units of measurement\(like subtracting weight\(lb\) from distance\(miles\)\) which is implemented using the [**Pint Python library**](https://pint.readthedocs.io/en/stable/) to compute several dimensionless quantities using the [**Buckingham π-theorem**](https://pint.readthedocs.io/en/0.10.1/pitheorem.html#:~:text=Buckingham%20%CF%80%20theorem%20states%20that,%3D%20n%20%2D%20k%20dimensionless%20parameters.).







