Fibers 3D object-store validation — 2026-10-29

Tested code: 65433d8cfc62b3db7f758647ce00799c0bddafe9
Base: ScrollPrize/villa 8ff06f7620dcb663ed327028dbb8a0cf7e9a8198

macOS arm64, Qt 6.11.2, LLVM Clang 22.1.8, CMake QuickBuild (-O1).
The full VC3D application compiled. All nine selected suites passed; OpenGL rendering was exercised.
The manifest test uses TMPDIR=/private/tmp to avoid macOS /var versus /private/var symlink spelling in its path-equality assertion.

Real source: Paris4_1mm_v2_crop_Z4000.afv, 364,708 fibers.
Sample per H/V family: 256 longest plus the first 512 IDs divisible by 257, deduplicated.
1,533 fibers (767 H, 766 V), 359,356 points imported through the standard v4 collection importer.
No coordinate conversion. Every displayed binary64 coordinate compared equal to its source JSON coordinate.
CT: PHercParis4/20230205180739, 7.91 micrometers.
The isolated object store was opened in the actual VC3D app. A Qt integration probe exercised H/V filtering, selection, clear, Main CT ribbon, and the collection-controller open-in-Line-Annotation path with its CT ribbon. Screenshots are actual OpenGL framebuffers.

The real-data project had no Lasagna normals attached: these screenshots exercise the documented fallback frame, with CT pixels available at L2. Lasagna resolver and surface-builder behavior was covered by tests, not real-data Lasagna registration.
Ubuntu, an SFTP attachment, and a whole-scroll object-store collection were not exercised in this validation.
The older PR demo illustrates the pre-cutover UI and is not evidence for this store migration.
