---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0632DAD6-F331-454F-9E7E-2164AB413E77
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroup.md
ms.openlocfilehash: 9c4bdfe189c16f3e2f6f90d3197149bdc57c78c8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357960"
---
# New-AzResourceGroup

## SYNOPSIS
Azure 리소스 그룹을 만듭니다.

## 구문

```
New-AzResourceGroup [-Name] <String> [-Location] <String> [-Tag <Hashtable>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명
**New-AzResourceGroup** cmdlet은 Azure 리소스 그룹을 만듭니다.
이름 및 위치만 사용하여 리소스 그룹을 만든 다음 New-AzResource cmdlet을 사용하여 리소스 그룹에 추가할 리소스를 만들 수 있습니다.
기존 리소스 그룹에 배포를 추가하기 위해 New-AzResourceGroupDeployment cmdlet을 사용 합니다. 기존 리소스 그룹에 리소스를 추가하기 위해 **New-AzResource** cmdlet을 사용 합니다. Azure 리소스는 데이터베이스 서버, 데이터베이스 또는 웹 사이트와 같은 사용자 관리 Azure 엔터티입니다. Azure 리소스 그룹은 단위로 배포되는 Azure 리소스의 컬렉션입니다.

## 예제

### 예제 1: 빈 리소스 그룹 만들기
```
PS> New-AzResourceGroup -Name RG01 -Location "South Central US"
```

이 명령은 리소스가 없는 리소스 그룹을 만듭니다. **New-AzResource** 또는 **New-AzResourceGroupDeployment** cmdlet을 사용하여 리소스 및 배포를 이 리소스 그룹에 추가할 수 있습니다.

### 예제 2: 위치 매개 변수를 사용하여 빈 리소스 그룹 만들기
```
PS> New-AzResourceGroup RG01 "South Central US"
```

이 명령은 리소스가 없는 리소스 그룹을 만듭니다.

### 예제 3: 태그가 있는 리소스 그룹 만들기
```
PS> New-AzResourceGroup -Name RG01 -Location "South Central US" -Tag @{Empty=$null; Department="Marketing"}
```

이 명령은 빈 리소스 그룹을 만듭니다. 이 명령은 리소스 그룹에 태그를 할당하는 것을 제외하고 예제 1의 명령과 동일합니다. 빈이라는 이름의 첫 번째 태그를 사용하여 리소스가 없는 리소스 그룹을 식별할 수 있습니다. 두 번째 태그는 Department라는 이름의 마케팅 값을 습니다. 이와 같은 태그를 사용하여 관리 또는 예산을 위한 리소스 그룹을 분류할 수 있습니다.

## PARAMETERS

### -ApiVersion
리소스 공급자가 지원하는 API 버전을 지정합니다.
기본 버전과 다른 버전을 지정할 수 있습니다.

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

### -DefaultProfile
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독

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

### -Force
사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.

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

### -Location
리소스 그룹의 위치를 지정합니다. 미국 서부 또는 동남 아시아와 같은 Azure 데이터 센터 위치를 지정합니다. 리소스 그룹을 모든 위치에 위치할 수 있습니다. 리소스 그룹은 Azure 구독과 동일한 위치 또는 리소스와 동일한 위치에 있을 수 없습니다.
각 리소스 종류를 지원하는 위치를 결정하기 위해 *ProviderNamespace* 매개 Get-AzResourceProvider cmdlet을 사용합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
리소스 그룹의 이름을 지정합니다. 리소스 이름은 구독에서 고유해야 합니다. 해당 이름이 있는 리소스 그룹이 이미 있는 경우 명령은 기존 리소스 그룹을 바꾸기 전에 확인을 요청하는 메시지를 표시합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Pre
이 cmdlet은 사용할 버전을 자동으로 결정할 때 릴리스 전 API 버전을 고려합니다.

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

### -Tag
해시 테이블 형식의 키-값 쌍입니다. 예: @{key0="value0";key1=$null;key2="value2"} 태그를 추가하거나 변경하려면 리소스 그룹에 대한 태그 컬렉션을 바꿔야 합니다.
리소스 및 그룹에 태그를 할당한 후  Get-AzResource 및 Get-AzResourceGroup 태그 이름 또는 이름 및 값으로 리소스 및 그룹을 검색할 수 있습니다. 태그를 사용하여 부서 또는 비용 센터와 같은 리소스를 분류하거나 리소스에 대한 메모 또는 메모를 추적할 수 있습니다.
미리 정의한 태그를 얻습니다. Get-AzTag cmdlet을 사용 합니다.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### System.String

### System.Collections.Hashtable

## 출력

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup

## 참고 사항

## 관련 링크

[Get-AzResourceProvider](./Get-AzResourceProvider.md)

[Get-AzResourceGroup](./Get-AzResourceGroup.md)

[New-AzResource](./New-AzResource.md)

[New-AzResourceGroupDeployment](./New-AzResourceGroupDeployment.md)

[Remove-AzResourceGroup](./Remove-AzResourceGroup.md)

[Set-AzResourceGroup](./Set-AzResourceGroup.md)
