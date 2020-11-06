---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerinstance/remove-azurermcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Remove-AzureRmContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Remove-AzureRmContainerGroup.md
ms.openlocfilehash: 80343713c9bf7a0e34a1d9a3b3b75825cbb97a12
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536047"
---
# Remove-AzureRmContainerGroup

## SYNOPSIS
컨테이너 그룹을 제거 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### RemoveContainerGroupByResourceGroupAndNameParamSet (기본값)
```
Remove-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveContainerGroupByPSContainerGroupParamSet
```
Remove-AzureRmContainerGroup -InputObject <PSContainerGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveContainerGroupByResourceIdParamSet
```
Remove-AzureRmContainerGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**제거-AzureRmContainerGroup** cmdlet은 컨테이너 그룹을 제거 합니다.

## 예제의

### 예제 1: 컨테이너 그룹 제거
```
PS C:\> Remove-AzureRmContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer
```

이 명령은 지정 된 컨테이너 그룹을 제거 합니다.

### 예제 2: 파이프를 기준으로 컨테이너 그룹 제거
```
PS C:\> Get-AzureRmContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer | Remove-AzureRmContainerGroup
```

이 명령은 파이프를 기준으로 컨테이너 그룹을 제거 합니다.

### 예제 3: 리소스 Id를 기준으로 컨테이너 그룹을 제거 합니다.
```
PS C:\> Find-AzureRmResource -ResourceGroupEquals MyResourceGroup -ResourceNameEquals MyContainer | Remove-AzureRmContainerGroup
```

이 명령은 리소스 Id를 기준으로 컨테이너 그룹을 제거 합니다.

## 변수

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

### -InputObject
제거할 컨테이너 그룹입니다.

```yaml
Type: PSContainerGroup
Parameter Sets: RemoveContainerGroupByPSContainerGroupParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -이름
컨테이너 그룹 이름입니다.

```yaml
Type: String
Parameter Sets: RemoveContainerGroupByResourceGroupAndNameParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
{{Fill PassThru 설명}}

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹 이름입니다.

```yaml
Type: String
Parameter Sets: RemoveContainerGroupByResourceGroupAndNameParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
리소스 id입니다.

```yaml
Type: String
Parameter Sets: RemoveContainerGroupByResourceIdParamSet
Aliases:

Required: True
Position: Named
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
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.
Cmdlet이 실행 되지 않습니다.

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

### System. 문자열
ContainerInstance. PSContainerGroup/.

## 출력

### ContainerInstance. PSContainerGroup/.

## 상속자

## 관련 링크
