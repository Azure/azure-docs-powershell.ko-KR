---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 18D5B95E-4CF1-4C79-AE8B-9F4DA49B46A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/add-azurermlogprofile
schema: 2.0.0
ms.openlocfilehash: 4302aa7dbc0cf31b9a7aa61678d871e9da140d51
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881566"
---
# Add-AzureRmLogProfile

## SYNOPSIS
새 활동 로그 프로필을 만듭니다. 이 프로필을 사용 하 여 활동 로그를 Azure storage 계정에 보관 하거나 같은 구독의 Azure 이벤트 허브에 스트리밍할 수 있습니다. 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Add-AzureRmLogProfile -Name <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-RetentionInDays <Int32>] -Location <System.Collections.Generic.List`1[System.String]>
 [-Category <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**추가-AzureRmLogProfile** cmdlet은 로그 프로필을 만듭니다.
- **저장소 계정** -표준 저장소 계정 (premium 저장소 계정 (지원 되지 않음)이 지원 되지 않음). ARM 또는 클래식 형식이 될 수 있습니다. 저장소 계정에 기록 된 경우 활동 로그를 저장 하는 비용은 표준 저장소 요금으로 청구 됩니다. 구독 당 하나의 로그 프로필만 있을 수 있습니다 consequentially 활동 로그 내보내기에는 구독 당 하나의 저장소 계정만 사용할 수 있습니다. 
- **이벤트 허브** -구독 당 하나의 로그 프로필만 사용할 수 있습니다 consequentially 활동 로그 내보내기에는 구독 당 하나의 이벤트 허브가 있을 수 있습니다. 활동 로그가 이벤트 허브로 스트리밍되는 경우 표준 이벤트 허브 가격이 적용 됩니다. 활동 로그에서 이벤트는 지역과 관련이 있거나 "전역" 일 수 있습니다. 전역 본질적으로 이러한 이벤트는 영역 agnostics 지역에 관계 없이 대부분의 이벤트가이 범주에 속합니다. 활동 로그 프로필이 포털에서 설정 된 경우 사용자 인터페이스에서 선택한 다른 지역과 함께 "Global"이 암시적으로 추가 됩니다. Cmdlet을 사용 하는 경우에는 "전역"으로 위치를 명시적으로 다른 지역과 별도로 언급 해야 합니다. 
**참고** : **위치에 "Global"을 설정 하지 않으면 대부분의 활동 로그가 내보내지지 않습니다.** 이 cmdlet은 ShouldProcess 패턴을 구현 합니다. 즉, 리소스를 실제로 생성, 수정 또는 제거 하기 전에 사용자에 게 확인을 요청할 수 있습니다.

## 예제의

### 예제 1: 새 로그 프로필을 추가 하 여 위치 조건과 일치 하는 활동 로그를 저장소 계정으로 내보내기
```
Add-AzureRmLogProfile -Location "Global","West US" -Name ExportLogProfile -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

## 변수

### -범주
범주 목록을 지정 합니다.

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

### -위치
로그 프로필의 위치를 지정 합니다.
유효한 값: 최신 위치 목록을 가져오려면 cmdlet을 실행 합니다. Get-AzureLocation | DisplayName 선택

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

### -이름
프로필의 이름을 지정 합니다.

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

### -보존 기간
보존 정책을 일 단위로 지정 합니다. 지정 된 저장소 계정에서 로그가 보존 되는 일 수입니다. 데이터를 계속 유지 하려면이를 **0** 으로 설정 합니다. 지정 하지 않으면 **0** 으로 설정 됩니다. 데이터 보존에는 일반 표준 저장소나 이벤트 허브 청구 요금이 적용 됩니다.

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
서비스 버스 규칙의 ID를 지정 합니다.

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
저장소 계정의 ID를 지정 합니다. ID는 저장소 계정의 정규화 된 리소스 ID입니다 예:  
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

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

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
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다. Cmdlet이 실행 되지 않습니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

### 시스템 Null 허용 ' 1 [[b77a5c561934e089, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken =]]

### System.webserver. List ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = b77a5c561934e089]]

## 출력

### Microsoft Azure.. PSLogProfile

## 상속자

## 관련 링크

[Get-AzureRmLogProfile](./Get-AzureRmLogProfile.md)

[제거-AzureRmLogProfile](./Remove-AzureRmLogProfile.md)


