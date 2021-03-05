---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5287D4DB-2709-4A3C-97D5-DB494CEEFD18
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/set-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 8f8ba0297ac0302e50dfdfdc25ddc3941fb10e34
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987238"
---
# Set-AzTrafficManagerEndpoint

## SYNOPSIS
Traffic Manager 엔드포인트를 업데이트합니다.

## 구문

```
Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Set-AzTrafficManagerEndpoint** cmdlet은 Azure Traffic Manager의 엔드포인트를 업데이트합니다.
이 cmdlet은 로컬 엔드포인트 개체의 설정을 업데이트합니다.
*TrafficManagerEndpoint* 매개 변수를 사용하거나 파이프라인을 사용하여 엔드포인트 개체를 지정할 수 있습니다.

Get-AzTrafficManagerEndpoint cmdlet을 사용하여 엔드포인트를 나타내는 로컬 개체를 얻을 수 있습니다.
개체를 로컬로 수정한 다음 **Set-AzTrafficManagerEndpoint를** 사용하여 변경 내용을 커밋합니다.

## 예제

### 예제 1: 엔드포인트 업데이트
```
PS C:\>$TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "endpoint1" -Type AzureEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> $TrafficManagerEndpoint.Weight = 20
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

첫 번째 명령은 **Get-AzTrafficManagerEndpoint** cmdlet을 사용하여 Azure Traffic Manager 엔드포인트를 얻습니다.
명령은 엔드포인트를 로컬로 $TrafficManagerEndpoint 변수에 저장합니다.

두 번째 명령은 로컬로 엔드포인트를 변경합니다.
이 명령은 엔드포인트 가중치를 20으로 변경합니다.

세 번째 명령은 Traffic Manager의 엔드포인트를 업데이트하여 로컬 값과 $TrafficManagerEndpoint.

## 매개 변수

### -DefaultProfile
Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficManagerEndpoint
로컬 **TrafficManagerEndpoint 개체를 지정합니다.**
이 cmdlet은 Traffic Manager를 업데이트하여 이 로컬 개체와 일치합니다.

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.

## 입력

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint

## 출력

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint

## 참고 사항

## 관련 링크
