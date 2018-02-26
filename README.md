# Camera SELinux Fix Latestart

Runs `magiskpolicy --live "allow hal_camera_default surfaceflinger_service service_manager find"` in `service.sh` when latestart event is called. 
This allows the system, and hence SELinux, to be loaded on encrypted phones when it is run, unlike on modules using `post-fs-data.sh`.