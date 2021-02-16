---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/get-azimportexportlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportLocation.md
ms.openlocfilehash: c603c01619128d1697256174e9d0bc00a1cea8ff
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209344"
---
# Get-AzImportExportLocation

## SYNOPSIS
가져오기 또는 내보내기 작업과 연결된 디스크를 배송할 수 있는 위치에 대한 세부 정보를 반환합니다.
위치는 Azure 지역입니다.

## 구문

### 목록(기본값)
```
Get-AzImportExportLocation [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### 가져오기
```
Get-AzImportExportLocation -Name <String> [-AcceptLanguage <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzImportExportLocation -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## 설명
가져오기 또는 내보내기 작업과 연결된 디스크를 배송할 수 있는 위치에 대한 세부 정보를 반환합니다.
위치는 Azure 지역입니다.

## 예제

### 예제 1: 기본 컨텍스트를 사용하여 모든 Azure 지역 위치 세부 정보 얻기
```powershell
PS C:\> Get-AzImportExportLocation
Name                 Type
----                 ----
Australia East       Microsoft.ImportExport/locations
Australia Southeast  Microsoft.ImportExport/locations
Brazil South         Microsoft.ImportExport/locations
Canada Central       Microsoft.ImportExport/locations
Canada East          Microsoft.ImportExport/locations
...
West Central US      Microsoft.ImportExport/locations
West Europe          Microsoft.ImportExport/locations
West India           Microsoft.ImportExport/locations
West US              Microsoft.ImportExport/locations
West US 2            Microsoft.ImportExport/locations
```

이 cmdlet은 기본 컨텍스트를 사용하여 모든 Azure 지역 위치 세부 정보를 얻습니다.

### 예제 2: 위치 이름으로 Azure 지역 위치 세부 정보 확인
```powershell
PS C:\> Get-AzImportExportLocation -Name eastus
Name    Type
----    ----
East US Microsoft.ImportExport/locations
```

이 cmdlet은 위치 이름으로 Azure 지역 위치 세부 정보를 얻습니다.

### 예제 3: ID별로 Azure 지역 위치 세부 정보 확인
```powershell
PS C:\> $Id = "/providers/Microsoft.ImportExport/locations/eastus"
PS C:\> Get-AzImportExportLocation -InputObject $Id
Name    Type
----    ----
East US Microsoft.ImportExport/locations
```

이 cmdlet 목록은 ID별로 Azure 지역 위치 세부 정보를 얻습니다.

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
위치의 이름입니다.
예를 들어 미국 서부 또는 westus입니다.

```yaml
Type: System.String
Parameter Sets: Get
Aliases: LocationName

Required: True
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

### Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.ILocation

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

