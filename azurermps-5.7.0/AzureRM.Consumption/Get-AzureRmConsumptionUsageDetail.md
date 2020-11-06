---
external help file: Microsoft.Azure.Commands.Consumption.dll-Help.xml
Module Name: AzureRM.Consumption
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.consumption/get-azurermconsumptionusagedetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionUsageDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionUsageDetail.md
ms.openlocfilehash: 2694ce516b1bb3202fc194e1c1eec55610f7b92a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525228"
---
# Get-AzureRmConsumptionUsageDetail

## SYNOPSIS
구독에 대 한 사용 현황 정보를 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### 구독 (기본값)
```
Get-AzureRmConsumptionUsageDetail [-MaxCount <Int32>] [-IncludeMeterDetails] [-IncludeAdditionalProperties]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### 청구
```
Get-AzureRmConsumptionUsageDetail -InvoiceName <String> [-MaxCount <Int32>] [-IncludeMeterDetails]
 [-IncludeAdditionalProperties] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### BillingPeriod
```
Get-AzureRmConsumptionUsageDetail -BillingPeriodName <String> [-MaxCount <Int32>] [-IncludeMeterDetails]
 [-IncludeAdditionalProperties] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzureRmConsumptionUsageDetail** cmdlet은 구독에 대 한 사용 세부 정보를 가져옵니다. 

## 예제의

### 예제 1
```
PS C:\> Get-AzureRmConsumptionUsageDetail -IncludeMeterDetails -InvoiceName 201704-117283130069214
```

지정 된 이름을 사용 하 여 송장의 사용 정보를 가져오고 결과에 MeterDetails 속성을 포함 합니다.

### 예제 2
```
PS C:\> Get-AzureRmConsumptionUsageDetail -IncludeAdditionalProperties -BillingPeriodName 201704-1
```

지정 된 이름의 청구 기간에 대 한 사용 세부 정보를 얻고 결과에 AdditionalProperties 속성을 포함 합니다.

### 예제 3
```
PS C:\> Get-AzureRmConsumptionUsageDetail -StartDate 2017-01-17 -EndDate 2017-01-19
```

2017-01-17에서 2017-01-19 사이의 구독에 대 한 사용 세부 정보를 가져옵니다.

## 변수

### -BillingPeriodName
와 연결 되는 사용 세부 정보를 가져올 특정 청구 기간의 이름입니다.

```yaml
Type: String
Parameter Sets: BillingPeriod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndDate
사용의 끝 날짜 (UTC)입니다.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeAdditionalProperties
용도에 추가 속성을 포함 합니다.

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

### -IncludeMeterDetails
용도에 측정기 세부 정보를 포함 합니다.

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

### -InvoiceName
에 연결 되는 사용 현황 정보를 가져올 특정 송장의 이름입니다.

```yaml
Type: String
Parameter Sets: Invoice
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxCount
반환할 최대 레코드 수를 결정 합니다.

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

### -시작 날짜
용도 시작 날짜 (UTC)입니다.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야

## 출력

### System.webserver. List ' 1 [[Microsoft PSUsageDetail, Microsoft azure. 0.1.0.0, Version =, Culture = 중립, PublicKeyToken = null]])

## 상속자

## 관련 링크

