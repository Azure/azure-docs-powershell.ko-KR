---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageblobrangetorestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
ms.openlocfilehash: cfbe2cc695ceb2db7c498e8ee2750fa0427da114
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493140"
---
# New-AzStorageBlobRangeToRestore

## SYNOPSIS
Storage 계정을 복원하는 Blob 범위 개체를 만듭니다.

## 구문

```
New-AzStorageBlobRangeToRestore [-StartRange <String>] [-EndRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**New-AzStorageBlobRangeToRestore** cmdlet은 Restore-AzStorageBlobRange에서 사용할 수 있는 Blob 범위 개체를 만듭니다.

## 예제

### 예제 1: 복원할 Blob 범위를 만듭니다.
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange container2/blob2
```

이 명령은 container1/blob1(포함)에서 시작하여 container2/blob2(제외)에서 끝나는 복원할 Blob 범위를 만듭니다.

### 예제 2: 첫 번째 Blob에서 사전순으로 특정 Blob으로 복원할 Blob 범위를 만듭니다(제외).
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange container2/blob2
```

이 명령은 사전순의 첫 번째 Blob에서 특정 Blob container2/blob2(제외)로 복원할 Blob 범위를 만듭니다.

### 예제 3: 특정 Blob(포함)에서 사전순으로 마지막 Blob으로 복원할 Blob 범위를 만듭니다.
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange ""
```

이 명령은 특정 Blob container1/blob1(포함)에서 사전순으로 마지막 Blob으로 복원할 Blob 범위를 만듭니다.

### 예제 4: 모든 Blob을 복원하는 Blob 범위를 만듭니다.
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange ""
```

이 명령은 모든 Blob을 복원하는 Blob 범위를 만듭니다.

## PARAMETERS

### -DefaultProfile
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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
Blob 복원 종료 범위를 지정합니다.
끝 범위는 복원 Blob에서 제외됩니다.
빈 strng로 설정하여 끝으로 복원합니다.

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
Blob 복원 시작 범위를 지정합니다.
시작 범위는 Blob 복원에 포함됩니다.
빈 문자열로 설정하여 원래 상태로 복원합니다.

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### 없음

## 출력

### Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreRange

## 참고 사항

## 관련 링크
