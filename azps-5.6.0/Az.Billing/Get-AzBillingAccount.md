---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/get-azbillingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
ms.openlocfilehash: 8c934adfd0bea950f97fbe8e8226568f9eaf57dc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959787"
---
# Get-AzBillingAccount

## SYNOPSIS
청구 계정을 얻습니다.

## 구문

### 목록(기본값)
```
Get-AzBillingAccount [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Single
```
Get-AzBillingAccount -Name <System.Collections.Generic.List`1[System.String]> [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-ListEntitiesToCreateSubscription]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Get-AzBillingAccount** cmdlet은 청구 계정을 얻게 며, 사용자가 액세스할 수 있습니다. 

## 예제

### 예제 1
```
PS C:\> Get-AzBillingAccount
```

사용자가 액세스할 수 있는 모든 청구 계정을 얻습니다.

### 예제 2
```
PS C:\> Get-AzBillingAccount -Name 00000000-0000-0000-0000-000000000000
```

지정된 이름으로 청구 계정을 얻습니다.

### 예제 3
```
PS C:\> Get-AzBillingAccount -IncludeAddress
```

사용자가 액세스할 수 있는 모든 청구 계정을 얻게 하여 결과에 주소를 포함합니다.

### 예제 4
```
PS C:\> Get-AzBillingAccount -ExpandBillingProfile
```

사용자가 액세스할 수 있는 모든 청구 계정을 얻게 하여 결과에 청구 프로필을 포함합니다.

### 예제 5
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection
```

사용자가 액세스할 수 있는 모든 청구 계정을 얻게 하여 결과에 청구 프로필 및 송장 섹션을 포함합니다.

### 예제 6
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection -ExpandAddress -Name 00000000-0000-0000-0000-000000000000
```

지정된 이름으로 청구 계정을 얻게 하여 결과에 주소, 청구 프로필 및 송장 섹션을 포함합니다.

## 매개 변수

### -DefaultProfile
azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독

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

### -IncludeAddress
청구 계정의 주소를 포함합니다.

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

### -ExpandBillingProfile
청구 계정 아래에 청구 프로필을 포함합니다.

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

### -ExpandInvoiceSection
청구 계정 아래에 청구 프로필 및 청구서 섹션을 포함합니다.

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

### -Name
특정 청구 계정의 이름입니다.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Single
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ListEntitiesToCreateSubscription
구독을 만드는 데 입력으로 사용할 수 있는 청구 계정 아래에 청구 엔터티를 나열합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.

## 입력

### 없음

## 출력

### Microsoft.Azure.Commands.Billing.Models.PSBillingAccount

## 참고 사항

## 관련 링크
