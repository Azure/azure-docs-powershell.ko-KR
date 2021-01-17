---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 60E0D10F-9B93-45A9-A1FF-5C943B8CA09C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: d450fa7795a530106a72180210d9cb133c7d3047
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492128"
---
# Set-AzSqlServerActiveDirectoryAdministrator

## SYNOPSIS
Azure AD 관리자를 프로비전하여 SQL Server.

## 구문

```
Set-AzSqlServerActiveDirectoryAdministrator [-DisplayName] <String> [[-ObjectId] <Guid>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 설명
**Set-AzSqlServerActiveDirectoryAdministrator** cmdlet은 현재 구독에서 AzureSQL 서버에 대한 Azure AD(Azure Active Directory) 관리자를 프로비전합니다.
한 번의 관리자만 프로비전할 수 있습니다.
Azure AD의 다음 멤버는 관리자 권한으로 프로비전할 SQL Server 있습니다.
- Azure AD의 네이티브 멤버 
- Azure AD의 페더리된 멤버 
- 네이티브 또는 페더리된 멤버인 다른 Azure AD에서 가져온 멤버 
- 보안 그룹으로 만든 Azure AD 그룹(예: Outlook.com, Hotmail.com 또는 Live.com 도메인의 그룹)은 관리자로 지원되지 않습니다.
다른 게스트 계정(예: Gmail.com 또는 Yahoo.com 도메인)은 관리자로 지원되지 않습니다.
관리자 권한으로 전용 Azure AD 그룹을 프로비전하는 것이 좋습니다.

## 예제

### 예제 1: 서버에 대한 관리자 그룹 프로비전
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" 
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- ---------------------------
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b False
```

이 명령은 Server01이라는 서버에 대해 DBAS라는 Azure AD 관리자 그룹을 프로비전합니다.
이 서버는 리소스 그룹 ResourceGroup01과 연결됩니다.

### 예제 2: 서버에 대한 관리자 사용자 프로비전
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "David Chew"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- 
resourcegroup01   server01   David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9 False
```

이 명령은 Azure AD 사용자를 Server01 서버의 관리자로 프로비전합니다.

### 예제 3: ID를 지정하여 관리자 그룹 프로비전
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b False
```

이 명령은 Server01이라는 서버에 대해 DBAS라는 Azure AD 관리자 그룹을 프로비전합니다.
이 명령은 ObjectId 매개 변수에 대한 *ID를 지정합니다.*
이렇게 하면 그룹의 표시 이름이 고유하지 않은 경우에도 명령이 성공합니다.

## PARAMETERS

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

### -DisplayName
이 cmdlet이 프로비전하는 Azure AD 관리자의 표시 이름을 지정합니다.

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
이 cmdlet이 프로비전하는 Azure AD 관리자의 고유 ID를 지정합니다.
표시 이름이 고유하지 않은 경우 이 매개 변수의 값을 지정해야 합니다.

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
서버가 할당된 리소스 그룹의 이름을 지정합니다.

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
이 cmdlet이 관리자를 프로비전하는 SQL Server 이름을 지정합니다.

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### System.String

### System.Guid

## 출력

### Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel

## 참고 사항

## 관련 링크

[Get-AzSqlServerActiveDirectoryAdministrator](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[Remove-AzSqlServerActiveDirectoryAdministrator](./Remove-AzSqlServerActiveDirectoryAdministrator.md)

[Disable-AzSqlServerActiveDirectoryOnlyAuthentication](./Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[SQL 데이터베이스 설명서](https://docs.microsoft.com/azure/sql-database/)


