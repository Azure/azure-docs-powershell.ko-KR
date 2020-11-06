---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FF2BFE34-4A12-49F9-9BE5-4084A36BC272
online version: ''
schema: 2.0.0
ms.openlocfilehash: d517ca49f0be3b6add58d151b3b2f79dad17611c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93524120"
---
# Set-AzureStorageTableStoredAccessPolicy

## SYNOPSIS
Azure storage 테이블에 대해 저장 된 액세스 정책을 설정 합니다.

## 구문과

```
Set-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**AzureStorageTableStoredAccessPolicy** Cmdlet은 Azure storage 테이블에 대해 저장 된 액세스 정책을 설정 합니다.

## 예제의

### 예제 1: 모든 권한이 있는 테이블에서 저장 된 액세스 정책 설정
```
PS C:\>Set-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy08"
```

이 명령은 MyTable 이라는 저장소 테이블에 대 한 Policy08 라는 액세스 정책을 설정 합니다.

## 변수

### -컨텍스트
Azure 저장소 컨텍스트를 지정 합니다.
저장소 컨텍스트를 얻으려면 New-AzureStorageContext cmdlet을 사용 합니다.

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ExpiryTime
저장 된 액세스 정책이 만료 되는 시간을 지정 합니다.

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

### -NoExpiryTime
액세스 정책에 만료 날짜가 없음을 나타냅니다.

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

### -NoStartTime
시작 시간이 $Null 설정 됨을 나타냅니다.

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

### -사용 권한
이 저장소 테이블에 대 한 공용 액세스 수준을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -정책
이 SAS 토큰에 대 한 사용 권한을 포함 하는 저장 된 액세스 정책을 지정 합니다.

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

### -StartTime
저장 된 액세스 정책이 유효 하 게 되는 시간을 지정 합니다.

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

### -테이블
Azure 저장소 테이블 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
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
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다. Cmdlet이 실행 되지 않습니다.

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

[Get-AzureStorageTableStoredAccessPolicy](./Get-AzureStorageTableStoredAccessPolicy.md)

[새로운 AzureStorageContext](./New-AzureStorageContext.md)

[새로운 AzureStorageTableStoredAccessPolicy](./New-AzureStorageTableStoredAccessPolicy.md)

[제거-AzureStorageTableStoredAccessPolicy](./Remove-AzureStorageTableStoredAccessPolicy.md)
