---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/get-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExport.md
ms.openlocfilehash: 13c5a7104c0b9d2d4e11e4fe0a2da772ee271c4c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209357"
---
# Get-AzImportExport

## SYNOPSIS
기존 작업 관련 정보를 얻습니다.

## 구문

### 목록(기본값)
```
Get-AzImportExport [-SubscriptionId <String[]>] [-Filter <String>] [-Top <Int32>] [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### 가져오기
```
Get-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzImportExport -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### List1
```
Get-AzImportExport -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Filter <String>] [-Top <Int32>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## 설명
기존 작업 관련 정보를 얻습니다.

## 예제

### 예제 1: 기본 컨텍스트를 통해 ImportExport 작업 가져오기
```powershell
PS C:\> Get-AzImportExport
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

이 cmdlet은 기본 컨텍스트를 통해 ImportExport 작업을 얻습니다.

### 예제 2: 리소스 그룹 및 작업 이름으로 ImportExport 작업 가져오기
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

이 cmdlet은 리소스 그룹 및 작업 이름으로 ImportExport 작업을 얻습니다.

### 예제 3: 지정된 리소스 그룹의 모든 ImportExport 작업을 나열합니다.
```powershell
PS C:\> Get-AzImportExport -ResourceGroupName ImportTestRG
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

이 cmdlet은 지정된 리소스 그룹의 모든 ImportExport 작업을 나열합니다.

### 예제 4: ID로 ImportExport 작업 가져오기
```powershell
PS C:\> $Id = "/subscriptions/<SubscriptionId>/resourceGroups/ImportTestRG/providers/Microsoft.ImportExport/jobs/test-job"
PS C:\> Get-AzImportExport -InputObject $Id
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

이 cmdlet 목록은 ID로 ImportExport 작업을 가져오는 목록을 제공합니다.

## PARAMETERS

### -AcceptLanguage
응답에 대한 기본 설정 언어를 지정합니다.

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
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Filter
결과를 특정 조건으로 제한하는 데 사용할 수 있습니다.

```yaml
Type: System.String
Parameter Sets: List, List1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
가져오기/내보내기 작업의 이름입니다.

```yaml
Type: System.String
Parameter Sets: Get
Aliases: JobName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹 이름은 사용자 구독 내의 리소스 그룹을 고유하게 식별합니다.

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Azure 사용자의 구독 ID입니다.

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Top
반환해야 하는 작업 수를 지정하는 정수 값입니다.
값은 100을 초과할 수 없습니다.

```yaml
Type: System.Int32
Parameter Sets: List, List1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity

## 출력

### Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse

## 참고 사항

별칭

복합 매개 변수 속성

아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다. 해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.


INPUTOBJECT: <IImportExportIdentity> ID 매개 변수
  - `[Id <String>]`: 리소스 ID 경로
  - `[JobName <String>]`: 가져오기/내보내기 작업의 이름입니다.
  - `[LocationName <String>]`: 위치의 이름입니다. 예를 들어 미국 서부 또는 westus입니다.
  - `[ResourceGroupName <String>]`: 리소스 그룹 이름은 사용자 구독 내의 리소스 그룹을 고유하게 식별합니다.
  - `[SubscriptionId <String>]`: Azure 사용자의 구독 ID입니다.

## 관련 링크

