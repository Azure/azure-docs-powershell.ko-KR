---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerKeyVaultKey.md
ms.openlocfilehash: 81ec18dd543a63a971d01a64c878774b266cf0fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536503"
---
# Remove-AzureRmSqlServerKeyVaultKey

## SYNOPSIS
SQL server에서 키 자격 증명 모음 키를 제거 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Remove-AzureRmSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 설명은
Remove-AzureRmSqlServerKeyVaultKey cmdlet은 지정 된 SQL server에서 키 자격 증명 모음 키를 제거 합니다.
키 보관소에 대 한 SQL server의 사용 권한은 변경 되지 않습니다.
사용 권한을 변경 하려면 Set-AzureRmKeyVaultAccessPolicy를 사용 합니다.
이 cmdlet은 키 자격 증명을 변경할 수 없습니다.
키 자격 증명 모음에서 키를 제거 하려면 AzureKeyVaultKey를 사용 합니다.

## 예제의

### 예제 1: 키 자격 증명 모음 키 제거
```
PS C:\> Remove-AzureRmSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

이 명령은 지정 된 서버에서 Id가 ' ' 인 키 보관소 키를 제거 합니다 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 .
ResourceGroupName: ContosoResourceGroup ServerName: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 Type: AzureKeyVault Uri: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 지문: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 AM

## 변수

### -AsJob
백그라운드에서 cmdlet 실행

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

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독

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

### -KeyId
Azure 키 자격 증명 모음 KeyId.

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

### -ResourceGroupName
리소스 그룹의 이름입니다.

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
Azure Sql Server 이름입니다.

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

## 출력

### ServerKeyVaultKey. AzureSqlServerKeyVaultKeyModel에 대 한

## 상속자

## 관련 링크

[SQL 데이터베이스 설명서](https://docs.microsoft.com/azure/sql-database/)
