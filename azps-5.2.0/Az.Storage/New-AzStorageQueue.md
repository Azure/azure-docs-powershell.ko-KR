---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueue.md
ms.openlocfilehash: 1c3f258f4aecbeb492e0e60e274c5e702ae1a3f2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324729"
---
# New-AzStorageQueue

## SYNOPSIS
저장소 큐를 만듭니다.

## 구문

```
New-AzStorageQueue [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명
**New-AzStorageQueue** cmdlet은 Azure에서 저장소 큐를 만듭니다.

## 예제

### 예제 1: Azure 저장소 큐 만들기
```
PS C:\>New-AzStorageQueue -Name "queueabc"
```

이 예제에서는 queueabc라는 저장소 큐를 만듭니다.

### 예제 2: 여러 Azure 저장소 큐 만들기
```
PS C:\>"queue1 queue2 queue3".split() | New-AzStorageQueue
```

이 예제에서는 여러 저장소 큐를 만듭니다.
.NET String 클래스의 Split 메서드를 사용하여 파이프라인에 이름을 전달합니다.

## PARAMETERS

### -Context
Azure 저장소 컨텍스트를 지정합니다.
New-AzStorageContext cmdlet을 사용하여 만들 수 있습니다.

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
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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

### -Name
큐의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### System.String

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext

## 출력

### Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue

## 참고 사항

## 관련 링크

[Get-AzStorageQueue](./Get-AzStorageQueue.md)

[Remove-AzStorageQueue](./Remove-AzStorageQueue.md)


