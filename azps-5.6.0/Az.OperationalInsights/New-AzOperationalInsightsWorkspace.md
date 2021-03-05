---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 4682807D-34E8-4057-8894-36820447067B
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/new-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 8d46c16afe8041181916eb25affed58e072798ea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989879"
---
# New-AzOperationalInsightsWorkspace

## SYNOPSIS
작업 영역이 만들어지거나 삭제된 작업 영역이 복원됩니다.

## 구문

```
New-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Sku] <String>] [[-Tag] <Hashtable>] [[-RetentionInDays] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [[-PublicNetworkAccessForIngestion] <String>]
 [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명
**New-AzOperationalInsightsWorkspace** cmdlet은 지정된 리소스 그룹 및 위치에 작업 영역이 생성됩니다. 또는 소프트 삭제된 작업 영역 복원.

## 예제

### 예제 1: 이름에 따라 작업 영역 만들기
```
PS C:\>New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Location "East US" -Sku "Standard"
```

이 명령은 ContosoResourceGroup이라는 리소스 그룹에 MyWorkspace라는 표준 SKU 작업 영역이 생성됩니다.

### 예제 2: 작업 영역 만들기 및 기존 계정에 연결
```
PS C:\>$OILinkTargets = Get-AzOperationalInsightsLinkTargets

PS C:\>$OILinkTargets[0] | New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku "Standard"
```

첫 번째 명령은 Get-AzOperationalInsightsLinkTargets cmdlet을 사용하여 Operational Insights 계정 링크 대상을 확인한 다음 해당 $OILinkTargets 저장합니다.
두 번째 명령은 파이프라인 연산자를 사용하여 $OILinkTargets 첫 번째 계정 링크 대상을 **New-AzOperationalInsightsWorkspace** cmdlet에 전달합니다.
명령은 MyWorkspace라는 표준 SKU 작업 영역이 만들어지며, 이 작업 영역은 이 작업 영역의 첫 번째 Operational Insights 계정에 $OILinkTargets.

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

### -Force
사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.

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

### -Location
작업 영역(예: 미국 동부 또는 유럽 서부)을 만들 위치를 지정합니다.

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

### -Name
작업 영역의 이름을 지정합니다.

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

### -PublicNetworkAccessForIngestion
작업 영역 섭취에 액세스하기 위한 네트워크 액세스 유형입니다. 값은 '사용' 또는 '사용 안 되어' 입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicNetworkAccessForQuery
작업 영역 쿼리에 액세스하기 위한 네트워크 액세스 유형입니다. 값은 '사용' 또는 '사용 안 되어' 입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Azure 리소스 그룹의 이름을 지정합니다.
작업 영역은 이 리소스 그룹에 만들어집니다.

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

### -RetentionInDays
작업 영역 데이터 보존 기간은 며칠입니다. 730일은 다른 모든 Sku에 대해 허용되는 최대 일입니다.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Sku
작업 영역의 서비스 계층을 지정합니다. 사용할 값에 대한 자세한 내용은 를 https://docs.microsoft.com/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers 확인하세요.
유효한 값은:
- 무료
- pergb2018
- pernode
- premium
- 독립 실행형
- 표준

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

### -Tag
작업 영역의 리소스 태그입니다.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -확인
cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.

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
cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.
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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## 입력

### System.String

### System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### System.Collections.Hashtable

### System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

## 출력

### Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace

## 참고 사항

새 가격 책정 모델이 릴리스되었습니다. CSP인 경우 sku에 대해 "독립 실행형"을 사용해야 합니다. 뒤에서 sku는 pergb2018로 변경됩니다. 자세한 내용은 다음을 참조하세요. https://docs.microsoft.com/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model

## 관련 링크

[Azure Operational Insights Cmdlet](./Az.OperationalInsights.md)

[Get-AzOperationalInsightsLinkTargets](./Get-AzOperationalInsightsLinkTargets.md)


