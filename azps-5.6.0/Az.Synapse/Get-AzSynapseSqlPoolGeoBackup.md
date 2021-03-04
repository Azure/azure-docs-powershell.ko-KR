---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqlpoolgeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolGeoBackup.md
ms.openlocfilehash: d1c0b6439b148d51506861a6bfffc6a6681343ef
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957867"
---
# Get-AzSynapseSqlPoolGeoBackup

## SYNOPSIS
Sql Pool의 지역 중복 백업을 얻습니다.

## 구문

### GetByNameParameterSet(기본값)
```
Get-AzSynapseSqlPoolGeoBackup [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SqlPoolGeoBackupResourceId
```
Get-AzSynapseSqlPoolGeoBackup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명
**Get-AzSynapseSqlPoolGeoBackup** cmdlet은 지정된 작업 영역의 SQL 풀 또는 사용 가능한 모든 지역 중복 백업의 지정된 지역 중복 백업을 얻습니다.
지역 중복 백업은 별도의 지리적 위치에서 데이터 파일을 사용하여 복원 가능한 리소스입니다.
새 지역으로 Geo-Restore 지역 정전이 발생하면 지역 중복 백업을 복원하여 Sql Pool을 복구할 수 있습니다.

## 예제

### 예제 1: 지정된 지역 중복 백업을 얻게 됩니다.
```powershell
PS C:\> Get-AzSynapseSqlPoolGeoBackup -ResourceGroupName ContosoResourceGroup -WorkspaceName "ContosoWorkspace" -Name "ContosoSqlPool"
```
cmdlet은 SQL 풀에 대한 지역 백업을 검색합니다.

### 예제 2: 작업 영역의 모든 지역 중복 백업 사용
```
PS C:\>Get-AzSynapseSqlPoolGeoBackup -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```
이 명령은 지정된 작업 영역의 사용 가능한 모든 지역 중복 백업을 제공합니다.

### 예제 3: 필터링을 사용하여 작업 영역의 모든 지역 중복 백업 사용
```
PS C:\>Get-AzSynapseSqlPoolGeoBackup -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -Name "Contoso*"
```
이 명령은 "Contoso"로 시작하는 지정된 작업 영역의 사용 가능한 모든 지역 중복 백업을 얻습니다.

## 매개 변수

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

### -Name
Synapse Sql 풀입니다.

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: The Synapse Sql pool.

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Sql Pool 지역 백업 리소스 ID를 입력합니다.

```yaml
Type: System.String
Parameter Sets: SqlPoolGeoBackupResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹 이름입니다.

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WorkspaceName
Synapse 작업 영역의 이름입니다.

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## 입력

### Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace

### Microsoft.Azure.Commands.Synapse.Models.PSSynapseResourceGroup

## 출력

### Microsoft.Azure.Commands.Synapse.Models.PSBackupModel

## 참고 사항

## 관련 링크
