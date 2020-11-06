---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 85b62b8ffbdcdcefff5bbb5c984a19ef0b7cb644
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93524160"
---
# Remove-AzsStorageQuota

## SYNOPSIS
기존 할당량 삭제

## 구문과

### 삭제 (기본값)
```
Remove-AzsStorageQuota -Name <String> [-Location <String>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### 리소스
```
Remove-AzsStorageQuota -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
기존 할당량 삭제

## 예제의

### --------------------------예제 1--------------------------
```
Remove-AzsStorageQuota -Name 'TestDeleteStorageQuota'
```

이름으로 저장소 할당량을 제거 합니다.

### --------------------------예제 2--------------------------
```
Get-AzsStorageQuota -Name 'testquota' | Remove-AzsStorageQuota
```

파이프에 따라 저장소 할당량을 제거 합니다.

## 변수

### -Force
확인 메시지를 표시 하지 않습니다.

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

### -위치
리소스 위치입니다.

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
저장소 할당량의 이름입니다.

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
리소스 id입니다.

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
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
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

## 상속자

## 관련 링크

