# Sensor context

ADASIND contains original, blurred, single-camera fisheye images, 1080 × 1920 px. The wide circular view shows road users and, in most frames, parts of the camera vehicle/driver at the bottom-left. Mount height, exact camera orientation, intrinsics, extrinsics and timestamps are not supplied here; they must not be inferred from apparent object size.

The lens circle occupies most of the width with black exterior regions near the top/bottom; frame-specific cx/cy/r are in assets/frames.csv. Two lens-border polygons exclude this exterior. Ego contours cover visible host vehicle parts; 006840 and 271039 have no visible ego and their erroneous ego polygons were removed before locking.

The parking task uses a conventional camera image, not ADASIND. The four-camera 50,000-frame exercise is hypothetical. Radial center/mid/edge bins are image positions, not distance or safety-risk bins.

Environment: CVAT 2.75.0 at http://localhost:8100. Set CVAT_URL to this address when rerunning doctor. Offline local-quality is used; no Premium/API-quality equivalence is claimed.
