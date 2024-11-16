I'll restructure the information using tables where appropriate:

### SVD of Jacobian

| Component | Meaning |
|-----------|---------|
| Σ (Sigma) | Singular values showing scaling in principal directions |
| UΣ | U vectors = principal axes of manipulation ellipsoid; Σ = length/scale |
| V | Right singular vectors mapping joint velocities to task space |

**Singularities/Self-motion**:
- Singularities: σ = 0 (loss of mobility)
- Self-motion: null space movements (redundant robots)

### Linear Algebra Concepts

| Concept | Description | When Used |
|---------|-------------|-----------|
| Eigenvectors | Vectors that maintain direction under transformation | System dynamics analysis |
| Singular Matrices | Non-invertible, det = 0 | Identifying loss of rank |
| Left Pseudo-inverse | (A^T A)^-1 A^T | Overdetermined systems |
| Right Pseudo-inverse | A^T (A A^T)^-1 | Underdetermined systems |

**Rank and Null Space**:
| Term | Definition |
|------|------------|
| Rank | Number of linearly independent columns/rows |
| Null Space | Vectors that map to zero |
| Relationship | Nullity + Rank = column count |

### Path Planning

| Method | Key Features |
|--------|-------------|
| Error Measures | - Cartesian error<br>- Joint space error<br>- Task-specific metrics |
| Jacobian-based IK | - Uses J^+ (pseudo-inverse)<br>- qdot = J^+ * xdot |
| QP Planning | - Minimizes objective function<br>- Handles constraints<br>- Multi-priority capable |

### PID Control

| Parameter | Formula Term | Effect When Increased |
|-----------|-------------|----------------------|
| Kp | Kp*e(t) | Faster response, more overshoot |
| Ki | Ki∫e(t)dt | Eliminates steady-state error, adds oscillation |
| Kd | Kd*de(t)/dt | More damping, reduces overshoot, amplifies noise |

### Camera Parameters

**Intrinsic Parameters**:
| Parameter | Description |
|-----------|-------------|
| fx, fy | Focal lengths |
| cx, cy | Principal point |
| s | Skew coefficient |

**Distortion Coefficients**:
| Type | Parameters |
|------|------------|
| Radial | k1, k2, k3 |
| Tangential | p1, p2 |

**Calibration Requirements**:
| Task | Minimum Points Required |
|------|------------------------|
| Essential Matrix | 6 points |
| Fundamental Matrix | 8+ points |
| Full Calibration | Multiple views of pattern |

### Robot with Camera

**PBVS Concerns**:
| Concern | Impact |
|---------|---------|
| Occlusion | Loss of visual features |
| Local Minima | Trapped in suboptimal solution |
| Feature Tracking | Reliability issues |
| Calibration Errors | Reduced accuracy |

**Calibration Reasons**:
| Reason | Benefit |
|--------|---------|
| Visual Servoing | Improved accuracy |
| Manipulation | Better precision |
| Coordinate Transform | Accurate camera-to-robot mapping |
| Mount Compensation | Corrects installation errors |

Path and Trajectory Generation components are more process-oriented and don't fit well in a table format, but for completeness:

**Straight Line Paths**:
- Linear interpolation in joint space
- Higher-order polynomials for smoothness
- May not be straight in Cartesian space

**Obstacle Avoidance Methods**:
- Potential field approaches
- Sampling-based (RRT, PRM)
- Optimization with collision constraints
