# 뉴크 버전관리
이번 챕터는 프로덕션단계에서 뉴크 버전을 어떻게 선택할지를 다루는 아티클 입니다.
굳이 이 내용을 따라할 필요는 없지만, 경험을 토대로 작성되었습니다.

저는 과거 프로덕션을 운용하면서 어떻게 하면 콘텐츠 제작 소프트웨어 버전을 안정적으로 관리할 수 있을지 한민한 적이 있습니다. 소프트웨어의 버전 선택만 잘해도 프로젝트를 진행하며 만나는 버그가 말도 안되게 줄어듭니다. 직원이 많으면 많을수록 덜 피곤해지는 겁니다.

소프트웨어 회사는 아래와 같은 업무를 진행합니다.
1. 매년 소프트웨어 제작사는 매출을 위해서 일정 기능이 추가된 새로운 버전을 출시합니다.
1. 출시된 제품은 고객, 회사가 사용하며 버그를 보고합니다.
    1. http://community.foundry.com/discuss/nuke
1. 소프트웨어 제작사를 통해서 버그가 수정됩니다.
1. 버그가 수정되면 다음 버전이 재배포 됩니다.
1. 위 상황은 1년을 두고 여러번 지속 될 수 있습니다.
    1. 릴리즈 노트를 자주 읽으며 자신의 환경에 참고할 만한 버그내용을 읽어보세요. https://thefoundry.s3.amazonaws.com/products/nuke/releases/11.2v5/Nuke11.2v5_ReleaseNotes.pdf
1. 소프트웨어 회사는 모든 버전에 대해서 유지보수, 관리할 수 없기 때문에 가장 오래된 버전의 관리를 중단합니다.

이러한 현상을 보면서 저는 작년 배포판중 가장 버그픽스가 많이 진행된 버전을 사용하면 꽤나 프로덕션에서 안정적이겠다고 생각하고 3~5년정도를 이 기준에 맞추어서 진행했습니다. 결과는 나름 만족했었습니다. 최신기능을 바로 사용할 순 없지만, 적어도 1년은 수많은 곳에서 테스트를 끝낸 버전일 테니까요. 수많은 회사들이 늘 최신기술을 요구받지는 않습니다. 일반적으로 안정적인 운용을 더 중요시하는 경우가 많습니다.