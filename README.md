# EmerNeRF_yang
Used for EmerNeRF

Train:
  
  python train_emernerf.py \
    --config_file configs/default_flow.yaml \
    --output_root $output_root \
    --project $project \
    --run_name ${scene_idx}_flow \
    data.scene_idx=$scene_idx \
    data.start_timestep=$start_timestep \
    data.end_timestep=$end_timestep \
    data.pixel_source.load_features=True \
    data.pixel_source.feature_model_type=dinov2_vitb14 \
    nerf.model.head.enable_feature_head=True \
    nerf.model.head.enable_learnable_pe=True \
    logging.saveckpt_freq=$num_iters \
    optim.num_iters=$num_iters
