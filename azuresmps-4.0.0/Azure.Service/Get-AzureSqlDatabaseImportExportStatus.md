---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 4661C479-6E3B-425D-B9D2-B36D7A83130C
online version: ''
schema: 2.0.0
ms.openlocfilehash: c3c55ebd22337a8078f3ae495b3901317f4201e0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046294"
---
# Get-AzureSqlDatabaseImportExportStatus

## SYNOPSIS
가져오기 또는 내보내기 요청의 상태를 가져옵니다.

## 구문과

### ByConnectionInfo
```
Get-AzureSqlDatabaseImportExportStatus -Username <String> -Password <String> -ServerName <String>
 -RequestId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByRequestObject
```
Get-AzureSqlDatabaseImportExportStatus -Request <ImportExportRequest> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## 설명은
**Get-AzureSqlDatabaseImportExportStatus** cmdlet은 가져오기 또는 내보내기 요청의 상태를 가져옵니다.
Start-AzureSqlDatabaseImport 또는 Start-AzureSqlDatabaseExport cmdlet이 요청을 시작 합니다.
*요청 매개 변수* 를 사용 하 여 요청 개체를 지정 하거나 *RequestId* 매개 변수 및 *Username* , *Password* , *ServerName* 매개 변수를 사용 하 여 요청을 식별할 수 있습니다.

## 예제의

### 예제 1: 내보내기 요청의 상태 가져오기
```
PS C:\> $ExportRequest = Start-AzureSqlDatabaseExport -SqlConnectionContext $SqlContext -StorageContainer $Container -DatabaseName $DatabaseName -BlobName $BlobName
PS C:\> Get-AzureSqlDatabaseImportExportStatus -Request $ExportRequest
```

첫 번째 명령은 내보내기 요청을 만든 다음 $ExportRequest 변수에 저장 합니다.

두 번째 명령은 $ExportRequest에 저장 된 내보내기 요청의 상태를 가져옵니다.

## 변수

### -암호
Azure SQL 데이터베이스 서버에 연결 하는 데 필요한 암호를 지정 합니다.
*RequestId* 매개 변수를 지정한 경우이 매개 변수를 지정 해야 합니다.

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -프로필
이 cmdlet이 읽는 Azure 프로필을 지정 합니다.
프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -요청
**Importexportrequest** 개체를 지정 합니다.
가져오기 또는 내보내기 요청 개체를 가져오려면 Start-AzureSqlDatabaseImport 또는 Start-AzureSqlDatabaseExport cmdlet을 사용 합니다.

```yaml
Type: ImportExportRequest
Parameter Sets: ByRequestObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RequestId
이 cmdlet이 상태를 가져오는 가져오기 또는 내보내기 작업의 GUID를 지정 합니다.
이 매개 변수를 지정 하는 경우 *UserName* , *Password* , *ServerName* 매개 변수를 지정 해야 합니다.

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerName
Azure SQL 데이터베이스 서버의 이름을 지정 합니다.
*RequestId* 매개 변수를 지정한 경우이 매개 변수를 지정 해야 합니다.

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -사용자 이름
Azure SQL 데이터베이스 서버에 연결 하는 데 필요한 사용자 이름을 지정 합니다.
*RequestId* 매개 변수를 지정한 경우이 매개 변수를 지정 해야 합니다.

```yaml
Type: String
Parameter Sets: ByConnectionInfo
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

## 출력

### WindowsAzure. SqlDatabase. *. StatusInfo

## 상속자

## 관련 링크

[Azure SQL 데이터베이스](https://azure.microsoft.com/en-us/services/sql-database/)

[가져오기/내보내기 데이터베이스 상태 가져오기](https://msdn.microsoft.com/en-us/library/azure/dn781289.aspx)

[Azure SQL 데이터베이스에 대 한 작업](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[시작-AzureSqlDatabaseExport](./Start-AzureSqlDatabaseExport.md)

[시작-AzureSqlDatabaseImport](./Start-AzureSqlDatabaseImport.md)


