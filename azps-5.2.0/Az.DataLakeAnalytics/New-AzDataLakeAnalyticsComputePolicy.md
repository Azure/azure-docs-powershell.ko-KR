---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/new-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 76df1cb780220a09ccc0d571fd88223e746eefe6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339626"
---
# New-AzDataLakeAnalyticsComputePolicy

## SYNOPSIS
특정 AAD 엔터티에 대한 Data Lake Analytics 계산 정책 규칙을 만듭니다.

## 구문

```
New-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-ObjectId] <Guid> [-ObjectType] <String> [-MaxAnalyticsUnitsPerJob <Int32>] [-MinPriorityPerJob <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명
**New-AzDataLakeAnalyticsComputePolicy는** Azure Data Lake Analytics 계정에서 특정 AAD 엔터티에 대해 지정된 계산 정책 규칙을 만듭니다.

## 예제

### 예제 1: 규칙 하나만 사용하여 계산 정책 만들기
```
PS C:\>New-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxAnalyticsUnitsPerJob 5
```

이 명령은 ID가 "83cb7ad2-3523-4b82-b909-d478b0d8aea3"인 사용자에 대한 "contosoadla" 계정에 "myPolicy"라는 정책을 만들어 5개 이상의 분석 단위가 있는 작업을 제출할 수 없습니다.

### 예제 2: 두 규칙 집합이 모두 있는 계산 정책 만들기
```
PS C:\>New-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxAnalyticsUnitsPerJob 5 -MinPriorityPerJob 100
```

이 명령은 ID가 "83cb7ad2-3523-4b82-b909-d478b0d8aea3"인 사용자에 대해 "contosoadla" 계정에 "myPolicy"라는 정책을 만들어 5개 이상의 분석 단위 또는 우선 순위가 100보다 낮은 작업을 제출할 수 없습니다.

## PARAMETERS

### -Account
계산 정책을 추가할 계정의 이름입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -MaxAnalyticsUnitsPerJob
이 정책에 대해 작업당 지원되는 최대 분석 단위입니다.
이 매개 변수, MinPriorityPerJob 또는 두 매개 변수를 모두 지정해야 합니다.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: MaxDegreeOfParallelismPerJob

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MinPriorityPerJob
이 정책에 대해 작업당 지원되는 최소 우선 순위입니다.
MaxAnalyticsUnitsPerJob 또는 두 매개 변수를 모두 지정해야 합니다.

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

### -Name
만들 계산 정책의 이름입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ComputePolicyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ObjectId
정책을 적용할 사용자 또는 그룹에 대한 Azure Active Directory 개체 ID입니다.

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ObjectType
전달된 개체 ID에 대한 Azure Active Directory 개체 형식입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: User, Group, ServicePrincipal

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
계정이 있는 리소스 그룹의 이름입니다.
선택 사항이며, 제공되지 않은 경우 검색을 시도합니다.

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

### -Confirm
cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
cmdlet이 실행되는 경우의 결과 표시 cmdlet이 실행되지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### System.String

### System.Guid

### System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

## 출력

### Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy

## 참고 사항

## 관련 링크
