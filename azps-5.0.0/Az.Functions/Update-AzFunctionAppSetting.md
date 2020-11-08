---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/update-azfunctionappsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppSetting.md
ms.openlocfilehash: 4255940b9cf17420fe0b522d81c6a974e9cf9324
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215403"
---
# Update-AzFunctionAppSetting

## SYNOPSIS
함수 앱에서 앱 설정을 추가 하거나 업데이트 합니다.

## 구문과

### ByName (기본값)
```
Update-AzFunctionAppSetting -Name <String> -ResourceGroupName <String> -AppSetting <Hashtable>
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### ByObjectInput
```
Update-AzFunctionAppSetting -AppSetting <Hashtable> -InputObject <ISite> [-Force] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## 설명은
함수 앱에서 앱 설정을 추가 하거나 업데이트 합니다.

## 예제의

### 예제 1: 함수 앱에 새 앱 설정을 추가 합니다.
```powershell
PS C:\> Update-AzFunctionAppSetting -Name MyAppName -ResourceGroupName MyResourceGroupName -AppSetting @{"Name1" = "Value1"}
```

이 명령은 함수 앱에 새 앱 설정을 추가 합니다.

## 변수

### -AppSetting
키 및 값이 있는 해시 테이블은 함수 앱에서 추가 하거나 업데이트할 앱 설정을 설명 합니다.
예: @ {"myappsetting" = "123"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile


```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
확인 메시지 없이 cmdlet에서 함수 앱 설정을 업데이트 하도록 강제 합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
생성 하려면 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite
Parameter Sets: ByObjectInput
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -이름
함수 앱의 이름입니다.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
자원이 속한 리소스 그룹의 이름입니다.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Azure 구독 ID입니다.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.
Cmdlet이 실행 되지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### Api20190801. ISite의. PowerShell for.

## 출력

### Api20190801. IStringDictionary의. PowerShell for.

## 상속자

별칭과

복합 매개 변수 속성

아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다. 해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.


INPUTOBJECT <ISite> : 
  - `Location <String>`: 리소스 위치입니다.
  - `CloningInfoSourceWebAppId <String>`: ARM 원본 앱의 리소스 ID입니다. 앱 리소스 ID는 프로덕션 슬롯 및 다른 슬롯의/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName}에 대 한/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} 형식입니다.
  - `[Kind <String>]`: 리소스 종류입니다.
  - `[Tag <IResourceTags>]`: 리소스 태그.
    - `[(Any) <String>]`:이 개체에 모든 속성이 추가 될 수 있음을 나타냅니다.
  - `[ClientAffinityEnabled <Boolean?>]`: <code>true</code> <code>false</code> 동일한 세션에서 클라이언트 요청을 동일한 인스턴스로 라우팅하기 위해 클라이언트 선호도를 사용 하도록 설정 하 고 세션 선호도 쿠키 보내기를 중지 합니다. 기본값은 <code>true</code> 입니다.
  - `[ClientCertEnabled <Boolean?>]`: <code>true</code> 클라이언트 인증서 인증 (TLS 상호 인증)을 사용 하도록 설정 하는 방법, 그렇지 않은 경우 <code>false</code> . 기본값은 <code>false</code> 입니다.
  - `[ClientCertExclusionPath <String>]`: 클라이언트 인증서 인증 쉼표로 구분 된 제외 경로
  - `[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: 복제 된 앱에 대 한 응용 프로그램 설정 재정의입니다. 이 설정을 지정 하면 원본 앱에서 복제 된 설정이 재정의 됩니다. 그렇지 않으면 원본 앱의 응용 프로그램 설정이 유지 됩니다.
    - `[(Any) <String>]`:이 개체에 모든 속성이 추가 될 수 있음을 나타냅니다.
  - `[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> 원본 앱에서 사용자 지정 호스트 이름을 복제 하 고, 그렇지 않으면 <code>false</code> .
  - `[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> 원본 앱에서 원본 컨트롤을 복제 하 고, 그렇지 않으면 <code>false</code> .
  - `[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> 원본 및 대상 앱에 대 한 부하 분산을 구성 합니다.
  - `[CloningInfoCorrelationId <String>]`: 복제 작업의 상관 관계 ID입니다. 이 ID는 여러 복제 작업을 결합 하 여 동일한 스냅숏을 사용 합니다.
  - `[CloningInfoHostingEnvironment <String>]`: 앱 서비스 환경.
  - `[CloningInfoOverwrite <Boolean?>]`: <code>true</code> 대상 앱을 덮어쓰려면, 그렇지 않으면 <code>false</code> .
  - `[CloningInfoSourceWebAppLocation <String>]`: 원본 앱의 위치 예: 미국 서 부 또는 서유럽
  - `[CloningInfoTrafficManagerProfileId <String>]`: 사용할 Traffic Manager 프로필의 ARM 리소스 ID입니다 (있는 경우). Traffic Manager 리소스 ID의 형식/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.
  - `[CloningInfoTrafficManagerProfileName <String>]`: 만들려는 Traffic Manager 프로필의 이름입니다. 이는 Traffic Manager 프로필이 아직 없는 경우에만 필요 합니다.
  - `[Config <ISiteConfig>]`: 앱의 구성입니다.
    - `IsPushEnabled <Boolean>`: 푸시 끝점을 사용할 수 있는지 여부를 나타내는 플래그를 가져오거나 설정 합니다.
    - `[ActionMinProcessExecutionTime <String>]`: 작업을 수행 하기 전에 프로세스를 실행 해야 하는 최소 시간
    - `[ActionType <AutoHealActionType?>]`: 수행 되도록 미리 정의 된 작업입니다.
    - `[AlwaysOn <Boolean?>]`: <code>true</code> Always On을 사용 하도록 설정 되 면, 그렇지 않으면 <code>false</code> .
    - `[ApiDefinitionUrl <String>]`: API 정의의 URL입니다.
    - `[ApiManagementConfigId <String>]`: APIM-Api 식별자입니다.
    - `[AppCommandLine <String>]`: 실행할 앱 명령줄입니다.
    - `[AppSetting <INameValuePair[]>]`: 응용 프로그램 설정
      - `[Name <String>]`: 쌍 이름.
      - `[Value <String>]`: Pair 값.
    - `[AutoHealEnabled <Boolean?>]`: <code>true</code> 자동 치료를 사용 하는 경우, 그렇지 않으면 <code>false</code> .
    - `[AutoSwapSlotName <String>]`: 자동 스왑 슬롯 이름입니다.
    - `[ConnectionString <IConnStringInfo[]>]`: 연결 문자열입니다.
      - `[ConnectionString <String>]`: 연결 문자열 값입니다.
      - `[Name <String>]`: 연결 문자열의 이름입니다.
      - `[Type <ConnectionStringType?>]`: 데이터베이스 유형입니다.
    - `[CorAllowedOrigin <String[]>]`: 교차 원본 호출을 허용 해야 하는 원본 목록 (예:)을 가져오거나 설정 http://example.com:12345) 합니다. "*"를 사용 하 여 all을 허용 합니다.
    - `[CorSupportCredentials <Boolean?>]`: 자격 증명을 사용 하 여 CORS 요청을 사용할 수 있는지 여부를 가져오거나 설정 합니다. 자세한 내용은         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         을 참조 하세요.
    - `[CustomActionExe <String>]`: 실행할 실행 파일입니다.
    - `[CustomActionParameter <String>]`: 실행 파일에 대 한 매개 변수입니다.
    - `[DefaultDocument <String[]>]`: 기본 문서.
    - `[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> 자세한 오류 로깅이 사용 되는 경우, 그렇지 않은 경우 <code>false</code> .
    - `[DocumentRoot <String>]`: 문서 루트
    - `[DynamicTagsJson <String>]`: 푸시 등록 끝점의 사용자 클레임에서 평가 되는 동적 태그 목록을 포함 하는 JSON 문자열을 가져오거나 설정 합니다.
    - `[ExperimentRampUpRule <IRampUpRule[]>]`: 램프 규칙의 목록입니다.
      - `[ActionHostName <String>]`: 트래픽을 결정 하는 경우 트래픽이 리디렉션되는 슬롯의 호스트 이름입니다. 즉. myapp-stage.azurewebsites.net.
      - `[ChangeDecisionCallbackUrl <String>]`: 사용자 지정 결정 알고리즘은 TiPCallback 사이트 확장에서 지정할 수 있는 URL을 제공할 수 있습니다. 모델링 및 계약에 대 한 TiPCallback 사이트 확장을 참조 하세요.         https://www.siteextensions.net/packages/TiPCallback/
      - `[ChangeIntervalInMinute <Int32?>]`: ReroutePercentage를 다시 계산 하는 간격 (분)을 지정 합니다.
      - `[ChangeStep <Double?>]`: 자동 램프 시나리오에서 <code>ReroutePercentage</code> \n 또는에 도달할 때까지 추가/제거 하는 단계입니다 <code>MinReroutePercentage</code>         <code>MaxReroutePercentage</code> . 사이트 메트릭은 .\NCustom 의사 결정 알고리즘에 지정 된 매 N 분을 <code>ChangeIntervalInMinutes</code> TiPCallback site extension에서 제공 하 고 URL에서 지정할 수 있는 것으로 확인 됩니다 <code>ChangeDecisionCallbackUrl</code> .
      - `[MaxReroutePercentage <Double?>]`: ReroutePercentage가 유지 되는 위쪽 경계를 지정 합니다.
      - `[MinReroutePercentage <Double?>]`: ReroutePercentage이 유지 되는 아래쪽 경계를 지정 합니다.
      - `[Name <String>]`: 라우팅 규칙의 이름입니다. 권장 되는 이름은 실험에서 트래픽을 수신 하는 슬롯을 가리키도록 하는 것입니다.
      - `[ReroutePercentage <Double?>]`: 리디렉션되는 소통량의 백분율 <code>ActionHostName</code> 입니다.
    - `[FtpsState <FtpsState?>]`: FTP/FTPS 서비스의 상태
    - `[HandlerMapping <IHandlerMapping[]>]`: 처리기 매핑.
      - `[Argument <String>]`: 스크립트 프로세서에 전달할 명령줄 인수입니다.
      - `[Extension <String>]`:이 확장명을 가진 요청은 지정 된 FastCGI 응용 프로그램을 사용 하 여 처리 됩니다.
      - `[ScriptProcessor <String>]`: FastCGI 응용 프로그램의 절대 경로입니다.
    - `[HealthCheckPath <String>]`: 상태 검사 경로
    - `[Http20Enabled <Boolean?>]`: Http20Enabled: 클라이언트가 http 2.0을 통해 연결할 수 있도록 웹 사이트를 구성 합니다.
    - `[HttpLoggingEnabled <Boolean?>]`: <code>true</code> HTTP 로깅이 사용 하도록 설정 되어 있으면 이 고, 그렇지 않으면 <code>false</code> 입니다.
    - `[IPSecurityRestriction <IIPSecurityRestriction[]>]`: 메인에 대 한 IP 보안 제한.
      - `[Action <String>]`:이 IP 범위에 대 한 액세스를 허용 하거나 거부 합니다.
      - `[Description <String>]`: IP 제한 규칙 설명입니다.
      - `[IPAddress <String>]`: IP 주소 보안 제한이에 유효 합니다.         순수한 ipv4 주소 (필수 SubnetMask 속성) 또는 ipv4/ipv6 표기법 (예: ipv4/mask (행간 비트 일치))의 형태가 될 수 있습니다. CIDR의 경우 SubnetMask 속성을 지정 하지 않아야 합니다.
      - `[Name <String>]`: IP 제한 규칙 이름입니다.
      - `[Priority <Int32?>]`: IP 제한 규칙의 우선 순위입니다.
      - `[SubnetMask <String>]`: 제한이 유효한 IP 주소 범위에 대 한 서브넷 마스크입니다.
      - `[SubnetTrafficTag <Int32?>]`: (내부) 서브넷 트래픽 태그
      - `[Tag <IPFilterTag?>]`:이 IP 필터를 사용할 용도를 정의 합니다. 이는 프록시에서 IP 필터링을 지원 하기 위한 것입니다.
      - `[VnetSubnetResourceId <String>]`: 가상 네트워크 리소스 id
      - `[VnetTrafficTag <Int32?>]`: (내부) Vnet 트래픽 태그
    - `[JavaContainer <String>]`: Java 컨테이너.
    - `[JavaContainerVersion <String>]`: Java 컨테이너 버전.
    - `[JavaVersion <String>]`: Java 버전.
    - `[LimitMaxDiskSizeInMb <Int64?>]`: 최대 허용 디스크 크기 사용량 (MB)입니다.
    - `[LimitMaxMemoryInMb <Int64?>]`: 허용 되는 최대 메모리 사용량 (MB)입니다.
    - `[LimitMaxPercentageCpu <Double?>]`: 허용 되는 최대 CPU 사용 백분율입니다.
    - `[LinuxFxVersion <String>]`: Linux 앱 프레임 워크 및 버전
    - `[LoadBalancing <SiteLoadBalancing?>]`: 사이트 로드 밸런싱.
    - `[LocalMySqlEnabled <Boolean?>]`: <code>true</code> 로컬 MySQL을 사용 하도록 설정 하 고, 그렇지 않으면 <code>false</code> .
    - `[LogsDirectorySizeLimit <Int32?>]`: HTTP 로그 디렉터리 크기 제한입니다.
    - `[MachineKeyDecryption <String>]`: 암호 해독에 사용 되는 알고리즘입니다.
    - `[MachineKeyDecryptionKey <String>]`: 암호 해독 키입니다.
    - `[MachineKeyValidation <String>]`: MachineKey 유효성 검사.
    - `[MachineKeyValidationKey <String>]`: 유효성 검사 키입니다.
    - `[ManagedPipelineMode <ManagedPipelineMode?>]`: 관리 되는 파이프라인 모드입니다.
    - `[ManagedServiceIdentityId <Int32?>]`: 관리 되는 서비스 Id Id
    - `[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: SSL 요청에 필요한 TLS의 최소 버전을 구성 합니다.
    - `[NetFrameworkVersion <String>]`: .NET Framework 버전.
    - `[NodeVersion <String>]`: Node.js 버전.
    - `[NumberOfWorker <Int32?>]`: 작업자 수.
    - `[PhpVersion <String>]`: PHP 버전.
    - `[PowerShellVersion <String>]`: PowerShell의 버전입니다.
    - `[PreWarmedInstanceCount <Int32?>]`: PreWarmed 인스턴스 수입니다.         이 설정은 사용량과 탄력적 요금제에만 적용 됩니다.
    - `[PublishingUsername <String>]`: 게시 사용자 이름입니다.
    - `[PushKind <String>]`: 리소스 종류입니다.
    - `[PythonVersion <String>]`: Python의 버전.
    - `[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> 원격 디버깅을 사용 하도록 설정한 경우, 그렇지 않으면 <code>false</code> .
    - `[RemoteDebuggingVersion <String>]`: 원격 디버깅 버전.
    - `[RequestCount <Int32?>]`: 요청 수.
    - `[RequestTimeInterval <String>]`: 시간 간격.
    - `[RequestTracingEnabled <Boolean?>]`: <code>true</code> 요청 추적을 사용 하도록 설정 하면 이 고, 그렇지 않으면 <code>false</code> 입니다.
    - `[RequestTracingExpirationTime <DateTime?>]`: 추적 만료 시간을 요청 합니다.
    - `[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: Scm에 대 한 IP 보안 제한.
    - `[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: Scm이 main을 사용할 수 있는 IP 보안 제한입니다.
    - `[ScmType <ScmType?>]`: SCM 유형.
    - `[SlowRequestCount <Int32?>]`: 요청 수.
    - `[SlowRequestTimeInterval <String>]`: 시간 간격.
    - `[SlowRequestTimeTaken <String>]`: 소요 시간.
    - `[TagWhitelistJson <String>]`: 푸시 등록 끝점에서 사용 하는 허용 목록 태그 목록을 포함 하는 JSON 문자열을 가져오거나 설정 합니다.
    - `[TagsRequiringAuth <String>]`: 푸시 등록 끝점에서 사용자 인증을 사용 해야 하는 태그 목록이 포함 된 JSON 문자열을 가져오거나 설정 합니다.         태그는 영숫자 문자로 구성 되며 ' _ ', ' @ ', ' # ', '. ', ': ', '-'로 구성할 수 있습니다.         PushRequestHandler에서 유효성 검사를 수행 해야 합니다.
    - `[TracingOption <String>]`: 추적 옵션
    - `[TriggerPrivateBytesInKb <Int32?>]`: 전용 바이트를 기준으로 하는 규칙입니다.
    - `[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: 상태 코드를 기준으로 하는 규칙입니다.
      - `[Count <Int32?>]`: 요청 수.
      - `[Status <Int32?>]`: HTTP 상태 코드.
      - `[SubStatus <Int32?>]`: 하위 상태 요청
      - `[TimeInterval <String>]`: 시간 간격.
      - `[Win32Status <Int32?>]`: Win32 오류 코드.
    - `[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> 32 비트 작업자 프로세스를 사용 하 고, 그렇지 않으면 <code>false</code> .
    - `[VirtualApplication <IVirtualApplication[]>]`: 가상 응용 프로그램.
      - `[PhysicalPath <String>]`: 실제 경로.
      - `[PreloadEnabled <Boolean?>]`: <code>true</code> 미리 로드를 사용 하도록 설정한 경우, 그렇지 않으면 <code>false</code> .
      - `[VirtualDirectory <IVirtualDirectory[]>]`: 가상 응용 프로그램의 가상 디렉터리입니다.
        - `[PhysicalPath <String>]`: 실제 경로.
        - `[VirtualPath <String>]`: 가상 응용 프로그램 경로입니다.
      - `[VirtualPath <String>]`: 가상 경로입니다.
    - `[VnetName <String>]`: 가상 네트워크 이름입니다.
    - `[WebSocketsEnabled <Boolean?>]`: <code>true</code> WebSocket을 사용 하도록 설정한 경우, 그렇지 않으면 <code>false</code> .
    - `[WindowsFxVersion <String>]`: 크 세 앱 프레임 워크 및 버전
    - `[XManagedServiceIdentityId <Int32?>]`: 관리 되는 명시적 서비스 Id Id
  - `[ContainerSize <Int32?>]`: 함수 컨테이너의 크기입니다.
  - `[DailyMemoryTimeQuota <Int32?>]`: 허용 되는 최대 메모리 시간 할당량 (동적 앱에만 해당).
  - `[Enabled <Boolean?>]`: <code>true</code> 앱을 사용 하도록 설정한 경우, 그렇지 않으면 <code>false</code> . 이 값을 false로 설정 하면 앱을 사용할 수 없게 됩니다 (앱을 오프 라인 상태로 전환).
  - `[HostNameSslState <IHostNameSslState[]>]`: Hostname SSL 상태는 앱의 호스트 이름에 대 한 SSL 바인딩을 관리 하는 데 사용 됩니다.
    - `[HostType <HostType?>]`: 호스트 이름이 표준 또는 리포지토리 호스트 이름 인지 여부를 나타냅니다.
    - `[Name <String>]`이름의.
    - `[SslState <SslState?>]`: SSL 유형입니다.
    - `[Thumbprint <String>]`: SSL 인증서 지문.
    - `[ToUpdate <Boolean?>]`: <code>true</code> 기존 호스트 이름을 업데이트 하도록 설정 합니다.
    - `[VirtualIP <String>]`: IP 기반 SSL을 사용 하는 경우 호스트 이름에 가상 IP 주소를 할당 합니다.
  - `[HostNamesDisabled <Boolean?>]`: <code>true</code> 앱의 공용 호스트 이름을 사용 하지 않도록 설정 하 고, 그렇지 않으면 <code>false</code> .          <code>true</code>앱이 API management 프로세스를 통해서만 액세스할 수 있는 경우
  - `[HostingEnvironmentProfileId <String>]`: 앱 서비스 환경의 리소스 ID입니다.
  - `[HttpsOnly <Boolean?>]`: HttpsOnly: 웹 사이트가 https 요청만 수락 하도록 구성 합니다. Http 요청에 대 한 문제 리디렉션
  - `[HyperV <Boolean?>]`: Hyper-v 샌드박스.
  - `[IdentityType <ManagedServiceIdentityType?>]`: 관리 되는 서비스 id의 유형입니다.
  - `[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: 리소스와 연결 된 사용자 할당 id의 목록입니다. 사용자 id 사전 키 참조는 '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName} ' 형식의 팔로 리소스 id를 사용 합니다.
    - `[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`:이 개체에 모든 속성이 추가 될 수 있음을 나타냅니다.
  - `[IsXenon <Boolean?>]`: 구식: Hyper-v 샌드박스.
  - `[RedundancyMode <RedundancyMode?>]`: 사이트 중복 모드
  - `[Reserved <Boolean?>]`: <code>true</code> 예약 된 경우, 그렇지 않으면 <code>false</code> .
  - `[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> 앱이 중지 되 면 SCM (KUDU) 사이트를 중지 하 고, 그렇지 않으면 <code>false</code> . 기본값은 <code>false</code> 입니다.
  - `[ServerFarmId <String>]`: 연결 된 앱 서비스 계획의 리소스 ID: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}" 형식으로 지정 됩니다.

## 관련 링크

