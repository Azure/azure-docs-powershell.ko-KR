---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplicationDefinition.md
ms.openlocfilehash: f1f71d188a6b25146103fe3fe5d91b8ba53eaaf8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985637"
---
# Get-AzManagedApplicationDefinition

## SYNOPSIS
관리되는 애플리케이션 정의를 얻습니다.

## 구문

### GetByNameAndResourceGroup(기본값)
```
Get-AzManagedApplicationDefinition [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetById
```
Get-AzManagedApplicationDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Get-AzManagedApplicationDefinition** cmdlet은 관리되는 애플리케이션 정의를 얻습니다.

## 예제

### 예제 1: 리소스 그룹에서 모든 관리되는 애플리케이션 정의를 얻습니다.
```
PS C:\>Get-AzManagedApplicationDefinition -ResourceGroupName "MyRG"
```

이 명령은 리소스 그룹 "MyRG"에서 관리되는 애플리케이션 정의를 얻습니다.

### 예제 2: 관리되는 애플리케이션 정의를 얻게 됩니다.
```
PS C:\>Get-AzManagedApplicationDefinition -ResourceGroupName "MyRG" -Name "myManagedAppDef"
```

이 명령은 리소스 그룹 "MyRG"에서 관리되는 애플리케이션 정의 "myManagedAppDef"를 얻습니다.

## 매개 변수

### -ApiVersion
설정하면 사용할 리소스 공급자 API의 버전을 나타냅니다.
지정하지 않으면 API 버전이 사용 가능한 최신 버전으로 자동으로 결정됩니다.

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

### -Id
구독을 포함하여 완전히 자격을 갖춘 관리되는 애플리케이션 정의 ID입니다.
예: /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}

```yaml
Type: System.String
Parameter Sets: GetById
Aliases: ResourceId, ManagedApplicationDefinitionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
관리되는 애플리케이션 정의 이름입니다.

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Pre
설정하면 cmdlet이 사용할 버전을 자동으로 결정할 때 미리 릴리스 API 버전을 사용해야 한다고 나타냅니다.

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

### -ResourceGroupName
리소스 그룹 이름입니다.

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## 입력

### System.String

## 출력

### System.Management.Automation.PSObject

## 참고 사항

## 관련 링크
