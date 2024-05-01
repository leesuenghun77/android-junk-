# android-junk-
안드로이드 캐시 정크 유튜브 빈폴더 모두 깨끗이 청소
#!/bin/sh
# 안드로이드 램 및 캐시 정리 스크립트

# 1. 램 정리
echo "램 정리 중..."
sync; echo 3 > /proc/sys/vm/drop_caches

# 2. 캐시 및 정크 파일 정리
echo "캐시 및 정크 파일 정리 중..."
rm -rf /cache/*
rm -rf /data/*/cache

# 3. 유튜브 캐시 정리
echo "유튜브 캐시 정리 중..."
rm -rf /data/data/com.google.android.youtube/cache

# 4. empty standby list 및 working set 정리
# 이 부분은 안드로이드 시스템에 따라 다를 수 있으므로, 시스템의 특정 요구 사항에 맞게 조정해야 합니다.
# 일반적으로 이러한 작업은 루트 권한이 필요하며, 안드로이드 버전에 따라 접근 방법이 다를 수 있습니다.

echo "정리 작업 완료."
gh repo clone aistra0528/Hail
