---

copyright:
  years: 1994, 2019
lastupdated: "2019-02-05"

---
{:new_window: target="_blank"}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:DomainName: data-hd-keyref="APPDomain"}
{:DomainName: data-hd-keyref="DomainName"}

# BMR 시스템 볼륨 이미지 복원
{: #restoreBMR}

{{site.data.keyword.backup_full}}에서 베어메탈 이미지 백업의 복원이 필요하면 BMR Rescue Kernel 시스템에서 이를 신속하게 복원할 수 있습니다. BMR을 사용하면 부트 가능한 운영 체제가 없어도 시스템을 복원할 수 있습니다. 이는 운영 체제가 더 이상 사용 가능하지 않거나 시스템의 드라이브가 대체된 경우에 유용합니다.

## BMR Rescue Kernel 시스템 시작

{{site.data.keyword.slportal}}을 통해 BMR Rescue Kernel 시스템에 액세스할 수 있습니다.
1. [{{site.data.keyword.cloud_notm}} 콘솔](https://{DomainName}/){:new_window}에 로그인하여 왼쪽 상단의 **메뉴** 아이콘을 클릭하십시오. **일반 인프라**를 선택하십시오.<br/>
또는 [{{site.data.keyword.slportal}} ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://control.softlayer.com/){:new_window}에 로그인할 수 있습니다.
2. **스토리지** > **백업**을 클릭하여 백업 서비스의 서버를 표시하십시오.
3. 저장소 옆의 **화살표**를 클릭하십시오.
4. **Bare Metal Restore 시작**을 클릭하십시오. 이 조치는 완료하는 데 수 분이 걸리는 트랜잭션을 시작합니다. 이후에 여기서 자세히 설명한 단계에 따라 서버에 액세스할 수 있습니다. 시스템이 부트 프로세스를 완료하면 사용자에게 이메일이 발송됩니다.


## BMR Rescue Kernel에서 복원

1. BMR Rescue Kernel 트랜잭션 로드 시에 두 가지 상이한 방법으로 이에 액세스하도록 선택할 수 있습니다.
  - {{site.data.keyword.slportal}}에 나열된 비밀번호 및 서버의 사설 또는 공인 IP 주소 및 VNC 클라이언트
  - IPMI 카드의 KVM 콘솔.
  이러한 방법은 둘 다 잘 작동됩니다.
2. 처음으로 BMR Rescue Kernel에 로그인하면 언어 선택 화면이 나타납니다. 원하는 언어를 선택하고 **다음**을 클릭하십시오.
<br/>![그림 1 - BMR 언어 선택](/images/bmr1.png)<br/> 소프트웨어의 라이센스 계약이 표시됩니다.
3. 이용 약관에 동의하면 선택란을 선택하고 **다음**을 클릭하여 계속하십시오. <br/> 기본 {{site.data.keyword.backup_notm}} 시스템 복원 메뉴가 표시됩니다.
4. **내 시스템 복원**을 선택하십시오.
<br/>![그림 2 - BMR 기본 메뉴](/images/bmr2.png)
5. 시스템 복원 마법사가 나타납니다. **다음**을 선택하여 계속하십시오.
<br/>![그림 3 - BMR 마법사](/images/bmr3.png)
6. 복원되는 백업 유형을 선택하십시오. **EVault 소프트웨어**를 선택한 후에 **다음**을 클릭하여 계속하십시오.
7. **백업 위치** 화면에서 저장소를 선택하고 저장소 주소, 계정 번호, 사용자 이름과 비밀번호를 입력하십시오. 그리고 **다음**을 클릭하여 계속하십시오.
<br/>![그림 4 - 백업 위치 선택](/images/bmr4.png)
8. 다음 화면에서는 목록에 시스템이 표시됩니다. 시스템이 강조표시되어 있는지 확인하고 **다음**을 클릭하십시오.
<br/>![그림 5 - 시스템 선택](/images/bmr5.png)
9. **백업 작업 선택** 화면에서 복원할 작업을 선택하고 **다음**을 클릭하십시오.
<br/>![그림 6 - 복원 지점 선택](/images/bmr6.png)
10. **복원 지점 선택** 메뉴에서 원하는 복원 지점을 선택하고 **다음**을 클릭하십시오.
<br/>![그림 8 - 복원 지점 선택](/images/bmr8.png)
11. 소스 및 대상 볼륨을 선택하십시오. 대상으로 소스를 복원하려면 소스 볼륨을 대상 볼륨으로 끌어오십시오.
<br/>![그림 9 - 소스 및 대상 볼륨 선택](/images/bmr9.png)
12. 데이터 병합 또는 형식화 확인 상자에 있는 두 개의 옵션 중에서 선택할 수 있습니다. 디스크를 형식화하는 정리 복원에 대해 **형식화**를 선택하십시오. 대상 볼륨에서 데이터를 병합하려면 **병합**을 선택하십시오.
<br/>![그림 10 - 병합 선택](/images/bmr10.png)
13. 기본 소스 및 대상 볼륨 화면에서 **다음**을 클릭하십시오.
14. 복원 플랜 요약 화면에서 상자를 선택하여 플랜에 동의하고 **다음**을 클릭하십시오.
<br/>![그림 11 - 복원 시작](/images/bmr11.png)
15. 복원 진행상태 화면이 나타나며 복원 시에 이의 진행상태를 표시합니다.
<br/>![그림 12 - 복원 진행상태](/images/bmr12.png)
16. 완료되면 복원이 정상적으로 완료되었음을 알리는 알림 창이 수신됩니다. **확인**을 클릭하십시오.
17. 복원 진행상태 화면에서 **다음**을 클릭하십시오.
18. 최종 화면에서 시스템 다시 시작에 대한 상자를 선택하고 **완료**를 선택하십시오. 서버가 복원된 볼륨 이미지를 로드합니다.
  이제 복원이 완료되었습니다. <br/>

  서버가 처음으로 다시 시작하면 예상치 못한 시스템 종료 메시지가 나타날 수 있습니다. 이는 이 백업 유형에서 일반적인 현상이며 최초 부팅 이후에는 사라집니다.
  {:tip}
