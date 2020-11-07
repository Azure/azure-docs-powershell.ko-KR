---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: ED37B17D-C513-422A-89EA-A6AF1C9A5FEE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermcontainerserviceagentpoolprofile
schema: 2.0.0
ms.openlocfilehash: 2bbc7d9e1ac125134931be483d3a693252ce12d0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882321"
---
# Remove-AzureRmContainerServiceAgentPoolProfile

## SYNOPSIS
컨테이너 서비스에서 에이전트 풀 프로필을 제거 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Remove-AzureRmContainerServiceAgentPoolProfile [-ContainerService] <PSContainerService> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**제거-AzureRmContainerServiceAgentPoolProfile** cmdlet은 컨테이너 서비스에서 에이전트 풀 프로필을 제거 합니다.

## 예제의

### 예제 1: 컨테이너 서비스에서 프로필 제거
```
PS C:\> $Container = Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" 
PS C:\> Remove-AzureRmContainerServiceAgentPoolProfile -ContainerService $Container -Name "AgentPool01"
```

첫 번째 명령은 Get-AzureRmContainerService cmdlet을 사용 하 여 CSResourceGroup17 이라는 컨테이너 서비스를 가져옵니다.
명령이 $Container 변수에 서비스를 저장 합니다.

두 번째 명령은 $Container에서 컨테이너 서비스의 AgentPool01 이라는 프로필을 제거 합니다.

## 변수

### -ContainerService
이 cmdlet에서 에이전트 풀 프로필을 제거 하는 컨테이너 서비스 개체를 지정 합니다.

```yaml
Type: PSContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
이 cmdlet이 제거 하는 에이전트 풀 프로필의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다. Cmdlet이 실행 되지 않습니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### ContainerService
' ContainerService ' 매개 변수는 파이프라인에서 ' ContainerService ' 형식의 값을 허용 합니다.

## 출력

### PSContainerService의. m a.

## 상속자

## 관련 링크

[추가-AzureRmContainerServiceAgentPoolProfile](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[Get-AzureRmContainerService](./Get-AzureRmContainerService.md)


