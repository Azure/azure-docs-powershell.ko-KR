---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 60E0D10F-9B93-45A9-A1FF-5C943B8CA09C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: 76d5c2fc90b4e0e518aa022a97c6b9ce369715db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531803"
---
# Set-AzureRmSqlServerActiveDirectoryAdministrator

## SYNOPSIS
SQL Server 용 Azure AD 관리자를 프로 비전 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Set-AzureRmSqlServerActiveDirectoryAdministrator [-DisplayName] <String> [[-ObjectId] <Guid>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## 설명은
**AzureRmSqlServerActiveDirectoryAdministrator** cmdlet은 현재 구독의 AzureSQL Server에 대 한 azure AD (Azure Active Directory) 관리자를 프로 비전 합니다.

한 번에 하나의 관리자만 프로 비전 할 수 있습니다.

Azure AD의 다음 구성원을 SQL Server 관리자로 구축할 수 있습니다.

- Azure AD의 네이티브 구성원 
- Azure AD의 페더레이션 구성원 
- 기본 또는 페더레이션 구성원 인 다른 Azure 광고에서 가져온 구성원 
- Azure AD 그룹을 보안 그룹으로 만듦

Microsoft 계정 (예: Outlook.com, Hotmail.com 또는 Live.com domains)은 관리자로 지원 되지 않습니다.
Gmail.com 또는 Yahoo.com 도메인에 있는 것과 같은 다른 게스트 계정은 관리자로 지원 되지 않습니다.

전용 Azure AD 그룹을 관리자로 프로 비전 하는 것이 좋습니다.

## 예제의

### 예제 1: 서버에 대 한 관리자 그룹 프로 비전
```
PS C:\>Set-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" 
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

이 명령은 Server01 이라는 서버에 대 한 Dba 라는 Azure AD 관리자 그룹을 프로 비전 합니다.
이 서버는 리소스 그룹 ResourceGroup01 연결 되어 있습니다.

### 예제 2: 서버에 대 한 관리자 사용자 프로 비전
```
PS C:\>Set-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "David Chew"
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
resourcegroup01   server01   David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9
```

이 명령은 Server01 이라는 서버의 관리자로 Azure AD 사용자를 프로 비전 합니다.

### 예제 3: ID를 지정 하 여 관리자 그룹 프로 비전
```
PS C:\>Set-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

이 명령은 Server01 이라는 서버에 대 한 Dba 라는 Azure AD 관리자 그룹을 프로 비전 합니다.
Command는 *ObjectId* 매개 변수에 대 한 ID를 지정 합니다.
이렇게 하면 그룹의 표시 이름이 고유 하지 않은 경우에도 명령이 성공 합니다.

## 변수

### -DisplayName
이 cmdlet이 프로 비전 하는 Azure AD 관리자의 표시 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ObjectId
이 cmdlet이 프로 비전 하는 Azure AD 관리자의 고유 ID를 지정 합니다.
표시 이름이 고유 하지 않은 경우이 매개 변수에 대 한 값을 지정 해야 합니다.

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
서버가 할당 된 리소스 그룹의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServerName
이 cmdlet이 관리자를 프로 비전 하는 SQL Server의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

### ServerActiveDirectoryAdministrator. AzureSqlServerActiveDirectoryAdministratorModel에 대 한

## 상속자

## 관련 링크

[Get-AzureRmSqlServerActiveDirectoryAdministrator](./Get-AzureRmSqlServerActiveDirectoryAdministrator.md)

[제거-AzureRmSqlServerActiveDirectoryAdministrator](./Remove-AzureRmSqlServerActiveDirectoryAdministrator.md)

[SQL 데이터베이스 설명서](https://docs.microsoft.com/azure/sql-database/)


