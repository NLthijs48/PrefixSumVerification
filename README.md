This project is the continueation of my [bachelor thesis project](http://fmt.cs.utwente.nl/education/bachelor/233/). The goal is to verify the Prefix Sum algorithm on two fronts, functional correctness and read/write patterns. The verification is about the OpenCL scalable version of the Prefix Sum algorithm, which will do as much work in parallel as possible.

The used algorithm has two stages, the upsweep and downsweep, of which in the bachelor project only the upsweep was verified in terms of read/write permissions. This project tries to expand this verification to both phases and does functional verification as well.

## Repository contents
- **/Specification:** `.pvl` specification of the algorithm, which can be verified by [VerCors](https://github.com/utwente-fmt/vercors)
- **/Cases:** Encountered problems, for which the creator of the tool Stefan Blom has been asked to investigat, either leading to a tool update or specification change.
- **Permissions and values x8 input.pdf**: Visualization of the permissions of all places in the two-dimensional array used by the algorithm during the execution of the Prefix Sum.
- **Permissions and values x8 input  12s.pdf**: Same as above, but now with extra read permission to another thread to allow for functional verification.
