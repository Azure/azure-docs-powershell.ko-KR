---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: f3afbd9b96de51f754dd87dfa42ed6f71e5b3577
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "93522684"
---
# Save-AzureRmContext

## SYNOPSIS
다른 PowerShell 세션에서 사용할 현재 인증 정보를 저장 합니다.

## 구문과

```
Save-AzureRmContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force] [-WhatIf] [-Confirm]
```

## 설명은
Save-AzureRmContext cmdlet은 다른 PowerShell 세션에서 사용할 현재 인증 정보를 저장 합니다.

## 예제의

### 예제 1: 현재 세션의 컨텍스트 저장
```
PS C:\> Add-AzureRmAccount
PS C:\> Save-AzureRmContext -Path C:\test.json
```

이 예제에서는 현재 세션의 Azure 컨텍스트를 제공 된 JSON 파일에 저장 합니다.

### 예제 2: 지정 된 컨텍스트 저장
```
PS C:\> Save-AzureRmContext -Profile (Add-AzureRmAccount) -Path C:\test.json
```

이 예제에서는 cmdlet에 전달 된 Azure 컨텍스트를 제공 된 JSON 파일에 저장 합니다.

## 변수

### -Force
지정 된 파일 (있는 경우)을 덮어씁니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
인증 정보를 저장할 파일의 경로를 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -프로필
이 cmdlet이 읽는 Azure 컨텍스트를 지정 합니다.
컨텍스트를 지정 하지 않으면이 cmdlet은 로컬 기본 컨텍스트를 읽습니다.

```yaml
Type: AzureRmProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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

## 출력

### Microsoft. Azure. PSAzureProfile

## 상속자

## 관련 링크

