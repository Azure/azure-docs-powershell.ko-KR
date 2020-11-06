---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9a58f869d5308b176a68614cbb2fa2fec401fa14
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523844"
---
# New-AzureStorageTable

## SYNOPSIS
저장소 테이블을 만듭니다.

## 구문과

```
New-AzureStorageTable [-Name] <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## 설명은
**AzureStorageTable** Cmdlet은 Azure의 저장소 계정과 연결 된 저장소 테이블을 만듭니다.

## 예제의

### 예제 1: azure 저장소 테이블 만들기
```
PS C:\>New-AzureStorageTable -Name "tableabc"
```

이 명령은 tableabc의 이름을 사용 하 여 저장소 테이블을 만듭니다.

### 예제 2: 여러 azure storage 테이블 만들기
```
PS C:\>"table1 table2 table3".split() | New-AzureStorageTable
```

이 명령은 여러 개의 표를 만듭니다.
.NET **문자열** 클래스의 **Split** 메서드를 사용 하 고 파이프라인의 이름을 전달 합니다.

## 변수

### -컨텍스트
저장소 컨텍스트를 지정 합니다.
이를 만들기 위해 New-AzureStorageContext cmdlet을 사용할 수 있습니다.

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

### -이름
새 테이블의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Table

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

[Get-AzureStorageTable](./Get-AzureStorageTable.md)

[제거-AzureStorageTable](./Remove-AzureStorageTable.md)


