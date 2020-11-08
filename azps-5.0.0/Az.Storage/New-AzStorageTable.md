---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTable.md
ms.openlocfilehash: 0f46570858368a821d176a5f4e0a907c8a56b49c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226064"
---
# New-AzStorageTable

## SYNOPSIS
저장소 테이블을 만듭니다.

## 구문과

```
New-AzStorageTable [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
**AzStorageTable** Cmdlet은 Azure의 저장소 계정과 연결 된 저장소 테이블을 만듭니다.

## 예제의

### 예제 1: azure 저장소 테이블 만들기
```
PS C:\>New-AzStorageTable -Name "tableabc"
```

이 명령은 tableabc의 이름을 사용 하 여 저장소 테이블을 만듭니다.

### 예제 2: 여러 azure storage 테이블 만들기
```
PS C:\>"table1 table2 table3".split() | New-AzStorageTable
```

이 명령은 여러 개의 표를 만듭니다.
.NET **문자열** 클래스의 **Split** 메서드를 사용 하 고 파이프라인의 이름을 전달 합니다.

## 변수

### -컨텍스트
저장소 컨텍스트를 지정 합니다.
이를 만들기 위해 New-AzStorageContext cmdlet을 사용할 수 있습니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
새 테이블의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

### Microsoft. Azure. 일반. IStorageContext

## 출력

### WindowsAzure. ResourceModel를 AzureStorageTable로 저장 합니다.

## 상속자

## 관련 링크

[Get-AzStorageTable](./Get-AzStorageTable.md)

[제거-AzStorageTable](./Remove-AzStorageTable.md)


