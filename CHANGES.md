
# AliceVision Changelog

## Release 2.0.0 (2018.08.09)

Release of the full 3D reconstruction pipeline.

### 2018.07

 - New Docker images for Centos 7 and Ubuntu 18
 - New "make bundle" for packaging
 - Refactor split sfm / sfmData / sfmDataIO
 - New visibility remapping methods: Push, PullPush
 - Improve texturing quality with better image selection
 - SfM support multiple folders for features and matches
 - PopSiftImageDescriber: no initialization if not used
 - Offline camera tracking improvements
 - Tests datasets Anna + test imageMatching options + tests sequence alone
 - Export animated camera ABC
 - Export undistorted images and filter option
 - MeshroomMaya script integration Image Plane
 - Minor fixes in cameraSensors DB search
 - New fallback if no sensor width info available but FocalLengthIn35mmFilm metadata is present
 - ImageMatchingMultiSfM: add “a_a+a_b” option

### 2018.06

 - SfM augmentation: lock cameras from the initial reconstruction
 - SfM : Add option in order to disable the cleaning of tracks forks

### 2018.03

 - Merge the MVS pipeline in the main branch
 - New options for better auto UVs based on geogram (needs reasonable mesh size in input)
 - Use full resolution images in the MVS pipeline: PrepareDenseScene creates full resolution undistorted images, DepthMap computes downscale when loading images and Texturing can be done in full resolution.
 - Improve depth map fusion with a multi-scale approach
 - ImageMatching: no conflit if multiple images with the same UID
 - Add SIFT_UPRIGHT imageDescriber

## Release 1.0.0 (2018.03.07)

Release of the Structure-From-Motion pipeline.

### 2018.02

 - Support Raw and Exr input files
 - Texturing: add multithreading / clean iteration over pixels in triangle
 - MVS: use UIDs
 - Major MVS refactoring
 - New Mesh Denoiser and Decimate based on MeshSDFilter
 - Integration of Uncertainty computation step

### 2018.01

 - meshing: remove facets with helper points but limit holes creation
 - texturing: don’t modify the topology
 - meshing: add an option to keep only the largest facets group
 - geogram as a submodule of cmpmvs
 - Update SfM
 - Modify Image Matching
 - SfM Reorientation software
 - Use OpenMP for featureExtraction with a new imageDescriber memory needs estimation
 - Rewrite “Identify the track to triangulate” in triangulateMultiViews_LORANSAC
 - popSIFT directly on floating point images
 - Use relative path for features and matches in SfM
 - Remove cereal dependency
 - Remove static functions in headers
 - MVS: add namespace per module
 - MVS: build as dynamic libraries
 - MVS: remove unneeded intermediate images

### 2017.12

 - Reduce the amount of storage for intermediate files and improve robustness to kill/restart jobs on renderfarm
 - New software to create simplified versions of the mesh
 - Use OpenImageIO in MVS
 - Use floating point image in texturing

### 2017.11

 - New Local Bundle Adjustment to speedup SfM on large scenes
 - Retexturing on an external user mesh with a retopology (no visibility information and support user UVs) with a first visibilities remapping method.
 - Add new images to a previous SfM reconstruction
 - Use OpenImageIO in SfM

### 2017.10

 - Reduce memory usage on Meshing

### 2017.10

 - SfM: Support for RIG of synchronized cameras/DSLR with a new constraint between rigidly fixed cameras
 - New software utility for 360° cameras

### 2017.08

 - Tetrahedralization scoring with boost maxflow

### 2017.07

 - Meshing tetrahedralization with geogram
 - Texturing speedup
 - Rewrite CUDA layer

### 2017.06

 - SfM: weighting on image describers to combine them correctly

### 2017.03

 - MVS: support for multiple image resolutions

### 2017.02

 - MVS: code comments
 - MVS; performance improvements
 - Texturing: fix UV coords
 - MVS: split Meshing and Texturing steps
 - Texturing: rewrite edge padding for performance reasons

### 2017.01

 - MVS: linux code porting

### 2016

 - Integration of PopSift: a new GPU SIFT implementation
 - SfM: Add LoRansac
 - SfM: new next best view strategy

### 2015

 - New Alembic file format
 - Integration of new CCTag markers with CPU and CPU implementations
 - New camera localization module with RIG support
 - SfM speedups and refactoring
 - New Image Matching based on vocabulary tree approach

### 2014

 - First public source code release of the SfM pipeline
