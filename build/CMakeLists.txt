# 최소한의 CMake 버전 요구
cmake_minimum_required(VERSION 3.10)

# 프로젝트 이름 설정
project(send-arp)

# 헤더 파일이 위치한 경로 추가
include_directories(header)

# 모든 소스 파일을 소스 변수에 추가
set(SOURCES
    ../src/arphdr.cpp
    ../src/ethhdr.cpp
    ../src/ip.cpp
    ../src/mac.cpp
    ../src/main.cpp
)

# 실행 파일 생성
add_executable(send-arp ${SOURCES})

# 라이브러리 링크
target_link_libraries(send-arp pcap)
