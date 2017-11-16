`disco_tree_2017-11-14-17-53-00.bag` contains mocap data from waving the Disco around near a tree with markers on it.
The marker at the origin of the tree's coordinate frame is just above the branch.

`disco_tree_nojointstate_2017-11-14-17-53-00.bag` is the same bag with the output of joint_state_publisher removed using the command:

```rosbag filter disco_tree_2017-11-14-17-53-00.bag disco_tree_nojointstate_2017-11-14-17-53-00.bag 'topic not in ["/tf", "/joint_states"] or (topic == "/tf" and m.transforms[0].header.frame_id not in ["base_link", "gimbal_link"])'```