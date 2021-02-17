---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/remove-azfunctionappsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppSetting.md
ms.openlocfilehash: abfa704b042b0a8cd25b8682e3b93306b5ca6277
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188412"
---
# Remove-AzFunctionAppSetting

## SYNOPSIS
함수 앱에서 앱 설정을 제거합니다.

## 구문

### ByName(기본값)
```
Remove-AzFunctionAppSetting -Name <String> -ResourceGroupName <String> -AppSettingName <String[]>
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### ByObjectInput
```
Remove-AzFunctionAppSetting -AppSettingName <String[]> -InputObject <ISite> [-Force]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## 설명
함수 앱에서 앱 설정을 제거합니다.

## 예제

### 예제 1: 함수 앱에서 앱 설정을 제거합니다.
```powershell
PS C:\> Remove-AzFunctionAppSetting -Name MyAppName -ResourceGroupName MyResourceGroupName -AppSettingName "MyAppSetting1", "MyAppSetting2"
```

이 명령은 함수 앱에서 앱 설정을 제거합니다.

## PARAMETERS

### -AppSettingName
함수 앱에서 제거할 함수 앱 설정 목록입니다.

```yaml
Type: System.String[]
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
확인 메시지를 표시하지 않고 cmdlet이 함수 앱 설정을 제거합니다.

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
생성을 위해 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.

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

### -Name
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
리소스가 속한 리소스 그룹의 이름입니다.

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

### -Confirm
cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.

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
cmdlet이 실행되는 경우의 결과 표시
cmdlet이 실행되지 않습니다.

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite

## 출력

### Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IStringDictionary

## 참고 사항

별칭

복합 매개 변수 속성

아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다. 해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.


INPUTOBJECT: <ISite> 
  - `Location <String>`: 리소스 위치입니다.
  - `CloningInfoSourceWebAppId <String>`: ARM 앱의 리소스 ID를 식별합니다. 앱 리소스 ID는 프로덕션 슬롯 및 /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName}의 형식입니다.
  - `[Kind <String>]`: 리소스의 종류입니다.
  - `[Tag <IResourceTags>]`: 리소스 태그입니다.
    - `[(Any) <String>]`: 이 개체에 추가할 수 있는 속성을 나타냅니다.
  - `[ClientAffinityEnabled <Boolean?>]`: 클라이언트 연결성을 사용하도록 설정하려면, 동일한 세션의 클라이언트 요청을 동일한 인스턴스로 라우팅하는 세션 연결 쿠키 전송을 <code>true</code> <code>false</code> 중지합니다. 기본값은 <code>true</code> .
  - `[ClientCertEnabled <Boolean?>]`: <code>true</code> 클라이언트 인증서 인증(TLS 상호 인증)을 사용하도록 설정하려면, 그렇지 않으면 <code>false</code> . 기본값은 <code>false</code> .
  - `[ClientCertExclusionPath <String>]`: 클라이언트 인증서 인증 콤마로 구분된 제외 경로
  - `[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: 복제된 앱에 대한 애플리케이션 설정이 오버라이드됩니다. 지정된 경우 이러한 설정은 원본 앱에서 복제된 설정을 오버라우트합니다. 그렇지 않으면 원본 앱의 애플리케이션 설정이 유지됩니다.
    - `[(Any) <String>]`: 이 개체에 추가할 수 있는 속성을 나타냅니다.
  - `[CloningInfoCloneCustomHostName <Boolean?>]`: 원본 앱에서 사용자 지정 호스트 이름을 복제합니다. 그렇지 않으면 <code>true</code> <code>false</code>
  - `[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> 원본 앱에서 소스 제어를 복제합니다. 그렇지 않으면 <code>false</code>
  - `[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> 원본 및 대상 앱에 대한 부하 분산을 구성합니다.
  - `[CloningInfoCorrelationId <String>]`: 복제 작업의 상관 관계 ID입니다. 이 ID는 동일한 스냅숏을 사용하기 위해 여러 복제 작업을 함께 관련합니다.
  - `[CloningInfoHostingEnvironment <String>]`: App Service Environment.
  - `[CloningInfoOverwrite <Boolean?>]`: <code>true</code> 대상 앱을 덮어 사용, 그렇지 않은 경우 <code>false</code> .
  - `[CloningInfoSourceWebAppLocation <String>]`: 원본 앱의 위치 예: 미국 서부 또는 북유럽
  - `[CloningInfoTrafficManagerProfileId <String>]`: ARM 사용할 Traffic Manager 프로필의 리소스 ID(있는 경우)를 제공합니다. Traffic Manager 리소스 ID는 /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}의 형식입니다.
  - `[CloningInfoTrafficManagerProfileName <String>]`: 만들 Traffic Manager 프로필의 이름입니다. Traffic Manager 프로필이 아직 없는 경우 필요합니다.
  - `[Config <ISiteConfig>]`: 앱의 구성입니다.
    - `IsPushEnabled <Boolean>`: 푸시 엔드포인트를 사용하도록 설정하는지 여부를 나타내는 플래그를 얻거나 설정합니다.
    - `[ActionMinProcessExecutionTime <String>]`: 작업을 수행하기 전에 프로세스가 실행되어야 하는 최소 시간
    - `[ActionType <AutoHealActionType?>]`: 수행될 미리 정의된 작업입니다.
    - `[AlwaysOn <Boolean?>]`: <code>true</code> Always On을 사용하도록 설정한 경우, 그렇지 않은 경우 <code>false</code> .
    - `[ApiDefinitionUrl <String>]`: API 정의의 URL입니다.
    - `[ApiManagementConfigId <String>]`: APIM-Api 식별자입니다.
    - `[AppCommandLine <String>]`: 앱 명령줄을 실행합니다.
    - `[AppSetting <INameValuePair[]>]`: 애플리케이션 설정입니다.
      - `[Name <String>]`: 페어링 이름입니다.
      - `[Value <String>]`: 쌍 값입니다.
    - `[AutoHealEnabled <Boolean?>]`: <code>true</code> 자동 고치기 사용이 설정된 경우, 그렇지 않으면 <code>false</code>
    - `[AutoSwapSlotName <String>]`: 슬롯 이름 자동 교환.
    - `[ConnectionString <IConnStringInfo[]>]`: 연결 문자열입니다.
      - `[ConnectionString <String>]`: 연결 문자열 값입니다.
      - `[Name <String>]`: 연결 문자열의 이름입니다.
      - `[Type <ConnectionStringType?>]`: 데이터베이스 유형입니다.
    - `[CorAllowedOrigin <String[]>]`: 원본 간 호출을 허용해야 하는 원본 목록을 얻거나 설정합니다(예: http://example.com:12345) "*"를 사용하여 모두 허용합니다.
    - `[CorSupportCredentials <Boolean?>]`: 자격 증명을 사용하여 CORS 요청이 허용될지 여부를 얻거나 설정합니다. 자세한         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         내용은 다음을 참조합니다.
    - `[CustomActionExe <String>]`: 실행할 실행 가능.
    - `[CustomActionParameter <String>]`: 실행 가능한 매개 변수입니다.
    - `[DefaultDocument <String[]>]`: 기본 문서입니다.
    - `[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> 자세한 오류 로깅을 사용하도록 설정한 경우, 그렇지 않으면 <code>false</code> .
    - `[DocumentRoot <String>]`: 문서 루트입니다.
    - `[DynamicTagsJson <String>]`: 푸시 등록 엔드포인트의 사용자 클레임에서 평가할 동적 태그 목록을 포함하는 JSON 문자열을 얻거나 설정합니다.
    - `[ExperimentRampUpRule <IRampUpRule[]>]`: 램프업 규칙 목록입니다.
      - `[ActionHostName <String>]`: 결정된 경우 트래픽이 리디렉션될 슬롯의 호스트 이름입니다. 예: myapp-stage.azurewebsites.net.
      - `[ChangeDecisionCallbackUrl <String>]`: URL을 지정할 수 있는 TiPCallback 사이트 확장에서 사용자 지정 의사 결정 알고리즘을 제공하면 됩니다. 스캐폴드 및 계약에 대한 TiPCallback 사이트 확장을 참조하세요.         https://www.siteextensions.net/packages/TiPCallback/
      - `[ChangeIntervalInMinute <Int32?>]`: ReroutePercentage를 다시 평가할 간격을 분으로 지정합니다.
      - `[ChangeStep <Double?>]`: 자동 램프 시나리오에서는 \n 또는 에 도달할 때까지 추가/제거하는 <code>ReroutePercentage</code> <code>MinReroutePercentage</code>         <code>MaxReroutePercentage</code> 단계입니다. 사이트 메트릭은 .\nCustom 의사 결정 알고리즘에 지정된 N분마다 확인되어 TiPCallback 사이트 확장에서 URL을 지정할 <code>ChangeIntervalInMinutes</code> 수 <code>ChangeDecisionCallbackUrl</code> 있습니다.
      - `[MaxReroutePercentage <Double?>]`: ReroutePercentage가 유지될 아래의 위쪽 경계를 지정합니다.
      - `[MinReroutePercentage <Double?>]`: ReroutePercentage가 유지될 아래쪽 경계를 지정합니다.
      - `[Name <String>]`: 라우팅 규칙의 이름입니다. 실험에서 트래픽을 수신할 슬롯을 지정하는 것이 좋습니다.
      - `[ReroutePercentage <Double?>]`: 리디렉션될 트래픽의 백분율입니다. <code>ActionHostName</code>
    - `[FtpsState <FtpsState?>]`: FTP/FTPS 서비스 상태
    - `[HandlerMapping <IHandlerMapping[]>]`: 처리기 매핑입니다.
      - `[Argument <String>]`: 스크립트 프로세서에 전달할 명령줄 인수입니다.
      - `[Extension <String>]`: 이 확장이 있는 요청은 지정된 FastCGI 애플리케이션을 사용하여 처리됩니다.
      - `[ScriptProcessor <String>]`: FastCGI 애플리케이션에 대한 절대 경로입니다.
    - `[HealthCheckPath <String>]`: 상태 검사 경로
    - `[Http20Enabled <Boolean?>]`: Http20Enabled: 클라이언트가 http2.0을 통해 연결할 수 있도록 웹 사이트를 구성합니다.
    - `[HttpLoggingEnabled <Boolean?>]`: <code>true</code> HTTP 로깅을 사용하도록 설정한 경우, 그렇지 않은 경우 <code>false</code> .
    - `[IPSecurityRestriction <IIPSecurityRestriction[]>]`: 기본에 대한 IP 보안 제한 사항입니다.
      - `[Action <String>]`: 이 IP 범위에 대한 액세스를 허용하거나 거부합니다.
      - `[Description <String>]`: IP 제한 규칙 설명입니다.
      - `[IPAddress <String>]`: IP 주소 보안 제한이 유효한 주소입니다.         순수 ipv4 주소(필수 SubnetMask 속성) 또는 ipv4/mask(선행 비트 일치)와 같은 CIDR 문구의 형식일 수 있습니다. CIDR의 경우 SubnetMask 속성을 지정하지 말아야 합니다.
      - `[Name <String>]`: IP 제한 규칙 이름입니다.
      - `[Priority <Int32?>]`: IP 제한 규칙의 우선 순위입니다.
      - `[SubnetMask <String>]`: IP 주소 범위에 대한 서브넷 마스크 제한이 유효합니다.
      - `[SubnetTrafficTag <Int32?>]`: (내부) 서브넷 트래픽 태그
      - `[Tag <IPFilterTag?>]`: 이 IP 필터를 사용할 것을 정의합니다. 이는 Proxies에서 IP 필터링을 지원하기 위한 것입니다.
      - `[VnetSubnetResourceId <String>]`: 가상 네트워크 리소스 ID
      - `[VnetTrafficTag <Int32?>]`: (내부) Vnet 트래픽 태그
    - `[JavaContainer <String>]`: Java 컨테이너입니다.
    - `[JavaContainerVersion <String>]`: Java 버전입니다.
    - `[JavaVersion <String>]`: Java 버전입니다.
    - `[LimitMaxDiskSizeInMb <Int64?>]`: 허용되는 최대 디스크 크기 사용량(MB)입니다.
    - `[LimitMaxMemoryInMb <Int64?>]`: 허용되는 최대 메모리 사용량(MB)입니다.
    - `[LimitMaxPercentageCpu <Double?>]`: 허용되는 최대 CPU 사용량 백분율입니다.
    - `[LinuxFxVersion <String>]`: Linux App Framework 및 버전
    - `[LoadBalancing <SiteLoadBalancing?>]`: 사이트 부하 분산.
    - `[LocalMySqlEnabled <Boolean?>]`: <code>true</code> 로컬 MySQL을 사용하도록 설정하려면, 그렇지 않으면 <code>false</code> .
    - `[LogsDirectorySizeLimit <Int32?>]`: HTTP 로그 디렉터리 크기 제한.
    - `[MachineKeyDecryption <String>]`: 암호 해독에 사용되는 알고리즘입니다.
    - `[MachineKeyDecryptionKey <String>]`: 암호 해독 키입니다.
    - `[MachineKeyValidation <String>]`: MachineKey 유효성 검사.
    - `[MachineKeyValidationKey <String>]`: 유효성 검사 키입니다.
    - `[ManagedPipelineMode <ManagedPipelineMode?>]`: 관리되는 파이프라인 모드입니다.
    - `[ManagedServiceIdentityId <Int32?>]`: 관리 서비스 ID ID
    - `[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: SSL 요청에 필요한 TLS의 최소 버전을 구성합니다.
    - `[NetFrameworkVersion <String>]`: .NET Framework 버전.
    - `[NodeVersion <String>]`: Node.js.
    - `[NumberOfWorker <Int32?>]`: 작업자 수입니다.
    - `[PhpVersion <String>]`: PHP 버전입니다.
    - `[PowerShellVersion <String>]`: PowerShell 버전입니다.
    - `[PreWarmedInstanceCount <Int32?>]`: 미리 준비된 인스턴스 수입니다.         이 설정은 소비 및 탄력적 계획에만 적용됩니다.
    - `[PublishingUsername <String>]`: 사용자 이름을 게시합니다.
    - `[PushKind <String>]`: 리소스의 종류입니다.
    - `[PythonVersion <String>]`: Python 버전입니다.
    - `[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> 원격 디버깅을 사용하도록 설정한 경우, 그렇지 않으면 <code>false</code>
    - `[RemoteDebuggingVersion <String>]`: 원격 디버깅 버전입니다.
    - `[RequestCount <Int32?>]`: 요청 수.
    - `[RequestTimeInterval <String>]`: 시간 간격입니다.
    - `[RequestTracingEnabled <Boolean?>]`: <code>true</code> 요청 추적을 사용하도록 설정한 경우, 그렇지 않으면 <code>false</code> .
    - `[RequestTracingExpirationTime <DateTime?>]`: 요청 추적 만료 시간입니다.
    - `[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: SCM에 대한 IP 보안 제한 사항입니다.
    - `[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: scm이 main을 사용하기 위한 IP 보안 제한 사항입니다.
    - `[ScmType <ScmType?>]`: SCM 형식입니다.
    - `[SlowRequestCount <Int32?>]`: 요청 수.
    - `[SlowRequestTimeInterval <String>]`: 시간 간격입니다.
    - `[SlowRequestTimeTaken <String>]`: 시간이 됐습니다.
    - `[TagWhitelistJson <String>]`: 푸시 등록 엔드포인트에서 사용할 수 있는 태그 목록을 포함하는 JSON 문자열을 얻거나 설정합니다.
    - `[TagsRequiringAuth <String>]`: 푸시 등록 엔드포인트에서 사용자 인증을 필요로 하는 태그 목록을 포함하는 JSON 문자열을 얻거나 설정합니다.         태그는 영문자 문자와 '_', '@', '#', '.', ':', '-'로 구성될 수 있습니다.         PushRequestHandler에서 유효성 검사를 수행해야 합니다.
    - `[TracingOption <String>]`: 추적 옵션.
    - `[TriggerPrivateBytesInKb <Int32?>]`: 개인 Bytes를 기반으로 하는 규칙입니다.
    - `[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: 상태 코드를 기반으로 하는 규칙입니다.
      - `[Count <Int32?>]`: 요청 수.
      - `[Status <Int32?>]`: HTTP 상태 코드입니다.
      - `[SubStatus <Int32?>]`: 요청 하위 상태입니다.
      - `[TimeInterval <String>]`: 시간 간격입니다.
      - `[Win32Status <Int32?>]`: Win32 오류 코드입니다.
    - `[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> 32비트 Worker 프로세스를 사용하는 경우. 그렇지 않으면 <code>false</code>
    - `[VirtualApplication <IVirtualApplication[]>]`: 가상 애플리케이션.
      - `[PhysicalPath <String>]`: 물리적 경로입니다.
      - `[PreloadEnabled <Boolean?>]`: <code>true</code> 미리 로드를 사용하도록 설정한 경우, 그렇지 않으면 <code>false</code> .
      - `[VirtualDirectory <IVirtualDirectory[]>]`: 가상 애플리케이션에 대한 가상디렉터리입니다.
        - `[PhysicalPath <String>]`: 물리적 경로입니다.
        - `[VirtualPath <String>]`: 가상 애플리케이션에 대한 경로입니다.
      - `[VirtualPath <String>]`: 가상 경로입니다.
    - `[VnetName <String>]`: Virtual Network 이름입니다.
    - `[WebSocketsEnabled <Boolean?>]`: <code>true</code> WebSocket을 사용하도록 설정한 경우, 그렇지 않으면 <code>false</code> .
    - `[WindowsFxVersion <String>]`: Xenon App Framework 및 버전
    - `[XManagedServiceIdentityId <Int32?>]`: 명시적 관리 서비스 ID ID
  - `[ContainerSize <Int32?>]`: 함수 컨테이너의 크기입니다.
  - `[DailyMemoryTimeQuota <Int32?>]`: 허용되는 최대 일일 메모리 시간 할당량(동적 앱에만 해당)
  - `[Enabled <Boolean?>]`: <code>true</code> 앱이 활성화되어 있는 경우, 그렇지 않은 경우 <code>false</code> . 이 값을 false로 설정하면 앱이 비활성화됩니다(앱을 오프라인으로 전환).
  - `[HostNameSslState <IHostNameSslState[]>]`: 호스트 이름 SSL 상태는 앱의 호스트 이름에 대한 SSL 바인딩을 관리하는 데 사용됩니다.
    - `[HostType <HostType?>]`: 호스트 이름의 표준 또는 리포지토리 호스트 이름인지 여부를 나타냅니다.
    - `[Name <String>]`: 호스트 이름입니다.
    - `[SslState <SslState?>]`: SSL 형식입니다.
    - `[Thumbprint <String>]`: SSL 인증서 지문입니다.
    - `[ToUpdate <Boolean?>]`: 기존 <code>true</code> 호스트 이름을 업데이트할 수 있습니다.
    - `[VirtualIP <String>]`: IP 기반 SSL을 사용하는 경우 호스트 이름에 할당된 가상 IP 주소입니다.
  - `[HostNamesDisabled <Boolean?>]`: 앱의 공용 호스트 이름을 사용하지 않도록 설정하는 <code>true</code> 것입니다. 그렇지 않으면 <code>false</code>          이 경우 앱은 API 관리 <code>true</code> 프로세스를 통해서만 액세스할 수 있습니다.
  - `[HostingEnvironmentProfileId <String>]`: App Service Environment의 리소스 ID입니다.
  - `[HttpsOnly <Boolean?>]`: HttpsOnly: https 요청만 수락하도록 웹 사이트를 구성합니다. http 요청에 대한 문제 리디렉션
  - `[HyperV <Boolean?>]`: Hyper-V 샌드박스.
  - `[IdentityType <ManagedServiceIdentityType?>]`: 관리 서비스 ID의 유형입니다.
  - `[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: 리소스와 연결된 사용자 할당 ID 목록입니다. 사용자 ARM ID 사전 키 참조는 '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName} 형식의 리소스 ID로 설정됩니다.
    - `[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: 이 개체에 추가할 수 있는 속성을 나타냅니다.
  - `[IsXenon <Boolean?>]`: 사용되지 않습니다. Hyper-V 샌드박스.
  - `[RedundancyMode <RedundancyMode?>]`: 사이트 중복 모드
  - `[Reserved <Boolean?>]`: <code>true</code> 예약된 경우, 그렇지 않으면 <code>false</code> .
  - `[ScmSiteAlsoStopped <Boolean?>]`: 앱이 중지된 경우 <code>true</code> SCM(KUDU) 사이트를 중지합니다. 그렇지 않으면 <code>false</code> 기본값은 <code>false</code> .
  - `[ServerFarmId <String>]`: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}"으로 형식이 지정되는 연결된 App Service 계획의 리소스 ID입니다.

## 관련 링크

