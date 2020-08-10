# Feature Construction:

Non-linear features are generated in an alternating multi-step process by first applying non-linear transformations\(can be user selected\) to the features \(e.g. log\(x\), √x, 1/x, x2, x3, \|x\|, exp\(x\), 2x, sin\(x\), cos\(x\)\) and then combining them with different operators \(+, −, ·\).

The new features are computed using the **SymPy Python library**, which simplifies the generated mathematical expressions and avoids redundant features. Autofeat creates logical features by allowing the user to specify the units of measurement\(like subtracting weight\(lb\) from distance\(miles\)\) which is implemented using the **Pint Python library** to compute several dimensionless quantities using the **Buckingham π-theorem**.







