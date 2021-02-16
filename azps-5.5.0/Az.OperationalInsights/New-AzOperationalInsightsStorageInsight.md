---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 7660F1A2-604D-4488-93F1-CB7C502F135E
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: 6d936e267c734ddd9df12e0feec22b2d6f6c4b65
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184097"
---
# New-AzOperationalInsightsStorageInsight

## SYNOPSIS
작업 영역 내에서 Storage 인사이트를 만듭니다.

## 구문

### ByWorkspaceName(기본값)
```
New-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByWorkspaceObject
```
New-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 설명
**New-AzOperationalInsightsStorageInsight** cmdlet은 기존 작업 영역의 새 Storage Insight를 만듭니다.

## 예제

### 예제 1: 이름으로 Storage 인사이트 만들기
```
PS C:\>$Storage = Get-AzStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzStorageAccountKey).Value[0]

PS C:\>New-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

첫 번째 명령은 Get-AzStorageAccount cmdlet을 사용하여 ContosoStorage라는 저장소 계정을 저장한 다음, $Storage 변수에 저장합니다.
두 번째 명령은 파이프라인 연산자를 사용하여 $Storage 저장소 계정 키를 Get-AzStorageAccountKey cmdlet에 저장소 계정을 전달한 다음, $StorageKey 변수에 저장합니다. 이 예제에서는 첫 번째 키를 검색합니다. 다른 값을 검색하기 위해 Value[0] 대신 Value[1]을 사용합니다.
마지막 명령은 MyWorkspace라는 작업 영역의 MyStorageInsight라는 저장소 인사이트를 만듭니다.
이 저장소 인사이트는 지정된 저장소 계정 리소스의 WADWindowsEventLogsTable 테이블의 데이터를 소비합니다.

### 예제 2: 작업 영역 개체를 사용하여 Storage Insight 만들기
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>$Storage = Get-AzStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzStorageAccountKey).Value[0]

PS C:\>New-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

첫 번째 명령은 Get-AzOperationalInsightsWorkspace cmdlet을 사용하여 MyWorkspace라는 작업 영역이 있는 다음, $Workspace 변수에 저장합니다.
두 번째 명령은 Get-AzStorageAccount cmdlet을 사용하여 지정된 저장소 계정을 얻은 다음, $Storage 변수에 저장합니다.
세 번째 명령은 파이프라인 연산자를 사용하여 $Storage 저장소 계정을 Get-AzStorageAccountKey cmdlet에 전달한 다음, $StorageKey 변수에 저장합니다. 이 예제에서는 첫 번째 키를 검색합니다. 다른 값을 검색하기 위해 Value[0] 대신 Value[1]을 사용합니다.
마지막 명령은 MyStorageInsight라는 저장소 인사이트를 이 명령에 정의된 작업 $Workspace.
Storage Insight는 지정된 스토리지 계정 리소스의 WADWindowsEventLogsTable 테이블의 데이터를 소비합니다.

## PARAMETERS

### -Containers
데이터를 포함하는 컨테이너 목록을 지정합니다.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -Name
Storage 인사이트의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
작업 영역이 포함된 Azure 리소스 그룹의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountKey
저장소 계정에 대한 액세스 키를 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountResourceId
저장소 계정의 Azure 리소스를 지정합니다.
이 검색은 Get-AzStorageAccount cmdlet을 실행하고 결과의 *ID* 매개 변수에 액세스하여 검색할 수 있습니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tables
데이터를 제공하는 테이블 목록을 지정합니다.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Workspace
새 Storage 인사이트에 대한 작업 공간을 지정합니다.

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WorkspaceName
기존 작업 영역의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace

### System.String

### System.String[]

## 출력

### Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight

## 참고 사항

## 관련 링크

[Azure Operational Insights Cmdlet](./Az.OperationalInsights.md)

[Get-AzOperationalInsightsWorkspace](./Get-AzOperationalInsightsWorkspace.md)


