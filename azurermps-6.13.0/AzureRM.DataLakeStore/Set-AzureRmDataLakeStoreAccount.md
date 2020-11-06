---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 0EB5C25C-D0A1-4444-AEA2-C963D5069CFC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: b9154b239e8d4ae2857cba18d3f7dcf9510a62b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526196"
---
# Set-AzureRmDataLakeStoreAccount

## SYNOPSIS
Data Lake Store 계정을 수정 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Set-AzureRmDataLakeStoreAccount [-Name] <String> [[-DefaultGroup] <String>] [[-Tag] <Hashtable>]
 [[-TrustedIdProviderState] <TrustedIdProviderState>] [[-FirewallState] <FirewallState>]
 [[-ResourceGroupName] <String>] [-Tier <TierType>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-KeyVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzureRmDataLakeStoreAccount** Cmdlet은 Data Lake store 계정을 수정 합니다.

## 예제의

### 예제 1: 계정에 태그 추가
```
PS C:\>Set-AzureRmDataLakeStoreAccount -Name "ContosoADL" -Tags @{"stage"="production"}
```

이 명령은 ContosoADL 이라는 Data Lake Store 계정에 지정 된 태그를 추가 합니다.

## 변수

### -AllowAzureIpState
방화벽을 통해 Azure 시작 Ip를 선택적으로 허용/차단 합니다.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.FirewallAllowAzureIpsState]
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultGroup
AzureActive Directory 그룹의 ID를 지정 합니다.
이 그룹은 사용자가 만든 파일 및 폴더의 기본 그룹입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -FirewallState
선택적으로 기존 방화벽 규칙을 사용 하거나 사용 하지 않도록 설정 합니다.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.FirewallState]
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -KeyVersion
암호화 유형이 사용자 지정 인 경우 사용자는이 매개 변수를 사용 하 여 해당 키 버전을 회전할 수 있습니다.

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

### -이름
Data Lake Store 계정의 이름을 지정 합니다.

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

### -ResourceGroupName
수정할 Data Lake Store 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### 태그
태그를 키-값 쌍으로 지정 합니다.
태그를 사용 하 여 다른 Azure 리소스에서 Data Lake Store 계정을 식별할 수 있습니다.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -티어
이 계정에서 사용할 적절 한 약정 계층입니다.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.TierType]
Parameter Sets: (All)
Aliases:
Accepted values: Consumption, Commitment1TB, Commitment10TB, Commitment100TB, Commitment500TB, Commitment1PB, Commitment5PB

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TrustedIdProviderState
필요에 따라 기존 신뢰할 수 있는 ID 공급자를 설정 하거나 해제 합니다.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.TrustedIdProviderState]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

### System.webserver. 컬렉션 테이블

### 시스템 Null 허용 ' 1 [[DataLake]. TrustedIdProviderState, DataLake, Version = 2.0.0.0, Culture = 중립, PublicKeyToken = 31bf3856ad364e35]],.

### 시스템 Null 허용 ' 1 [[DataLake]. FirewallState, DataLake, Version = 2.0.0.0, Culture = 중립, PublicKeyToken = 31bf3856ad364e35]],.

### 시스템 Null 허용 ' 1 [[DataLake]. TierType, DataLake, Version = 2.0.0.0, Culture = 중립, PublicKeyToken = 31bf3856ad364e35]],.

### 시스템 Null 허용 ' 1 [[DataLake]. FirewallAllowAzureIpsState, DataLake, Version = 2.0.0.0, Culture = 중립, PublicKeyToken = 31bf3856ad364e35]],.

## 출력

### Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount

## 상속자

## 관련 링크

[Get-AzureRmDataLakeStoreAccount](./Get-AzureRmDataLakeStoreAccount.md)

[새로운 AzureRmDataLakeStoreAccount](./New-AzureRmDataLakeStoreAccount.md)

[제거-AzureRmDataLakeStoreAccount](./Remove-AzureRmDataLakeStoreAccount.md)

[테스트-AzureRmDataLakeStoreAccount](./Test-AzureRmDataLakeStoreAccount.md)


