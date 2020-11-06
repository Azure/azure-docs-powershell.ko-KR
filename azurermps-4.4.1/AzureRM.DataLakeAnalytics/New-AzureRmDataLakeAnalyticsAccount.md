---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0A7CD695-6D14-4BC9-B960-0CAFE502B88B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 7c35821cbaf75a616ab1b9b8bbc2db9fc2a96794
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536415"
---
# New-AzureRmDataLakeAnalyticsAccount

## SYNOPSIS
Data Lake Analytics 계정을 만듭니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
New-AzureRmDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-DefaultDataLakeStore] <String> [[-Tags] <Hashtable>] [-MaxDegreeOfParallelism <Int32>]
 [-MaxJobCount <Int32>] [-QueryStoreRetention <Int32>] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzureRmDataLakeAnalyticsAccount** Cmdlet은 Azure Data Lake Analytics 계정을 만듭니다.

## 예제의

### 예제 1: Data Lake Analytics 계정 만들기
```
PS C:\>New-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount" -ResourceGroupName "ContosoOrg" -Location "East US 2" -DefaultDataLakeStore "ContosoAdlStore"
```

이 명령은 ContosoAdlStore 데이터 저장소를 사용 하는 ContosoAdlAccount 이라는 데이터 호수 분석 계정을 ContosoOrg 이라는 리소스 그룹에 만듭니다.

## 변수

### -DefaultDataLakeStore
기본 데이터 원본으로 설정할 Data Lake Store 계정의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -위치
Data Lake Analytics 계정을 만들 위치를 지정 합니다.
이번에는 미국 동부 2만 지원 됩니다.

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

### -MaxDegreeOfParallelism
이 계정에 대해 지원 되는 최대 병렬 처리 수준 (선택 사항)입니다. 아무것도 지정 하지 않으면 기본적으로 30입니다.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MaxJobCount
계정에서 동시에 실행 되는 선택적으로 지원 되는 최대 작업 시간입니다. 아무것도 지정 하지 않으면 기본적으로 3이 됩니다.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -이름
Data Lake Analytics 계정 이름을 지정 합니다.

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

### -QueryStoreRetention
작업 메타 데이터가 유지 되는 선택적 일 수입니다. 지정 하지 않을 경우 기본값은 30 일입니다.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Data Lake Analytics 계정의 리소스 그룹 이름을 지정 합니다.
리소스 그룹을 만들려면 New-AzureRmResourceGroup cmdlet을 사용 합니다.

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

### 태그
다른 Azure 리소스 간에 데이터 호수 분석 계정을 식별 하는 데 사용할 수 있는 키-값 쌍을 지정 합니다.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -티어
이 계정에서 사용할 적절 한 약정 계층입니다.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Analytics.Models.TierType]
Parameter Sets: (All)
Aliases: 
Accepted values: Consumption, Commitment100AUHours, Commitment500AUHours, Commitment1000AUHours, Commitment5000AUHours, Commitment10000AUHours, Commitment50000AUHours, Commitment100000AUHours, Commitment500000AUHours

Required: False
Position: Named
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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

### PSDataLakeAnalyticsAccount
새로 만든 계정에 대 한 세부 정보입니다.

## 상속자

## 관련 링크

[Get-AzureRmDataLakeAnalyticsAccount](./Get-AzureRmDataLakeAnalyticsAccount.md)

[제거-AzureRmDataLakeAnalyticsAccount](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[Set-AzureRmDataLakeAnalyticsAccount](./Set-AzureRmDataLakeAnalyticsAccount.md)

[테스트-AzureRmDataLakeAnalyticsAccount](./Test-AzureRmDataLakeAnalyticsAccount.md)


