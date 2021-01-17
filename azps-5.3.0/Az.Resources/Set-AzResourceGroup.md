---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 4E5C059B-36F3-41C8-9FDB-69F5318CF39B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceGroup.md
ms.openlocfilehash: 0523041357becb38475bb496c94ba1fd48c5acaf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489372"
---
# Set-AzResourceGroup

## SYNOPSIS
리소스 그룹을 수정합니다.

## 구문

### SetByResourceGroupName(기본값)
```
Set-AzResourceGroup -Name <String> [-Tag] <Hashtable> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResourceGroupId
```
Set-AzResourceGroup [-Tag] <Hashtable> -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Set-AzResourceGroup** cmdlet은 리소스 그룹의 속성을 수정합니다.
이 cmdlet을 사용하여 리소스 그룹에 적용된 Azure 태그를 추가, 변경 또는 삭제할 수 있습니다.
이름 매개 *변수를* 지정하여 리소스 그룹 및 *태그* 매개 변수를 식별하여 태그를 수정합니다.
이 cmdlet을 사용하여 리소스 그룹의 이름을 변경할 수 없습니다.

## 예제

### 예제 1: 리소스 그룹에 태그 적용
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{Department="IT"}
```

이 명령은 IT 값이 있는 부서 태그를 기존 태그가 없는 리소스 그룹에 적용합니다.

### 예제 2: 리소스 그룹에 태그 추가
```
PS C:\>$Tags = (Get-AzResourceGroup -Name "ContosoRG").Tags
PS C:\> $Tags
PS C:\> $Tags += @{"Status"="Approved"; "FY2016"=$null}
PS C:\> Set-AzResourceGroup -Name "ContosoRG" -Tag $Tags
PS C:> (Get-AzResourceGroup -Name "ContosoRG").Tags
```

이 예제에서는 Approved 값과 FY2016 태그가 있는 상태 태그를 기존 태그가 있는 리소스 그룹에 추가합니다. 지정한 태그가 기존 태그를 대체하기 때문에 새 태그 컬렉션에 기존 태그를 포함해야 합니다. 또는 태그가 손실됩니다.
첫 번째 명령은 ContosoRG 리소스 그룹을 얻게 하여 dot 메서드를 사용하여 태그 속성의 값을 얻습니다. 이 명령은 태그를 $Tags 저장합니다.
두 번째 명령은 $Tags 변수에서 태그를 얻습니다.
세 번째 명령은 += 할당 연산자를 사용하여 상태 및 FY2016 태그를 변수 변수의 태그 배열에 $Tags 있습니다.
네 번째 명령은 **Set-AzResourceGroup의** *Tag* 매개 변수를 사용하여 $Tags 변수의 태그를 ContosoRG 리소스 그룹에 적용합니다.
다섯 번째 명령은 ContosoRG 리소스 그룹에 적용된 모든 태그를 얻습니다. 출력은 리소스 그룹에 Department 태그와 두 개의 새 태그인 상태 및 FY2015가 있는 것으로 표시됩니다.

### 예제 3: 리소스 그룹에 대한 모든 태그 삭제
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{}
```

이 명령은 ContosoRG 리소스 그룹에서 모든 태그를 삭제하는 빈 해시 테이블 값이 있는 Tag 매개 변수를 지정합니다. 

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

### -Id
수정할 리소스 그룹의 ID를 지정합니다.

```yaml
Type: System.String
Parameter Sets: SetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
수정할 리소스 그룹의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: SetByResourceGroupName
Aliases: ResourceGroupName

Required: True
Position: Named
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
해시 테이블 형식의 키-값 쌍입니다. 예: @{key0="value0";key1=$null;key2="value2"} 태그는 리소스 및 리소스 그룹에 만들고 적용할 수 있는 이름-값 쌍입니다. 리소스 및 그룹에 태그를 할당한 후  Get-AzResource 및 Get-AzResourceGroup 태그 이름 및 값으로 리소스 및 그룹을 검색할 수 있습니다. 태그를 사용하여 부서 또는 비용 센터와 같은 리소스를 분류하거나 리소스에 대한 메모 또는 메모를 추적할 수 있습니다.
태그를 추가하거나 변경하려면 리소스 그룹에 대한 태그 컬렉션을 바꿔야 합니다. 태그를 삭제하려면 삭제하려는 태그를 제외하고 **Get-AzResourceGroup에서** 리소스 그룹에 현재 적용된 모든 태그가 있는 해시 테이블을 입력합니다. 리소스 그룹에서 모든 태그를 삭제하려면 빈 해시 테이블을 `@{}` 지정합니다.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
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

[Get-AzResource](./Get-AzResource.md)

[Get-AzResourceGroup](./Get-AzResourceGroup.md)

[New-AzResourceGroup](./New-AzResourceGroup.md)

[Remove-AzResourceGroup](./Remove-AzResourceGroup.md)
