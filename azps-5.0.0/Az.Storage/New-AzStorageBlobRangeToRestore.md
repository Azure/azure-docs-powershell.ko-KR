---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageblobrangetorestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
ms.openlocfilehash: cfbe2cc695ceb2db7c498e8ee2750fa0427da114
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217175"
---
# New-AzStorageBlobRangeToRestore

## SYNOPSIS
저장소 계정을 복원 하는 Blob Range 개체를 만듭니다.

## 구문과

```
New-AzStorageBlobRangeToRestore [-StartRange <String>] [-EndRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzStorageBlobRangeToRestore** Cmdlet은 Restore-AzStorageBlobRange에서 사용할 수 있는 Blob range 개체를 만듭니다.

## 예제의

### 예제 1: 복원할 blob 범위 만들기
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange container2/blob2
```

이 명령은 container1/blob1 (포함)에서 시작 하 고 container2/blob2 (exclude)에서 끝나는 blob 범위를 만듭니다.

### 예제 2: 사전순으로 첫 번째 blob에서 특정 blob (제외)로 복원 하는 blob 범위를 만듭니다.
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange container2/blob2
```

이 명령은 사전순의 첫 번째 blob에서 특정 blob container2/blob2 (exclude)으로 복원 하는 blob 범위를 만듭니다.

### 예제 3: 특정 blob (포함)에서 마지막 blob까지 사전순으로 복원 하는 blob 범위를 만듭니다.
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange ""
```

이 명령은 특정 blob container1/blob1 (포함)에서 마지막 blob까지 사전순으로 복원 하는 blob 범위를 만듭니다.

### 예제 4: 모든 blob을 복원 하는 blob 범위 만들기
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange ""
```

이 명령은 모든 blob을 복원 하는 blob 범위를 만듭니다.

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

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

### -EndRange
Blob 복원 종료 범위를 지정 합니다.
Restore blob에서 End 범위가 제외 됩니다.
이를 빈 strng로 설정 하 여 끝까지 복원할 수 있습니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartRange
Blob 복원 시작 범위를 지정 합니다.
시작 범위는 복원 blob에 포함 됩니다.
처음부터 복원할 수 있도록 빈 문자열로 설정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야

## 출력

### PSBlobRestoreRange를 통해 관리 합니다.

## 상속자

## 관련 링크
