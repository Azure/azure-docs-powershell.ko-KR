---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 5287D4DB-2709-4A3C-97D5-DB494CEEFD18
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 8856a2f9f1a65d6d312571d75e2400a7dcf30bc0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532198"
---
# Set-AzureRmTrafficManagerEndpoint

## SYNOPSIS
Traffic Manager 끝점을 업데이트 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**Set-AzureRmTrafficManagerEndpoint** Cmdlet은 Azure Traffic Manager의 끝점을 업데이트 합니다.
이 cmdlet은 로컬 끝점 개체에서 설정을 업데이트 합니다.
*TrafficManagerEndpoint* 매개 변수를 사용 하거나 파이프라인을 사용 하 여 끝점 개체를 지정할 수 있습니다.

Get-AzureRmTrafficManagerEndpoint cmdlet을 사용 하 여 끝점을 나타내는 로컬 개체를 가져올 수 있습니다.
개체를 로컬로 수정한 다음 **Set-AzureRmTrafficManagerEndpoint** 를 사용 하 여 변경 내용을 커밋합니다.

## 예제의

### 예제 1: 끝점 업데이트
```
PS C:\>$TrafficManagerEndpoint = Get-AzureRmTrafficManagerEndpoint -Name "endpoint1" -Type AzureEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> $TrafficManagerEndpoint.Weight = 20
PS C:\> Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

첫 번째 명령은 **AzureRmTrafficManagerEndpoint** cmdlet을 사용 하 여 Azure Traffic Manager 끝점을 가져옵니다.
명령은 $TrafficManagerEndpoint 변수에 로컬로 끝점을 저장 합니다.

두 번째 명령은 해당 끝점을 로컬로 변경 합니다.
이 명령은 끝점 가중치를 20으로 변경 합니다.

세 번째 명령은 $TrafficManagerEndpoint의 로컬 값과 일치 하도록 Traffic Manager에서 끝점을 업데이트 합니다.

## 변수

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

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### TrafficManagerEndpoint (Network.)
이 cmdlet은 **TrafficManagerEndpoint** 개체를 허용 합니다.

## 출력

### TrafficManagerEndpoint (Network.)
이 cmdlet은 **TrafficManagerEndpoint** 개체를 반환 합니다.

## 상속자

## 관련 링크

