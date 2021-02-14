---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/get-AzCloudServicePublicIPAddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServicePublicIPAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServicePublicIPAddress.md
ms.openlocfilehash: 2a3b643a9ad9d9c588589003e5edb24ceddc4ae1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181804"
---
# Get-AzCloudServicePublicIPAddress

## SYNOPSIS
클라우드 서비스의 공용 IP 주소를 얻습니다.

## 구문

### CloudServiceName(기본값)
```
Get-AzCloudServicePublicIPAddress -CloudServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [<CommonParameters>]
```

### CloudService
```
Get-AzCloudServicePublicIPAddress -CloudService <CloudService> [-SubscriptionId <String>] [<CommonParameters>]
```

## 설명
클라우드 서비스의 공용 IP 주소를 얻습니다.

## 예제

### 예제 1: 특정 클라우드 서비스 이름에 대한 인스턴스 수준 공용 IP 주소를 얻습니다.
```powershell
PS C:\> Get-AzCloudServicePublicIPAddress -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca

```

특정 클라우드 서비스 이름에 대한 인스턴스 수준 공용 IP 주소를 얻습니다.

### 예제 2: 주어진 클라우드 서비스 개체에 대한 인스턴스 수준 공용 IP 주소를 얻습니다.
```powershell
PS C:\> $cs = Get-AzCloudService -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca
PS C:\> Get-AzCloudServicePublicIPAddress -CloudService $cs

```

주어진 클라우드 서비스 개체에 대한 인스턴스 수준 공용 IP 주소를 얻습니다.

## PARAMETERS

### -CloudService
CloudService 인스턴스.
생성을 위해 CLOUDSERVICE 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudService
Parameter Sets: CloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CloudServiceName
CloudServiceName.

```yaml
Type: System.String
Parameter Sets: CloudServiceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
ResourceGroupName.

```yaml
Type: System.String
Parameter Sets: CloudServiceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
구독.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

## 출력

## 참고 사항

별칭

복합 매개 변수 속성

아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다. 해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.


CLOUDSERVICE: <CloudService> CloudService 인스턴스.
  - `Location <String>`: 리소스 위치입니다.
  - `[Configuration <String>]`: 클라우드 서비스에 대한 XML 서비스 구성(.cscfg)을 지정합니다.
  - `[ConfigurationUrl <String>]`: Blob service에서 서비스 구성의 위치를 참조하는 URL을 지정합니다. 서비스 패키지 URL은 모든 저장소 계정에서 SAS(공유 액세스 서명) URI일 수 있습니다.         쓰기 전용 속성으로 GET 호출에서 반환되지 않습니다.
  - `[ExtensionProfile <ICloudServiceExtensionProfile>]`: 클라우드 서비스 확장 프로필을 설명합니다.
    - `[Extension <IExtension[]>]`: 클라우드 서비스에 대한 확장 목록입니다.
      - `[AutoUpgradeMinorVersion <Boolean?>]`: 플랫폼이 사용 가능해질 때 typeHandlerVersion을 더 높은 부 버전으로 자동으로 업그레이드할 수 있는지 여부를 명시적으로 지정합니다.
      - `[ForceUpdateTag <String>]`: 제공된 공용 및 보호된 설정을 강제 적용하기 위한 태그입니다.         태그 값을 변경하면 공용 또는 보호된 설정을 변경하지 않고 확장을 다시 실행합니다.         forceUpdateTag가 변경되지 않은 경우 공용 또는 보호된 설정에 대한 업데이트는 처리기에서 계속 적용됩니다.         forceUpdateTag 또는 공용 또는 보호된 설정이 변경되지 않는 경우 확장은 동일한 시퀀스 번호의 역할 인스턴스로 흐르며, 다시 실행할지 여부는 처리기 구현에 따라 결정됩니다.
      - `[Name <String>]`: 확장의 이름입니다.
      - `[ProtectedSetting <String>]`: 역할 인스턴스로 보내기 전에 암호화되는 확장에 대한 보호된 설정입니다.
      - `[ProtectedSettingFromKeyVaultSecretUrl <String>]`: 
      - `[Publisher <String>]`: 확장 처리기 게시자의 이름입니다.
      - `[RolesAppliedTo <String[]>]`: 이 확장을 적용할 역할의 선택적 목록입니다. 속성이 지정되지 않은 경우 또는 '*'를 지정하면 클라우드 서비스의 모든 역할에 확장이 적용됩니다.
      - `[Setting <String>]`: 확장에 대한 공용 설정입니다. JSON 확장의 경우 확장에 대한 JSON 설정입니다. XML 확장(예: RDP)의 경우 확장에 대한 XML 설정입니다.
      - `[SourceVaultId <String>]`: 리소스 ID
      - `[Type <String>]`: 확장의 유형을 지정합니다.
      - `[TypeHandlerVersion <String>]`: 확장의 버전을 지정합니다. 확장의 버전을 지정합니다. 이 요소를 지정하지 않은 경우 또는 값으로 추가(*)를 사용하는 경우 최신 버전의 확장이 사용됩니다. 값이 주 버전 번호와 부 버전 번호(X.)로 지정된 경우 지정된 주 버전의 최신 부 버전이 선택됩니다. 주 버전 번호와 부 버전 번호(X.Y)가 지정되면 특정 확장 버전이 선택됩니다. 버전이 지정된 경우 역할 인스턴스에서 자동 업그레이드가 수행됩니다.
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
      - `[VaultCertificate <ICloudServiceVaultCertificate[]>]`: 인증서를 포함하는 SourceVault의 키 자격 증명 모음 참조 목록입니다.
        - `[CertificateUrl <String>]`: Key Vault에 비밀로 업로드된 인증서의 URL입니다.
  - `[PackageUrl <String>]`: Blob service에서 서비스 패키지의 위치를 참조하는 URL을 지정합니다. 서비스 패키지 URL은 모든 저장소 계정에서 SAS(공유 액세스 서명) URI일 수 있습니다.         쓰기 전용 속성으로 GET 호출에서 반환되지 않습니다.
  - `[RoleProfile <ICloudServiceRoleProfile>]`: 클라우드 서비스에 대한 역할 프로필을 설명합니다.
    - `[Role <ICloudServiceRoleProfileProperties[]>]`: 클라우드 서비스에 대한 역할 목록입니다.
      - `[Name <String>]`: 리소스 이름입니다.
      - `[SkuCapacity <Int64?>]`: 클라우드 서비스의 역할 인스턴스 수를 지정합니다.
      - `[SkuName <String>]`: SKU 이름입니다. 참고: 클라우드 서비스가 현재 있는 하드웨어에서 새 SKU가 지원되지 않는 경우 클라우드 서비스를 삭제하고 다시 새로 고치거나 이전 SKU로 다시 이동해야 합니다.
      - `[SkuTier <String>]`: 클라우드 서비스의 계층을 지정합니다. 가능한 값은 <br /><br /> **표준** <br /><br /> **기본**
  - `[StartCloudService <Boolean?>]`: (선택 사항) 클라우드 서비스를 만든 직후 시작할지 여부를 나타냅니다. 기본값은 `true` .         false이면 서비스 모델이 여전히 배포되지만 코드는 즉시 실행되지 않습니다. 대신, 서비스가 시작될 때 시작을 호출할 때까지 PoweredOff입니다. 배포된 서비스는 전원이 공급되는 경우에도 요금이 계속 부과됩니다.
  - `[Tag <ICloudServiceTags>]`: 리소스 태그입니다.
    - `[(Any) <String>]`: 이 개체에 추가할 수 있는 속성을 나타냅니다.
  - `[UpgradeMode <CloudServiceUpgradeMode?>]`: 클라우드 서비스에 대한 업데이트 모드입니다. 역할 인스턴스는 서비스가 배포될 때 도메인을 업데이트하기 위해 할당됩니다. 업데이트는 각 업데이트 도메인에서 수동으로 시작하거나 모든 업데이트 도메인에서 자동으로 시작할 수 있습니다.         가능한 값은 <br /><br />**자동**<br /><br />**수동** <br /><br />**동시**<br /><br />         지정하지 않으면 기본값은 자동입니다. Manual로 설정된 경우 PUT UpdateDomain을 호출하여 업데이트를 적용해야 합니다. 자동으로 설정하면 업데이트가 순서대로 각 업데이트 도메인에 자동으로 적용됩니다.

## 관련 링크

