# Repository Python Function Documentation

## File: arguments/__init__.py

### Module-Level Functions
- `get_combined_args(parser: ArgumentParser)`
  - Docstring: No docstring provided.

### Class: GroupParams
*Docstring:* No docstring provided.

### Class: ParamGroup
*Docstring:* No docstring provided.

**Methods:**
    - `__init__(self, parser: ArgumentParser, name: str, fill_none=False)`
      - Docstring: No docstring provided.

    - `extract(self, args)`
      - Docstring: No docstring provided.

### Class: ModelParams
*Docstring:* No docstring provided.

**Methods:**
    - `__init__(self, parser, sentinel=False)`
      - Docstring: No docstring provided.

    - `extract(self, args)`
      - Docstring: No docstring provided.

### Class: PipelineParams
*Docstring:* No docstring provided.

**Methods:**
    - `__init__(self, parser)`
      - Docstring: No docstring provided.

### Class: OptimizationParams
*Docstring:* No docstring provided.

**Methods:**
    - `__init__(self, parser)`
      - Docstring: No docstring provided.

## File: convert.py

_No functions or classes defined._

## File: full_eval.py

_No functions or classes defined._

## File: gaussian_renderer/__init__.py

### Module-Level Functions
- `render(viewpoint_camera, pc: GaussianModel, pipe, bg_color: torch.Tensor, scaling_modifier=1.0, separate_sh=False, override_color=None, use_trained_exp=False)`
  - Docstring: Render the scene.  Background tensor (bg_color) must be on GPU!

## File: gaussian_renderer/network_gui.py

### Module-Level Functions
- `init(wish_host, wish_port)`
  - Docstring: No docstring provided.

- `try_connect()`
  - Docstring: No docstring provided.

- `read()`
  - Docstring: No docstring provided.

- `send(message_bytes, verify)`
  - Docstring: No docstring provided.

- `receive()`
  - Docstring: No docstring provided.

## File: lpipsPyTorch/__init__.py

### Module-Level Functions
- `lpips(x: torch.Tensor, y: torch.Tensor, net_type: str='alex', version: str='0.1')`
  - Docstring: Function that measures Learned Perceptual Image Patch Similarity (LPIPS).  Arguments: x, y (torch.Tensor): the input tensors to compare. net_type (str): the network type to compare the features: 'alex' | 'squeeze' | 'vgg'. Default: 'alex'. version (str): the version of LPIPS. Default: 0.1.

## File: lpipsPyTorch/modules/lpips.py
### Class: LPIPS
*Docstring:* Creates a criterion that measures Learned Perceptual Image Patch Similarity (LPIPS).  Arguments: net_type (str): the network type to compare the features: 'alex' | 'squeeze' | 'vgg'. Default: 'alex'. version (str): the version of LPIPS. Default: 0.1.

**Methods:**
    - `__init__(self, net_type: str='alex', version: str='0.1')`
      - Docstring: No docstring provided.

    - `forward(self, x: torch.Tensor, y: torch.Tensor)`
      - Docstring: No docstring provided.

## File: lpipsPyTorch/modules/networks.py

### Module-Level Functions
- `get_network(net_type: str)`
  - Docstring: No docstring provided.

### Class: LinLayers
*Docstring:* No docstring provided.

**Methods:**
    - `__init__(self, n_channels_list: Sequence[int])`
      - Docstring: No docstring provided.

### Class: BaseNet
*Docstring:* No docstring provided.

**Methods:**
    - `__init__(self)`
      - Docstring: No docstring provided.

    - `set_requires_grad(self, state: bool)`
      - Docstring: No docstring provided.

    - `z_score(self, x: torch.Tensor)`
      - Docstring: No docstring provided.

    - `forward(self, x: torch.Tensor)`
      - Docstring: No docstring provided.

### Class: SqueezeNet
*Docstring:* No docstring provided.

**Methods:**
    - `__init__(self)`
      - Docstring: No docstring provided.

### Class: AlexNet
*Docstring:* No docstring provided.

**Methods:**
    - `__init__(self)`
      - Docstring: No docstring provided.

### Class: VGG16
*Docstring:* No docstring provided.

**Methods:**
    - `__init__(self)`
      - Docstring: No docstring provided.

## File: lpipsPyTorch/modules/utils.py

### Module-Level Functions
- `normalize_activation(x, eps=1e-10)`
  - Docstring: No docstring provided.

- `get_state_dict(net_type: str='alex', version: str='0.1')`
  - Docstring: No docstring provided.

## File: metrics.py

### Module-Level Functions
- `readImages(renders_dir, gt_dir)`
  - Docstring: No docstring provided.

- `evaluate(model_paths)`
  - Docstring: No docstring provided.

## File: render.py

### Module-Level Functions
- `render_set(model_path, name, iteration, views, gaussians, pipeline, background, train_test_exp, separate_sh)`
  - Docstring: No docstring provided.

- `render_sets(dataset: ModelParams, iteration: int, pipeline: PipelineParams, skip_train: bool, skip_test: bool, separate_sh: bool)`
  - Docstring: No docstring provided.

## File: scene/__init__.py
### Class: Scene
*Docstring:* No docstring provided.

**Methods:**
    - `__init__(self, args: ModelParams, gaussians: GaussianModel, load_iteration=None, shuffle=True, resolution_scales=[1.0])`
      - Docstring: b :param path: Path to colmap scene main folder.

    - `save(self, iteration)`
      - Docstring: No docstring provided.

    - `getTrainCameras(self, scale=1.0)`
      - Docstring: No docstring provided.

    - `getTestCameras(self, scale=1.0)`
      - Docstring: No docstring provided.

## File: scene/cameras.py
### Class: Camera
*Docstring:* No docstring provided.

**Methods:**
    - `__init__(self, resolution, colmap_id, R, T, FoVx, FoVy, depth_params, image, invdepthmap, image_name, uid, trans=np.array([0.0, 0.0, 0.0]), scale=1.0, data_device='cuda', train_test_exp=False, is_test_dataset=False, is_test_view=False)`
      - Docstring: No docstring provided.

### Class: MiniCam
*Docstring:* No docstring provided.

**Methods:**
    - `__init__(self, width, height, fovy, fovx, znear, zfar, world_view_transform, full_proj_transform)`
      - Docstring: No docstring provided.

## File: scene/colmap_loader.py

### Module-Level Functions
- `qvec2rotmat(qvec)`
  - Docstring: No docstring provided.

- `rotmat2qvec(R)`
  - Docstring: No docstring provided.

- `read_next_bytes(fid, num_bytes, format_char_sequence, endian_character='<')`
  - Docstring: Read and unpack the next bytes from a binary file. :param fid: :param num_bytes: Sum of combination of {2, 4, 8}, e.g. 2, 6, 16, 30, etc. :param format_char_sequence: List of {c, e, f, d, h, H, i, I, l, L, q, Q}. :param endian_character: Any of {@, =, <, >, !} :return: Tuple of read and unpacked values.

- `read_points3D_text(path)`
  - Docstring: see: src/base/reconstruction.cc void Reconstruction::ReadPoints3DText(const std::string& path) void Reconstruction::WritePoints3DText(const std::string& path)

- `read_points3D_binary(path_to_model_file)`
  - Docstring: see: src/base/reconstruction.cc void Reconstruction::ReadPoints3DBinary(const std::string& path) void Reconstruction::WritePoints3DBinary(const std::string& path)

- `read_intrinsics_text(path)`
  - Docstring: Taken from https://github.com/colmap/colmap/blob/dev/scripts/python/read_write_model.py

- `read_extrinsics_binary(path_to_model_file)`
  - Docstring: see: src/base/reconstruction.cc void Reconstruction::ReadImagesBinary(const std::string& path) void Reconstruction::WriteImagesBinary(const std::string& path)

- `read_intrinsics_binary(path_to_model_file)`
  - Docstring: see: src/base/reconstruction.cc void Reconstruction::WriteCamerasBinary(const std::string& path) void Reconstruction::ReadCamerasBinary(const std::string& path)

- `read_extrinsics_text(path)`
  - Docstring: Taken from https://github.com/colmap/colmap/blob/dev/scripts/python/read_write_model.py

- `read_colmap_bin_array(path)`
  - Docstring: Taken from https://github.com/colmap/colmap/blob/dev/scripts/python/read_dense.py  :param path: path to the colmap binary file. :return: nd array with the floating point values in the value

### Class: Image
*Docstring:* No docstring provided.

**Methods:**
    - `qvec2rotmat(self)`
      - Docstring: No docstring provided.

## File: scene/dataset_readers.py

### Module-Level Functions
- `getNerfppNorm(cam_info)`
  - Docstring: No docstring provided.
  - Nested Functions:
    - `get_center_and_diag(cam_centers)`
      - Docstring: No docstring provided.

- `readColmapCameras(cam_extrinsics, cam_intrinsics, depths_params, images_folder, depths_folder, test_cam_names_list)`
  - Docstring: No docstring provided.

- `fetchPly(path)`
  - Docstring: No docstring provided.

- `storePly(path, xyz, rgb)`
  - Docstring: No docstring provided.

- `readColmapSceneInfo(path, images, depths, eval, train_test_exp, llffhold=8)`
  - Docstring: No docstring provided.

- `readCamerasFromTransforms(path, transformsfile, depths_folder, white_background, is_test, extension='.png')`
  - Docstring: No docstring provided.

- `readNerfSyntheticInfo(path, white_background, depths, eval, extension='.png')`
  - Docstring: No docstring provided.

### Class: CameraInfo
*Docstring:* No docstring provided.

### Class: SceneInfo
*Docstring:* No docstring provided.

## File: scene/gaussian_model.py
### Class: GaussianModel
*Docstring:* No docstring provided.

**Methods:**
    - `setup_functions(self)`
      - Docstring: No docstring provided.
      - Nested Functions:
        - `build_covariance_from_scaling_rotation(scaling, scaling_modifier, rotation)`
          - Docstring: No docstring provided.

    - `__init__(self, sh_degree, optimizer_type='default')`
      - Docstring: No docstring provided.

    - `capture(self)`
      - Docstring: No docstring provided.

    - `restore(self, model_args, training_args)`
      - Docstring: No docstring provided.

    - `get_scaling(self)`
      - Docstring: No docstring provided.
      - Decorators: `@property`

    - `get_rotation(self)`
      - Docstring: No docstring provided.
      - Decorators: `@property`

    - `get_xyz(self)`
      - Docstring: No docstring provided.
      - Decorators: `@property`

    - `get_features(self)`
      - Docstring: No docstring provided.
      - Decorators: `@property`

    - `get_features_dc(self)`
      - Docstring: No docstring provided.
      - Decorators: `@property`

    - `get_features_rest(self)`
      - Docstring: No docstring provided.
      - Decorators: `@property`

    - `get_opacity(self)`
      - Docstring: No docstring provided.
      - Decorators: `@property`

    - `get_exposure(self)`
      - Docstring: No docstring provided.
      - Decorators: `@property`

    - `get_exposure_from_name(self, image_name)`
      - Docstring: No docstring provided.

    - `get_covariance(self, scaling_modifier=1)`
      - Docstring: No docstring provided.

    - `oneupSHdegree(self)`
      - Docstring: No docstring provided.

    - `create_from_pcd(self, pcd: BasicPointCloud, cam_infos: int, spatial_lr_scale: float)`
      - Docstring: No docstring provided.

    - `training_setup(self, training_args)`
      - Docstring: No docstring provided.

    - `update_learning_rate(self, iteration)`
      - Docstring: Learning rate scheduling per step

    - `construct_list_of_attributes(self)`
      - Docstring: No docstring provided.

    - `save_ply(self, path)`
      - Docstring: No docstring provided.

    - `reset_opacity(self)`
      - Docstring: No docstring provided.

    - `load_ply(self, path, use_train_test_exp=False)`
      - Docstring: No docstring provided.

    - `replace_tensor_to_optimizer(self, tensor, name)`
      - Docstring: No docstring provided.

    - `_prune_optimizer(self, mask)`
      - Docstring: No docstring provided.

    - `prune_points(self, mask)`
      - Docstring: No docstring provided.

    - `cat_tensors_to_optimizer(self, tensors_dict)`
      - Docstring: No docstring provided.

    - `densification_postfix(self, new_xyz, new_features_dc, new_features_rest, new_opacities, new_scaling, new_rotation, new_tmp_radii)`
      - Docstring: No docstring provided.

    - `densify_and_split(self, grads, grad_threshold, scene_extent, N=2)`
      - Docstring: No docstring provided.

    - `densify_and_clone(self, grads, grad_threshold, scene_extent)`
      - Docstring: No docstring provided.

    - `densify_and_prune(self, max_grad, min_opacity, extent, max_screen_size, radii)`
      - Docstring: No docstring provided.

    - `add_densification_stats(self, viewspace_point_tensor, update_filter)`
      - Docstring: No docstring provided.

## File: train.py

### Module-Level Functions
- `training(dataset, opt, pipe, testing_iterations, saving_iterations, checkpoint_iterations, checkpoint, debug_from)`
  - Docstring: No docstring provided.

- `prepare_output_and_logger(args)`
  - Docstring: No docstring provided.

- `training_report(tb_writer, iteration, Ll1, loss, l1_loss, elapsed, testing_iterations, scene: Scene, renderFunc, renderArgs, train_test_exp)`
  - Docstring: No docstring provided.

## File: utils/camera_utils.py

### Module-Level Functions
- `loadCam(args, id, cam_info, resolution_scale, is_nerf_synthetic, is_test_dataset)`
  - Docstring: No docstring provided.

- `cameraList_from_camInfos(cam_infos, resolution_scale, args, is_nerf_synthetic, is_test_dataset)`
  - Docstring: No docstring provided.

- `camera_to_JSON(id, camera: Camera)`
  - Docstring: No docstring provided.

## File: utils/general_utils.py

### Module-Level Functions
- `inverse_sigmoid(x)`
  - Docstring: No docstring provided.

- `PILtoTorch(pil_image, resolution)`
  - Docstring: No docstring provided.

- `get_expon_lr_func(lr_init, lr_final, lr_delay_steps=0, lr_delay_mult=1.0, max_steps=1000000)`
  - Docstring: Copied from Plenoxels  Continuous learning rate decay function. Adapted from JaxNeRF The returned rate is lr_init when step=0 and lr_final when step=max_steps, and is log-linearly interpolated elsewhere (equivalent to exponential decay). If lr_delay_steps>0 then the learning rate will be scaled by some smooth function of lr_delay_mult, such that the initial learning rate is lr_init*lr_delay_mult at the beginning of optimization but will be eased back to the normal learning rate when steps>lr_delay_steps. :param conf: config subtree 'lr' or similar :param max_steps: int, the number of steps during optimization. :return HoF which takes step as input
  - Nested Functions:
    - `helper(step)`
      - Docstring: No docstring provided.

- `strip_lowerdiag(L)`
  - Docstring: No docstring provided.

- `strip_symmetric(sym)`
  - Docstring: No docstring provided.

- `build_rotation(r)`
  - Docstring: No docstring provided.

- `build_scaling_rotation(s, r)`
  - Docstring: No docstring provided.

- `safe_state(silent)`
  - Docstring: No docstring provided.
  - Nested Functions:
    - `__init__(self, silent)`
      - Docstring: No docstring provided.
    - `write(self, x)`
      - Docstring: No docstring provided.
    - `flush(self)`
      - Docstring: No docstring provided.

### Class: F
*Docstring:* No docstring provided.

## File: utils/graphics_utils.py

### Module-Level Functions
- `geom_transform_points(points, transf_matrix)`
  - Docstring: No docstring provided.

- `getWorld2View(R, t)`
  - Docstring: No docstring provided.

- `getWorld2View2(R, t, translate=np.array([0.0, 0.0, 0.0]), scale=1.0)`
  - Docstring: No docstring provided.

- `getProjectionMatrix(znear, zfar, fovX, fovY)`
  - Docstring: No docstring provided.

- `fov2focal(fov, pixels)`
  - Docstring: No docstring provided.

- `focal2fov(focal, pixels)`
  - Docstring: No docstring provided.

### Class: BasicPointCloud
*Docstring:* No docstring provided.

## File: utils/image_utils.py

### Module-Level Functions
- `mse(img1, img2)`
  - Docstring: No docstring provided.

- `psnr(img1, img2)`
  - Docstring: No docstring provided.

## File: utils/loss_utils.py

### Module-Level Functions
- `l1_loss(network_output, gt)`
  - Docstring: No docstring provided.

- `l2_loss(network_output, gt)`
  - Docstring: No docstring provided.

- `gaussian(window_size, sigma)`
  - Docstring: No docstring provided.

- `create_window(window_size, channel)`
  - Docstring: No docstring provided.

- `ssim(img1, img2, window_size=11, size_average=True)`
  - Docstring: No docstring provided.

- `_ssim(img1, img2, window, window_size, channel, size_average=True)`
  - Docstring: No docstring provided.

- `fast_ssim(img1, img2)`
  - Docstring: No docstring provided.

### Class: FusedSSIMMap
*Docstring:* No docstring provided.

**Methods:**
    - `forward(ctx, C1, C2, img1, img2)`
      - Docstring: No docstring provided.
      - Decorators: `@staticmethod`

    - `backward(ctx, opt_grad)`
      - Docstring: No docstring provided.
      - Decorators: `@staticmethod`

## File: utils/make_depth_scale.py

### Module-Level Functions
- `get_scales(key, cameras, images, points3d_ordered, args)`
  - Docstring: No docstring provided.

## File: utils/read_write_model.py

### Module-Level Functions
- `read_next_bytes(fid, num_bytes, format_char_sequence, endian_character='<')`
  - Docstring: Read and unpack the next bytes from a binary file. :param fid: :param num_bytes: Sum of combination of {2, 4, 8}, e.g. 2, 6, 16, 30, etc. :param format_char_sequence: List of {c, e, f, d, h, H, i, I, l, L, q, Q}. :param endian_character: Any of {@, =, <, >, !} :return: Tuple of read and unpacked values.

- `write_next_bytes(fid, data, format_char_sequence, endian_character='<')`
  - Docstring: pack and write to a binary file. :param fid: :param data: data to send, if multiple elements are sent at the same time, they should be encapsuled either in a list or a tuple :param format_char_sequence: List of {c, e, f, d, h, H, i, I, l, L, q, Q}. should be the same length as the data list or tuple :param endian_character: Any of {@, =, <, >, !}

- `read_cameras_text(path)`
  - Docstring: see: src/colmap/scene/reconstruction.cc void Reconstruction::WriteCamerasText(const std::string& path) void Reconstruction::ReadCamerasText(const std::string& path)

- `read_cameras_binary(path_to_model_file)`
  - Docstring: see: src/colmap/scene/reconstruction.cc void Reconstruction::WriteCamerasBinary(const std::string& path) void Reconstruction::ReadCamerasBinary(const std::string& path)

- `write_cameras_text(cameras, path)`
  - Docstring: see: src/colmap/scene/reconstruction.cc void Reconstruction::WriteCamerasText(const std::string& path) void Reconstruction::ReadCamerasText(const std::string& path)

- `write_cameras_binary(cameras, path_to_model_file)`
  - Docstring: see: src/colmap/scene/reconstruction.cc void Reconstruction::WriteCamerasBinary(const std::string& path) void Reconstruction::ReadCamerasBinary(const std::string& path)

- `read_images_text(path)`
  - Docstring: see: src/colmap/scene/reconstruction.cc void Reconstruction::ReadImagesText(const std::string& path) void Reconstruction::WriteImagesText(const std::string& path)

- `read_images_binary(path_to_model_file)`
  - Docstring: see: src/colmap/scene/reconstruction.cc void Reconstruction::ReadImagesBinary(const std::string& path) void Reconstruction::WriteImagesBinary(const std::string& path)

- `write_images_text(images, path)`
  - Docstring: see: src/colmap/scene/reconstruction.cc void Reconstruction::ReadImagesText(const std::string& path) void Reconstruction::WriteImagesText(const std::string& path)

- `write_images_binary(images, path_to_model_file)`
  - Docstring: see: src/colmap/scene/reconstruction.cc void Reconstruction::ReadImagesBinary(const std::string& path) void Reconstruction::WriteImagesBinary(const std::string& path)

- `read_points3D_text(path)`
  - Docstring: see: src/colmap/scene/reconstruction.cc void Reconstruction::ReadPoints3DText(const std::string& path) void Reconstruction::WritePoints3DText(const std::string& path)

- `read_points3D_binary(path_to_model_file)`
  - Docstring: see: src/colmap/scene/reconstruction.cc void Reconstruction::ReadPoints3DBinary(const std::string& path) void Reconstruction::WritePoints3DBinary(const std::string& path)

- `write_points3D_text(points3D, path)`
  - Docstring: see: src/colmap/scene/reconstruction.cc void Reconstruction::ReadPoints3DText(const std::string& path) void Reconstruction::WritePoints3DText(const std::string& path)

- `write_points3D_binary(points3D, path_to_model_file)`
  - Docstring: see: src/colmap/scene/reconstruction.cc void Reconstruction::ReadPoints3DBinary(const std::string& path) void Reconstruction::WritePoints3DBinary(const std::string& path)

- `detect_model_format(path, ext)`
  - Docstring: No docstring provided.

- `read_model(path, ext='')`
  - Docstring: No docstring provided.

- `write_model(cameras, images, points3D, path, ext='.bin')`
  - Docstring: No docstring provided.

- `qvec2rotmat(qvec)`
  - Docstring: No docstring provided.

- `rotmat2qvec(R)`
  - Docstring: No docstring provided.

### Class: Image
*Docstring:* No docstring provided.

**Methods:**
    - `qvec2rotmat(self)`
      - Docstring: No docstring provided.

## File: utils/sh_utils.py

### Module-Level Functions
- `eval_sh(deg, sh, dirs)`
  - Docstring: Evaluate spherical harmonics at unit directions using hardcoded SH polynomials. Works with torch/np/jnp. ... Can be 0 or more batch dimensions. Args: deg: int SH deg. Currently, 0-3 supported sh: jnp.ndarray SH coeffs [..., C, (deg + 1) ** 2] dirs: jnp.ndarray unit directions [..., 3] Returns: [..., C]

- `RGB2SH(rgb)`
  - Docstring: No docstring provided.

- `SH2RGB(sh)`
  - Docstring: No docstring provided.

## File: utils/system_utils.py

### Module-Level Functions
- `mkdir_p(folder_path)`
  - Docstring: No docstring provided.

- `searchForMaxIteration(folder)`
  - Docstring: No docstring provided.

## Submodule: diff-gaussian-rasterization (CUDA Functions)

_No CUDA functions detected or submodule unavailable._
