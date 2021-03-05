---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/update-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Update-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Update-AzCloudService.md
ms.openlocfilehash: bb67420e3fbb4479a79c7a837aad3b9a65635d88
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007179"
---
# Update-AzCloudService

## SYNOPSIS
클라우드 서비스를 만들거나 업데이트합니다.
일부 속성은 클라우드 서비스 생성 중에만 설정할 수 있습니다.

## 구문

```
Update-AzCloudService -InputObject <ICloudServiceIdentity> -Parameter <ICloudService>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## 설명
클라우드 서비스를 만들거나 업데이트합니다.
일부 속성은 클라우드 서비스 생성 중에만 설정할 수 있습니다.

## 예제

### 예제 1: 기존 클라우드 서비스에 RDP 확장 추가
```powershell
# Create RDP extension object
PS C:\> $rdpExtension = New-AzCloudServiceRemoteDesktopExtensionObject -Name "RDPExtension" -Credential $credential -Expiration $expiration -TypeHandlerVersion "1.2.1"
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"
# Add RDP extension to existing cloud service extension object
PS C:\> $cloudService.ExtensionProfile.Extension = $cloudService.ExtensionProfile.Extension + $rdpExtension
# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

위의 명령 집합은 ContosOrg라는 리소스 그룹에 속하는 ContosoCS라는 기존 클라우드 서비스에 RDP 확장을 추가합니다.

### 예제 2: 클라우드 서비스에서 모든 확장 제거
```powershell
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"
# Set extension to empty list
PS C:\> $cloudService.ExtensionProfile.Extension = @()
# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

위의 명령 집합은 ContosOrg라는 리소스 그룹에 속하는 ContosoCS라는 기존 클라우드 서비스에서 모든 확장을 제거합니다.

### 예제 3: 클라우드 서비스에서 RDP 확장 제거
```powershell
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"
# Remove extension by name RDPExtension
PS C:\> $cloudService.ExtensionProfile.Extension = $cloudService.ExtensionProfile.Extension | Where-Object { $_.Name -ne "RDPExtension" }
# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

위의 명령 집합은 ContosOrg라는 리소스 그룹에 속하는 ContosoCS라는 기존 클라우드 서비스에서 RDP 확장을 제거합니다.

### 예제 4: Scale-Out/Scale-In 인스턴스
```powershell
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"

# Scale-out all role instance count by 1
PS C:\> $cloudService.RoleProfile.Role | ForEach-Object {$_.SkuCapacity += 1}

# Scale-in ContosoFrontend role instance count by 1
PS C:\> $role = $cloudService.RoleProfile.Role | Where-Object {$_.Name -eq "ContosoFrontend"}
PS C:\> $role.SkuCapacity -= 1

# Update cloud service configuration as per the new role instance count
PS C:\> $cloudService.Configuration = $configuration

# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

위의 명령 집합에서는 ContosOrg라는 리소스 그룹에 속하는 ContosoCS라는 클라우드 서비스에 대한 확장 및 확장 역할 인스턴스 수를 확장하는 방법을 보여줍니다.

## 매개 변수

### -AsJob
작업으로 명령을 실행합니다.

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

### -DefaultProfile
Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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

### -InputObject
ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -NoWait
명령 비동기 실행

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

### -매개 변수
클라우드 서비스를 설명합니다.
구성을 위해 매개 변수 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -확인
cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.

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
cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.
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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## 입력

### Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService

### Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity

## 출력

### Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService

## 참고 사항

별칭

복잡한 매개 변수 속성

아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다. 해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.


INPUTOBJECT <ICloudServiceIdentity> : ID 매개 변수
  - `[CloudServiceName <String>]`: 
  - `[Id <String>]`: 리소스 ID 경로
  - `[ResourceGroupName <String>]`: 
  - `[RoleInstanceName <String>]`: 역할 인스턴스의 이름입니다.
  - `[RoleName <String>]`: 역할의 이름입니다.
  - `[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명입니다. 구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.
  - `[UpdateDomain <Int32?>]`: 업데이트 도메인을 식별하는 정수 값을 지정합니다. 업데이트 도메인은 0 기반 인덱스로 식별됩니다. 첫 번째 업데이트 도메인에는 ID가 0이고, 두 번째 도메인에는 1의 ID가 있습니다.

매개 <ICloudService> 변수 : 클라우드 서비스를 설명합니다.
  - `Location <String>`: 리소스 위치입니다.
  - `[Configuration <String>]`: 클라우드 서비스에 대한 XML 서비스 구성(.cscfg)을 지정합니다.
  - `[ConfigurationUrl <String>]`: Blob 서비스의 서비스 구성 위치를 참조하는 URL을 지정합니다. 서비스 패키지 URL은 모든 저장소 계정의 SAS(공유 액세스 서명) URI일 수 있습니다.         이 속성은 쓰기 전용 속성으로 GET 호출에서 반환되지 않습니다.
  - `[ExtensionProfile <ICloudServiceExtensionProfile>]`: 클라우드 서비스 확장 프로필을 설명합니다.
    - `[Extension <IExtension[]>]`: 클라우드 서비스에 대한 확장 목록입니다.
      - `[AutoUpgradeMinorVersion <Boolean?>]`: 플랫폼이 사용할 수 있는 경우 형식HandlerVersion을 더 높은 부 버전으로 자동으로 업그레이드할 수 있는지 여부를 명시적으로 지정합니다.
      - `[ForceUpdateTag <String>]`: 제공된 공용 및 보호된 설정을 강제 적용하려면 태그를 지정합니다.         태그 값을 변경하면 공개 또는 보호된 설정을 변경하지 않고 확장을 다시 실행할 수 있습니다.         forceUpdateTag가 변경되지 않은 경우 처리기에서 공용 또는 보호된 설정에 대한 업데이트가 계속 적용됩니다.         ForceUpdateTag 또는 공용 또는 보호된 설정이 변경되지 않은 경우 확장은 동일한 시퀀스 번호가 있는 역할 인스턴스로 흐르며 다시 실행할지 여부를 처리기 구현에 따라 결정됩니다.
      - `[Name <String>]`: 확장의 이름입니다.
      - `[ProtectedSetting <String>]`: 역할 인스턴스로 보내기 전에 암호화된 확장에 대한 보호된 설정입니다.
      - `[ProtectedSettingFromKeyVaultSecretUrl <String>]`: 
      - `[Publisher <String>]`: 확장 처리기 게시자의 이름입니다.
      - `[RolesAppliedTo <String[]>]`: 이 확장을 적용할 역할의 선택적 목록입니다. 속성이 지정되지 않은 경우 또는 '*'가 지정되어 있는 경우 클라우드 서비스의 모든 역할에 확장이 적용됩니다.
      - `[Setting <String>]`: 확장에 대한 공용 설정입니다. JSON 확장의 경우 확장에 대한 JSON 설정입니다. XML 확장(예: RDP)의 경우 확장에 대한 XML 설정입니다.
      - `[SourceVaultId <String>]`: 리소스 ID
      - `[Type <String>]`: 확장의 유형을 지정합니다.
      - `[TypeHandlerVersion <String>]`: 확장의 버전을 지정합니다. 확장의 버전을 지정합니다. 이 요소를 지정하지 않은 경우 또는 (*) 를 값으로 사용하는 경우 확장의 최신 버전이 사용됩니다. 값이 주 버전 번호와 부 버전 번호(X)로 지정된 경우 지정된 주 버전의 최신 부 버전이 선택됩니다. 주 버전 번호와 부 버전 번호가 지정된 경우(X.Y) 특정 확장 버전이 선택됩니다. 버전을 지정하면 역할 인스턴스에서 자동 업그레이드가 수행됩니다.
  - `[NetworkProfile <ICloudServiceNetworkProfile>]`: 클라우드 서비스에 대한 네트워크 프로필입니다.
    - `[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: 클라우드 서비스에 대한 부하 균형 조정기 구성 목록입니다.
      - `[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: IP 목록
        - `[Name <String>]`: 
        - `[PrivateIPAddress <String>]`: 클라우드 서비스에서 참조하는 개인 IP 주소입니다.
        - `[PublicIPAddressId <String>]`: 리소스 ID
        - `[SubnetId <String>]`: 리소스 ID
      - `[Name <String>]`: 리소스 이름
    - `[SwappableCloudService <ISubResource>]`: 
      - `[Id <String>]`: 리소스 ID
  - `[OSProfile <ICloudServiceOSProfile>]`: 클라우드 서비스에 대한 OS 프로필을 설명합니다.
    - `[Secret <ICloudServiceVaultSecretGroup[]>]`: 역할 인스턴스에 설치해야 하는 인증서 집합을 지정합니다.
      - `[SourceVaultId <String>]`: 리소스 ID
      - `[VaultCertificate <ICloudServiceVaultCertificate[]>]`: 인증서를 포함하는 SourceVault의 주요 자격 증명 모음 참조 목록입니다.
        - `[CertificateUrl <String>]`: Key Vault에 비밀로 업로드된 인증서의 URL입니다.
  - `[PackageUrl <String>]`: Blob 서비스에서 서비스 패키지의 위치를 참조하는 URL을 지정합니다. 서비스 패키지 URL은 모든 저장소 계정의 SAS(공유 액세스 서명) URI일 수 있습니다.         이 속성은 쓰기 전용 속성으로 GET 호출에서 반환되지 않습니다.
  - `[RoleProfile <ICloudServiceRoleProfile>]`: 클라우드 서비스의 역할 프로필을 설명합니다.
    - `[Role <ICloudServiceRoleProfileProperties[]>]`: 클라우드 서비스에 대한 역할 목록입니다.
      - `[Name <String>]`: 리소스 이름입니다.
      - `[SkuCapacity <Int64?>]`: 클라우드 서비스의 역할 인스턴스 수를 지정합니다.
      - `[SkuName <String>]`: sku 이름입니다. 참고: 클라우드 서비스가 현재 있는 하드웨어에서 새 SKU가 지원되지 않는 경우 클라우드 서비스를 삭제하고 다시하거나 이전 sku로 다시 이동해야 합니다.
      - `[SkuTier <String>]`: 클라우드 서비스의 계층을 지정합니다. 가능한 값은 <br /><br /> **표준** <br /><br /> **기본**
  - `[StartCloudService <Boolean?>]`: (선택 사항) 클라우드 서비스를 만들자마자 시작할지 여부를 나타냅니다. 기본값은 `true` 입니다.         false인 경우 서비스 모델이 여전히 배포되지만 코드는 즉시 실행되지 않습니다. 대신 서비스가 시작을 호출할 때까지 PoweredOff가 됩니다. 이 때 서비스가 시작됩니다. 배포된 서비스는 여전히 전원이 공급되는 경우에도 요금이 청구됩니다.
  - `[Tag <ICloudServiceTags>]`: 리소스 태그입니다.
    - `[(Any) <String>]`: 이 개체에 속성을 추가할 수 있는 경우를 나타냅니다.
  - `[UpgradeMode <CloudServiceUpgradeMode?>]`: 클라우드 서비스에 대한 업데이트 모드입니다. 역할 인스턴스는 서비스가 배포될 때 도메인을 업데이트하기 위해 할당됩니다. 업데이트는 각 업데이트 도메인에서 수동으로 시작하거나 모든 업데이트 도메인에서 자동으로 시작할 수 있습니다.         가능한 값은 <br /><br />**자동**<br /><br />**수동** <br /><br />**동시**<br /><br />         지정하지 않으면 기본값은 자동입니다. 수동으로 설정하면 업데이트를 적용하려면 PUT UpdateDomain을 호출해야 합니다. 자동으로 설정하면 업데이트가 순차적으로 각 업데이트 도메인에 자동으로 적용됩니다.

## 관련 링크

