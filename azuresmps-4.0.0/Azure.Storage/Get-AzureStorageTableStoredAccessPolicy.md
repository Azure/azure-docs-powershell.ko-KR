---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BF5526C1-11B9-47A8-A5A6-CB275B470A9E
online version: ''
schema: 2.0.0
ms.openlocfilehash: a8c22b3eb95ab940670043f9ae467663c951027d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523992"
---
# Get-AzureStorageTableStoredAccessPolicy

## SYNOPSIS
Azure storage 테이블에 대 한 저장 된 액세스 정책 또는 정책을 가져옵니다.

## 구문과

```
Get-AzureStorageTableStoredAccessPolicy [-Table] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## 설명은
**AzureStorageTableStoredAccessPolicy** Cmdlet은 Azure storage 테이블에 대 한 저장 된 액세스 정책 또는 정책을 나열 합니다.

## 예제의

### 예제 1: 저장소 테이블에 저장 된 액세스 정책 가져오기
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02" -Policy "Policy50"
```

이 명령은 Table02 이라는 저장소 테이블에서 Policy50 라는 액세스 정책을 가져옵니다.

### 예제 2: 저장소 테이블에 저장 된 모든 액세스 정책 가져오기
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02"
```

이 명령은 Table02 이라는 테이블에 있는 모든 액세스 정책을 가져옵니다.

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

### -정책
이 SA (공유 액세스 서명) 토큰에 대 한 사용 권한을 포함 하는 저장 된 액세스 정책을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

## 상속자

## 관련 링크

[새로운 AzureStorageTableStoredAccessPolicy](./New-AzureStorageTableStoredAccessPolicy.md)

[제거-AzureStorageTableStoredAccessPolicy](./Remove-AzureStorageTableStoredAccessPolicy.md)

[Set-AzureStorageTableStoredAccessPolicy](./Set-AzureStorageTableStoredAccessPolicy.md)

[새로운 AzureStorageContext](./New-AzureStorageContext.md)


