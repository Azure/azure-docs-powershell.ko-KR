---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 5EE936CA-DD9A-4BC6-B835-E22AE633B46D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4bc7c8f39f1bdbd35cfffeb59b3b4f184f30845e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045427"
---
# Start-AzureSqlDatabaseImport

## SYNOPSIS
Blob 저장소에서 Azure SQL 데이터베이스로 가져오기 작업을 시작 합니다.

## 구문과

### ByContainerObject
```
Start-AzureSqlDatabaseImport -SqlConnectionContext <ISqlServerConnectionInformation>
 -StorageContainer <AzureStorageContainer> -DatabaseName <String> -BlobName <String>
 [-Edition <DatabaseEdition>] [-DatabaseMaxSize <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByContainerName
```
Start-AzureSqlDatabaseImport -SqlConnectionContext <ISqlServerConnectionInformation>
 -StorageContext <IStorageContext> -StorageContainerName <String> -DatabaseName <String> -BlobName <String>
 [-Edition <DatabaseEdition>] [-DatabaseMaxSize <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**AzureSqlDatabaseImport** Cmdlet은 azure Blob Storage에서 Azure SQL 데이터베이스로 가져오기 작업을 시작 합니다.
데이터베이스가 없는 경우이 cmdlet은 사용자가 지정한 크기와 버전 값을 사용 하 여 데이터베이스를 만듭니다.
작업에 데이터베이스 서버 연결 컨텍스트가 필요 합니다.
Get-AzureSqlDatabaseImportExportStatus cmdlet을 사용 하 여 가져오기 작업의 상태를 가져옵니다.

## 예제의

### 예제 1: 데이터베이스 가져오기
```
PS C:\>$Credential = Get-Credential
PS C:\> $SqlContext = New-AzureSqlDatabaseServerContext -ServerName $ServerName -Credentials $Credential
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName $StorageName -StorageAccountKey $StorageKey
PS C:\> $Container = Get-AzureStorageContainer -Name $ContainerName -Context $StorageContext
PS C:\> $ImportRequest = Start-AzureSqlDatabaseImport -SqlConnectionContext $SqlContext -StorageContainer $Container -DatabaseName $DatabaseName -BlobName $BlobName
```

이 예제에서는 $BlobName 변수의 Blob 저장소에서 DatabaseName 이라는 Azure SQL 데이터베이스에 가져오기 프로세스를 시작 합니다.

## 변수

### -BlobName
이 cmdlet에서 데이터베이스를 가져오는 Azure Blob 저장소의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseMaxSize
데이터베이스의 최대 크기 (기가바이트)를 지정 합니다.
데이터베이스가 없는 경우이 cmdlet은이 최대 크기를 기준으로 생성 합니다.
허용 되는 값은 버전에 따라 다릅니다.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseName
데이터베이스의 이름을 지정 합니다.
데이터베이스가 없는 경우이 cmdlet은 데이터베이스를 만들고이 매개 변수에서 지정 하는 이름을 할당 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -에디션
데이터베이스의 버전을 지정 합니다.
데이터베이스가 없으면이 cmdlet이이 버전으로 생성 합니다.
유효한 값은 다음과 같습니다. 

- 않아야
- 웹 
- 조직 
- 기본적
- 표준이
- Premium

기본값은 웹입니다.

```yaml
Type: DatabaseEdition
Parameter Sets: (All)
Aliases: 

Required: False
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

### -SqlConnectionContext
데이터베이스를 포함 하는 서버의 연결 컨텍스트를 지정 합니다.

```yaml
Type: ISqlServerConnectionInformation
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageContainer
이 cmdlet에서 데이터베이스를 가져오는 Blob을 포함 하는 저장소 컨테이너를 지정 합니다.

```yaml
Type: AzureStorageContainer
Parameter Sets: ByContainerObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageContainerName
Blob 저장소 컨테이너의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: ByContainerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageContext
Blob 저장소 컨테이너의 컨텍스트를 지정 합니다.

```yaml
Type: IStorageContext
Parameter Sets: ByContainerName
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

### SqlDatabase. WindowsAzure Exportrequest.

## 상속자

## 관련 링크

[Azure SQL 데이터베이스](https://azure.microsoft.com/en-us/services/sql-database/)

[데이터베이스 가져오기](https://msdn.microsoft.com/en-us/library/azure/dn781284.aspx)

[Azure SQL 데이터베이스에 대 한 작업](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Get-AzureSqlDatabaseImportExportStatus](./Get-AzureSqlDatabaseImportExportStatus.md)

[시작-AzureSqlDatabaseExport](./Start-AzureSqlDatabaseExport.md)


