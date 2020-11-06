---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 46efba5e2ab9a5c51172264b343b0f4f2b508065
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "93522683"
---
# Import-AzureRmContext

## SYNOPSIS
파일에서 Azure 인증 정보를 로드 합니다.

## 구문과

### InMemoryProfile
```
Import-AzureRmContext [-AzureContext] <AzureRmProfile> [-WhatIf] [-Confirm]
```

### ProfileFromDisk
```
Import-AzureRmContext [-Path] <String> [-WhatIf] [-Confirm]
```

## 설명은
Import-AzureRmContext cmdlet은 파일에서 인증 정보를 로드 하 여 Azure 환경 및 컨텍스트를 설정 합니다.
현재 세션에서 실행 하는 cmdlet은이 정보를 사용 하 여 Azure Resource Manager에 대 한 요청을 인증 합니다.

## 예제의

### 예제 1: AzureRmProfile에서 컨텍스트 가져오기
```
PS C:\> Import-AzureRmContext -AzureContext (Add-AzureRmAccount)

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

이 예제에서는 cmdlet으로 전달 되는 PSAzureProfile에서 컨텍스트를 가져옵니다.

### 예제 2: JSON 파일에서 컨텍스트 가져오기
```
PS C:\> Import-AzureRmContext -Path C:\test.json

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

이 예제에서는 cmdlet으로 전달 되는 JSON 파일에서 컨텍스트를 선택 합니다.
이 JSON 파일은 가져오기-AzureRmContext에서 만들 수 있습니다.

## 변수

### -AzureContext
이 cmdlet이 읽는 Azure 컨텍스트를 지정 합니다.
컨텍스트를 지정 하지 않으면이 cmdlet은 로컬 기본 컨텍스트를 읽습니다.

```yaml
Type: AzureRmProfile
Parameter Sets: InMemoryProfile
Aliases: Profile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Path
Save-AzureRMContext를 사용 하 여 저장 된 컨텍스트 정보의 경로를 지정 합니다.

```yaml
Type: String
Parameter Sets: ProfileFromDisk
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

```yaml
Type: SwitchParameter
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

## 입력

### AzureRMProfile (일반. 인증. 모델)
System. 문자열

## 출력

### Microsoft. Azure. PSAzureProfile

## 상속자

## 관련 링크

