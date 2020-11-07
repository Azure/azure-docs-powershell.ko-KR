---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2B82F5BA-ABC6-4B37-B641-353CFE814290
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Update-AzSqlServerAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlServerAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlServerAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 3ec370f0e4865ed5695e4f0890f99b50709e9ad8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878677"
---
# Update-AzSqlServerAdvancedThreatProtectionSetting

## SYNOPSIS
서버에서 고급 위협 방지 설정을 설정 합니다.

## 구문과

```
Update-AzSqlServerAdvancedThreatProtectionSetting [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**AzSqlServerAdvancedThreatProtectionSetting** Cmdlet은 Azure SQL server에서 고급 위협 방지 설정을 설정 합니다.
서버에서 고급 위협 보호를 사용 하도록 설정 하려면 해당 서버에서 감사 설정을 사용 하도록 설정 해야 합니다.
이 cmdlet을 사용 하려면 서버를 식별 하는 *ResourceGroupName* 및 ServerName 매개 변수를 지정 합니다.

## 예제의

### 예제 1: 데이터베이스에 대 한 고급 위협 보호 설정 설정
```
PS C:\>Update-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

이 명령은 Server01 라는 서버에 대 한 고급 위협 방지 설정을 설정 합니다.

## 변수

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

### -EmailAdmins
고급 위협 방지 설정이 전자 메일을 사용 하 여 관리자에 게 연락 하는지 여부를 지정 합니다.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ExcludedDetectionType
설정에서 제외할 검색 유형의 배열을 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.
- Sql_Injection
- Sql_Injection_Vulnerability
- Access_Anomaly
- 않아야

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NotificationRecipientsEmails
설정이 알림을 보내는 세미콜론으로 구분 된 전자 메일 주소 목록을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
작업 중인 항목을 나타내는 개체를 반환 합니다.
기본적으로이 cmdlet은 출력을 생성 하지 않습니다.

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

### -ResourceGroupName
서버가 속한 리소스 그룹의 이름을 지정 합니다.

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

### -보존 기간
감사 로그 보존 일 수

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServerName
서버의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountName
사용할 저장소 계정의 이름을 지정 합니다. 와일드 카드는 허용 되지 않습니다. 이 매개 변수는 필요 하지 않습니다. 이 매개 변수를 제공 하지 않으면 cmdlet은 이전에 데이터베이스의 고급 위협 보호 설정의 일부로 정의 된 저장소 계정을 사용 합니다. 데이터베이스 위협 검색 설정을 처음 정의 하 고이 매개 변수를 제공 하지 않으면 cmdlet이 실패 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### System. 문자열

### 시스템 Null 허용 ' 1 [[CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]

### ThreatDetection. DetectionType []/. *

### 시스템 Null 허용 ' 1 [[System.webserver, System.webserver, CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]

## 출력

### ThreatDetection. ServerThreatDetectionsettingsModel에 대 한

## 상속자

## 관련 링크

[Get-AzSqlServerThreatDetectionsettings](./Get-AzSqlServerThreatDetectionsettings.md)

[제거-AzSqlServerThreatDetectionsettings](03e90cd1-6ae2-4134-bc5e-28cc080614c9)

[SQL 데이터베이스 설명서](https://docs.microsoft.com/azure/sql-database/)
