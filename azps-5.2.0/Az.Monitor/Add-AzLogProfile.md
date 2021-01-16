---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 18D5B95E-4CF1-4C79-AE8B-9F4DA49B46A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzLogProfile.md
ms.openlocfilehash: bc0f1a6aacc6188a982fe75fa021bdafdc4e02de
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322335"
---
# Add-AzLogProfile

## SYNOPSIS
새 활동 로그 프로필을 만듭니다. 이 프로필은 활동 로그를 Azure Storage 계정에 보관하거나 동일한 구독의 Azure 이벤트 허브로 스트림하는 데 사용됩니다. 

## 구문

```
Add-AzLogProfile -Name <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-RetentionInDays <Int32>] -Location <System.Collections.Generic.List`1[System.String]>
 [-Category <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명
**Add-AzLogProfile** cmdlet은 로그 프로필을 만듭니다.
- **Storage 계정** - 표준 스토리지 계정(Premium Storage 계정은 지원되지 않습니다)만 지원됩니다. 클래식 또는 클래식 형식일 ARM 있습니다. 저장소 계정에 기록된 경우 활동 로그를 저장하는 비용은 일반 표준 저장소 요금으로 청구됩니다. 구독당 하나의 로그 프로필만 있을 수 있습니다. 따라서 구독당 하나의 저장소 계정만 활동 로그를 내보내는 데 사용할 수 있습니다. 
- **이벤트 허브** - 구독당 하나의 로그 프로필만 있을 수 있습니다. 따라서 구독당 하나의 이벤트 허브만 활동 로그를 내보낼 수 있습니다. 활동 로그가 이벤트 허브로 스트리밍된 경우 표준 이벤트 허브 가격 책정이 적용됩니다. 활동 로그에서 이벤트는 지역에 대한 것이거나 "전역"일 수 있습니다. 전역은 기본적으로 이러한 이벤트는 지역 독립적이며 지역과 독립적입니다. 실제로 대부분의 이벤트는 이 범주에 속합니다. 활동 로그 프로필이 포털에서 설정된 경우 사용자 인터페이스에서 선택한 다른 지역과 함께 "전역"을 암시적으로 추가합니다. cmdlet을 사용하는 경우 다른 지역과 별도로 "전역"으로 위치를 명시적으로 언급해야 합니다. 
**참고** :- **위치에서 "전역"을** 설정하지 못하면 대부분의 활동 로그가 내보내지지 않습니다. 이 cmdlet은 ShouldProcess 패턴을 구현합니다. 즉, 리소스를 실제로 만들거나 수정하거나 제거하기 전에 사용자로부터 확인을 요청할 수 있습니다.

## 예제

### 예제 1: 위치 조건과 일치하는 활동 로그를 저장소 계정으로 내보내는 새 로그 프로필 추가
```powershell
Add-AzLogProfile -Location "Global","West US" -Name ExportLogProfile -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

### 예제 2

새 활동 로그 프로필을 만듭니다. (자동Generated)

```powershell <!-- Aladdin Generated Example --> 
Add-AzLogProfile -Location 'Global' -Name ExportLogProfile -RetentionInDays <Int32> -ServiceBusRuleId <String> -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

## PARAMETERS

### -Category
범주 목록을 지정합니다.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
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

### -Location
로그 프로필의 위치를 지정합니다.
유효한 값: 아래 cmdlet을 실행하여 최신 위치 목록을 얻습니다. Get-AzLocation | DisplayName 선택

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
프로필의 이름을 지정합니다.

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

### -RetentionInDays
보존 정책(일)을 지정합니다. 지정된 저장소 계정에서 로그가 보존되는 일 수입니다. 데이터를 보존하기 위해 이 데이터를 **0으로 설정합니다.** 지정하지 않으면 기본값은 **0입니다.** 일반 표준 저장소 또는 이벤트 허브 청구 요금은 데이터 보존에 적용됩니다.

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

### -ServiceBusRuleId
Service Bus 규칙의 ID를 지정합니다.

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

### -StorageAccountId
Storage 계정의 ID를 지정합니다. ID는 저장소 계정의 정식 리소스 ID입니다. 예를 들면 다음과 같습니다.  
/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### System.String

### System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

## 출력

### Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile

## 참고 사항

## 관련 링크

[Get-AzLogProfile](./Get-AzLogProfile.md)

[Remove-AzLogProfile](./Remove-AzLogProfile.md)


