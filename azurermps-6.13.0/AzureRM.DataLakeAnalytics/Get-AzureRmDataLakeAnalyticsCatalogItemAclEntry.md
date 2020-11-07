---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticscatalogitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry.md
ms.openlocfilehash: 349fe79bf3ff3bea0097542ee0189b5a1999bd35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703870"
---
# Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry

## SYNOPSIS
Data Lake Analytics에서 카탈로그 또는 카탈로그 항목의 ACL에 있는 항목을 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### GetCatalogAclEntry (기본값)
```
Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetCatalogAclEntryForUserOwner
```
Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetCatalogAclEntryForGroupOwner
```
Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetCatalogItemAclEntry
```
Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> -ItemType <String>
 -Path <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetCatalogItemAclEntryForUserOwner
```
Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner] -ItemType <String>
 -Path <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetCatalogItemAclEntryForGroupOwner
```
Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner] -ItemType <String>
 -Path <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzureRmDataLakeAnalyticsCatalogItemAclEntry** Cmdlet은 Data Lake Analytics에서 카탈로그 또는 카탈로그 항목의 ACL (액세스 제어 목록)에 있는 항목 (ace) 목록을 가져옵니다.

## 예제의

### 예제 1: 카탈로그에 대 한 ACL 가져오기
```powershell
PS C:\> Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla"

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
```

이 명령은 지정 된 Data Lake Analytics 계정의 카탈로그에 대 한 ACL을 가져옵니다.

### 예제 2: 카탈로그에 대 한 사용자 소유자의 ACL 항목 가져오기
```powershell
PS C:\> Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner

Type      Id                                   Permissions
----      --                                   -----------
UserOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

이 명령은 지정 된 Data Lake Analytics 계정의 카탈로그에 대 한 사용자 소유자의 ACL 항목을 가져옵니다.

### 예제 3: 카탈로그에 대 한 그룹 소유자의 ACL 항목 가져오기
```powershell
PS C:\> Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -GroupOwner

Type       Id                                   Permissions
----       --                                   -----------
GroupOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

이 명령은 지정 된 Data Lake Analytics 계정 카탈로그에 대 한 그룹 소유자의 ACL 항목을 가져옵니다.

### 예제 4: 데이터베이스의 ACL 가져오기
```powershell
PS C:\> Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -ItemType Database -Path "databaseName"

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
```

이 명령은 지정 된 Data Lake Analytics 계정의 데이터베이스에 대 한 ACL을 가져옵니다.

### 예제 5: 데이터베이스에 대 한 사용자 소유자의 ACL 항목 가져오기
```powershell
PS C:\> Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner -ItemType Database -Path "databaseName"

Type      Id                                   Permissions
----      --                                   -----------
UserOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

이 명령은 지정 된 Data Lake Analytics 계정 데이터베이스의 사용자 소유자에 대 한 ACL 항목을 가져옵니다.

### 예제 6: 데이터베이스의 그룹 소유자에 대 한 ACL 항목 가져오기
```powershell
PS C:\> Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -GroupOwner -ItemType Database -Path "databaseName"

Type       Id                                   Permissions
----       --                                   -----------
GroupOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

이 명령은 지정 된 Data Lake Analytics 계정 데이터베이스에 대 한 그룹 소유자의 ACL 항목을 가져옵니다.

## 변수

### -계정
Data Lake Analytics 계정 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GroupOwner
그룹 소유자 용 카탈로그의 ACL 항목 가져오기

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetCatalogAclEntryForGroupOwner, GetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ItemType
카탈로그 또는 카탈로그 항목의 유형을 지정 합니다. 이 매개 변수에 허용 되는 값은 다음과 같습니다.
- 카탈로그인
- 데이터

```yaml
Type: System.String
Parameter Sets: GetCatalogItemAclEntry, GetCatalogItemAclEntryForUserOwner, GetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Path
카탈로그 또는 카탈로그 항목의 Data Lake Analytics 경로를 지정 합니다.
경로의 각 부분은 마침표 (.)로 구분 되어야 합니다.

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: GetCatalogItemAclEntry, GetCatalogItemAclEntryForUserOwner, GetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UserOwner
사용자 소유자 용 카탈로그의 ACL 항목을 가져옵니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetCatalogAclEntryForUserOwner, GetCatalogItemAclEntryForUserOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

### DataLakeAnalytics. CatalogPathInstance/.

## 출력

### Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl

## 상속자

## 관련 링크

[U-SQL은 이제 데이터베이스 수준 액세스 제어를 제공 합니다.](https://github.com/Azure/AzureDataLake/blob/master/docs/Release_Notes/2016/2016_08_01/USQL_Release_Notes_2016_08_01.md#u-sql-now-offers-database-level-access-control)

[제거-AzureRmDataLakeAnalyticsCatalogItemAclEntry](Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry.md)

[Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry](Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry.md)
