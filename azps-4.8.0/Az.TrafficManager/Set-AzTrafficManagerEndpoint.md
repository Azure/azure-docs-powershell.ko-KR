---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5287D4DB-2709-4A3C-97D5-DB494CEEFD18
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/set-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 0000a7a1dba5f175d70fb93631176a49a9da2d13
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213137"
---
# Set-AzTrafficManagerEndpoint

## SYNOPSIS
Traffic Manager 끝점을 업데이트 합니다.

## 구문과

```
Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**Set-AzTrafficManagerEndpoint** Cmdlet은 Azure Traffic Manager의 끝점을 업데이트 합니다.
이 cmdlet은 로컬 끝점 개체에서 설정을 업데이트 합니다.
*TrafficManagerEndpoint* 매개 변수를 사용 하거나 파이프라인을 사용 하 여 끝점 개체를 지정할 수 있습니다.

Get-AzTrafficManagerEndpoint cmdlet을 사용 하 여 끝점을 나타내는 로컬 개체를 가져올 수 있습니다.
개체를 로컬로 수정한 다음 **Set-AzTrafficManagerEndpoint** 를 사용 하 여 변경 내용을 커밋합니다.

## 예제의

### 예제 1: 끝점 업데이트
```
PS C:\>$TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "endpoint1" -Type AzureEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> $TrafficManagerEndpoint.Weight = 20
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

첫 번째 명령은 **AzTrafficManagerEndpoint** cmdlet을 사용 하 여 Azure Traffic Manager 끝점을 가져옵니다.
명령은 $TrafficManagerEndpoint 변수에 로컬로 끝점을 저장 합니다.

두 번째 명령은 해당 끝점을 로컬로 변경 합니다.
이 명령은 끝점 가중치를 20으로 변경 합니다.

세 번째 명령은 $TrafficManagerEndpoint의 로컬 값과 일치 하도록 Traffic Manager에서 끝점을 업데이트 합니다.

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

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
로컬 **TrafficManagerEndpoint** 개체를 지정 합니다.
이 cmdlet은이 로컬 개체와 일치 하도록 Traffic Manager를 업데이트 합니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### TrafficManager. TrafficManagerEndpoint/.

## 출력

### TrafficManager. TrafficManagerEndpoint/.

## 상속자

## 관련 링크
