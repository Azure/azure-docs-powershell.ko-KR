---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 7660F1A2-604D-4488-93F1-CB7C502F135E
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: 6d936e267c734ddd9df12e0feec22b2d6f6c4b65
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056133"
---
# New-AzOperationalInsightsStorageInsight

## SYNOPSIS
작업 영역 내에서 저장소를 파악 합니다.

## 구문과

### ByWorkspaceName (기본값)
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

## 설명은
**새 AzOperationalInsightsStorageInsight** cmdlet은 기존 작업 영역에서 새 저장소를 만듭니다.

## 예제의

### 예제 1: 이름으로 저장소를 파악 하 여 만들기
```
PS C:\>$Storage = Get-AzStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzStorageAccountKey).Value[0]

PS C:\>New-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

첫 번째 명령은 Get-AzStorageAccount cmdlet을 사용 하 여 ContosoStorage 이라는 저장소 계정을 가져오고이를 $Storage 변수에 저장 합니다.
두 번째 명령은 파이프라인 연산자를 사용 하 여 지정 된 저장소 계정 키를 얻은 다음 $StorageKey 변수에 저장 하 여 $Storage의 저장소 계정을 Get-AzStorageAccountKey cmdlet에 전달 합니다. 이 예제에서는 첫 번째 키를 검색 합니다. 다른 항목을 검색 하려면 값 [0] 대신 값 [1]을 사용 합니다.
마지막 명령은 MyWorkspace 라는 작업 영역에서 MyStorageInsight 이라는 저장소 정보를 만듭니다.
이 저장소에서는 지정 된 저장소 계정 리소스의 WADWindowsEventLogsTable 테이블에 있는 데이터를 사용 합니다.

### 예제 2: workspace 개체를 사용 하 여 저장소 통찰력 만들기
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>$Storage = Get-AzStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzStorageAccountKey).Value[0]

PS C:\>New-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

첫 번째 명령은 Get-AzOperationalInsightsWorkspace cmdlet을 사용 하 여 MyWorkspace 라는 작업 영역을 가져오고이를 $Workspace 변수에 저장 합니다.
두 번째 명령은 Get-AzStorageAccount cmdlet을 사용 하 여 지정 된 저장소 계정을 가져오고이를 $Storage 변수에 저장 합니다.
세 번째 명령은 파이프라인 연산자를 사용 하 여 지정 된 키를 가져와 Get-AzStorageAccountKey cmdlet에 $Storage의 저장소 계정을 전달한 다음 $StorageKey 변수에 저장 합니다. 이 예제에서는 첫 번째 키를 검색 합니다. 다른 항목을 검색 하려면 값 [0] 대신 값 [1]을 사용 합니다.
마지막 명령은 $Workspace에 정의 된 작업 영역에서 MyStorageInsight 이라는 저장소 정보를 만듭니다.
저장소 정보 저장소가 지정 된 저장소 계정 리소스의 WADWindowsEventLogsTable 테이블에 있는 데이터를 사용 합니다.

## 변수

### -컨테이너
데이터를 포함 하는 컨테이너의 목록을 지정 합니다.

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
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독

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
사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.

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

### -이름
저장소의 이름을 지정 합니다.

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
작업 영역을 포함 하는 Azure 리소스 그룹의 이름을 지정 합니다.

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
저장소 계정의 선택 키를 지정 합니다.

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
저장소 계정의 Azure 리소스를 지정 합니다.
이는 Get-AzStorageAccount cmdlet을 실행 하 고 결과의 *Id* 매개 변수에 액세스 하 여 검색할 수 있습니다.

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

### -테이블
데이터를 제공 하는 테이블 목록을 지정 합니다.

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

### -작업 영역
새 저장소에 대 한 작업 영역을 지정 합니다.

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
기존 작업 영역의 이름을 지정 합니다.

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

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

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
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.
Cmdlet이 실행 되지 않습니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### OperationalInsights. m a m/작업 영역

### System. 문자열

### System.webserver []

## 출력

### OperationalInsights. PSStorageInsight.

## 상속자

## 관련 링크

[Azure Operational Insights Cmdlet](./Az.OperationalInsights.md)

[Get-AzOperationalInsightsWorkspace](./Get-AzOperationalInsightsWorkspace.md)


