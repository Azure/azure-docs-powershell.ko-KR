---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B5A2F2A8-5D20-47E4-AFC5-44F687142A08
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4e40d833125725f0ae1baff920a283112db24cdc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045864"
---
# Set-AzureSqlDatabaseServer

## SYNOPSIS
Azure SQL 데이터베이스 서버의 속성을 수정 합니다.

## 구문과

```
Set-AzureSqlDatabaseServer -ServerName <String> -AdminPassword <String> [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**AzureSqlDatabaseServer** cmdlet은 지정 된 Azure SQL 데이터베이스 서버의 인스턴스 속성을 수정 합니다.
현재 릴리스에서는 서버에 대 한 관리자 계정 암호만 업데이트할 수 있습니다.

## 예제의

### 예제 1: 서버의 암호 변경
```
PS C:\>Set-AzureSqlDatabaseServer -ServerName "lpqd0zbr8y" -AdminPassword "NewPassword"
```

이 명령은 lpqd0zbr8y 이라는 Azure SQL 데이터베이스 서버에 대 한 관리자 계정 암호를 변경 합니다.

## 변수

### -AdminPassword
Azure SQL 데이터베이스 서버에 대 한 관리자 계정 암호를 지정 합니다.
강력한 암호를 지정 해야 합니다.
자세한 내용은 Microsoft 개발자 네트워크에서 [강력한 암호](https://go.microsoft.com/fwlink/p/?LinkId=154152) 를 참조 하세요 https://go.microsoft.com/fwlink/p/?LinkId=154152) .

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

### -Force
사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.

```yaml
Type: SwitchParameter
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

### -ServerName
이 cmdlet이 수정 하는 서버의 이름을 지정 합니다.
정규화 된 DNS 이름이 아니라 서버 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

```yaml
Type: SwitchParameter
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### WindowsAzure. SqlDatabase. SqlDatabaseServerContext

## 출력

## 상속자

## 관련 링크

[Azure SQL 데이터베이스](https://azure.microsoft.com/en-us/services/sql-database/)

[Azure SQL 데이터베이스에 대 한 작업](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Get-AzureSqlDatabaseServer](./Get-AzureSqlDatabaseServer.md)

[새로운 AzureSqlDatabaseServer](./New-AzureSqlDatabaseServer.md)

[제거-AzureSqlDatabaseServer](./Remove-AzureSqlDatabaseServer.md)


