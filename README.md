pip install kiss_slam 하고 
명령어 도움 kiss_slam_pipeline --help 
open3D github repo 에서 0.19.0 버전 다운받아야합니다

ImportError 발생 하면 export PYTHONPATH=$PYTHONPATH:/home/(username)/kiss_ws/src/kiss_slam_ros/src 이거 한번 해보세요

추가로 node_main.py 에서 자신의 라이다 포인트 토픽에 맞게 변경해주셔야 합니다.


##실행 rosrun kiss_slam_ros kiss_slam_node.py
