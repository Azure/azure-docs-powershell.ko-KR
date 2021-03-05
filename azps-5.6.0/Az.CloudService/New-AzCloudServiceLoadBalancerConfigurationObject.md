---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.CloudService/new-AzCloudServiceLoadBalancerConfigurationObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceLoadBalancerConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceLoadBalancerConfigurationObject.md
ms.openlocfilehash: 5d3acb8c03ceae44024ed8c6c52a8ee962c9861c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986183"
---
# New-AzCloudServiceLoadBalancerConfigurationObject

## SYNOPSIS
LoadBalancerConfiguration에 대한 메모리 내 개체 만들기

## 구문

```
New-AzCloudServiceLoadBalancerConfigurationObject
 [-FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>] [-Name <String>] [<CommonParameters>]
```

## 설명
LoadBalancerConfiguration에 대한 메모리 내 개체 만들기

## 예제

### 예제 1: 부하 균형 조정기 구성 개체 만들기
```powershell
PS C:\> $publicIP = Get-AzPublicIpAddress -ResourceGroupName 'ContosoOrg' -Name 'ContosoPublicIP'
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIP.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
```

이 명령은 클라우드 서비스를 만들거나 업데이트하는 데 사용되는 Load Balancer 구성 개체를 만듭니다.
자세한 내용은 New-AzCloudService를 참조합니다.

## 매개 변수

### -FrontendIPConfiguration
FrontendIPConfiguration.
생성을 위해 FRONTENDIPCONFIGURATION 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ILoadBalancerFrontendIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
LoadBalancerConfiguration의 이름입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## 입력

## 출력

### Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.LoadBalancerConfiguration

## 참고 사항

별칭

복잡한 매개 변수 속성

아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다. 해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.


FRONTENDIPCONFIGURATION <ILoadBalancerFrontendIPConfiguration[]>: FrontendIPConfiguration.
  - `[Name <String>]`: 
  - `[PrivateIPAddress <String>]`: 클라우드 서비스에서 참조하는 개인 IP 주소입니다.
  - `[PublicIPAddressId <String>]`: 리소스 ID
  - `[SubnetId <String>]`: 리소스 ID

## 관련 링크

