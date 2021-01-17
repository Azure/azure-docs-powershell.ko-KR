---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2DBAF415-A039-479E-B3CA-E00FD5E476C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyAssignment.md
ms.openlocfilehash: 4d5b230b741deec10daa44dab7e4faa44ac96b61
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490531"
---
# Get-AzPolicyAssignment

## SYNOPSIS
정책 할당을 얻습니다.

## 구문

### DefaultParameterSet(기본값)
```
Get-AzPolicyAssignment [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### NameParameterSet
```
Get-AzPolicyAssignment [-Name <String>] [-Scope <String>] [-PolicyDefinitionId <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### IncludeDescendentParameterSet
```
Get-AzPolicyAssignment [-Scope <String>] [-IncludeDescendent] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### IdParameterSet
```
Get-AzPolicyAssignment -Id <String> [-PolicyDefinitionId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Get-AzPolicyAssignment** cmdlet은 모든 정책 할당 또는 특정 할당을 얻습니다.
이름 및 범위 또는 ID로 얻을 정책 할당을 식별합니다.

## 예제

### 예제 1: 모든 정책 할당을 얻습니다.
```
PS C:\> Get-AzPolicyAssignment
```

이 명령은 모든 정책 할당을 얻습니다.

### 예제 2: 특정 정책 할당을 얻게 됩니다.
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> Get-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
```

첫 번째 명령은 Get-AzResourceGroup cmdlet을 사용하여 ResourceGroup11이라는 리소스 그룹을 $ResourceGroup 변수에 저장합니다.
두 번째 명령은 해당 리소스의 **ResourceId** 속성이 식별하는 범위에 대한 PolicyAssignment07이라는 $ResourceGroup 할당합니다.

### 예제 3: 관리 그룹에 할당된 모든 정책 할당을 얻습니다.
```
PS C:\> $mgId = 'myManagementGroup'
PS C:\> Get-AzPolicyAssignment -Scope '/providers/Microsoft.Management/managementgroups/$mgId'
```

첫 번째 명령은 쿼리할 관리 그룹의 ID를 지정합니다.
두 번째 명령은 ID가 'myManagementGroup'인 관리 그룹에 할당된 모든 정책 할당을 얻습니다.

## PARAMETERS

### -ApiVersion
사용할 리소스 공급자 API의 버전을 지정합니다.
버전을 지정하지 않으면 이 cmdlet은 사용 가능한 최신 버전을 사용하게 됩니다.

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
이 cmdlet에서 얻을 정책 할당에 대한 정식 리소스 ID를 지정합니다.

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IncludeDescendent
반환된 정책 할당 목록에 조상 범위의 할당과 내하원 범위의 할당을 포함하여 주어진 범위와 관련된 모든 할당을 포함하게 합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: IncludeDescendentParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
이 cmdlet이 얻을 정책 할당의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PolicyDefinitionId
이 cmdlet에서 얻을 정책 할당의 정책 정의 ID를 지정합니다.

```yaml
Type: System.String
Parameter Sets: NameParameterSet, IdParameterSet
Aliases:

Required: False
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

### -Scope
이 cmdlet이 얻을 할당에 대해 정책이 적용되는 범위를 지정합니다.

```yaml
Type: System.String
Parameter Sets: NameParameterSet, IncludeDescendentParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### System.String

### System.Management.Automation.SwitchParameter

## 출력

### System.Management.Automation.PSObject

## 참고 사항

## 관련 링크

[New-AzPolicyAssignment](./New-AzPolicyAssignment.md)

[Remove-AzPolicyAssignment](./Remove-AzPolicyAssignment.md)

[Set-AzPolicyAssignment](./Set-AzPolicyAssignment.md)


