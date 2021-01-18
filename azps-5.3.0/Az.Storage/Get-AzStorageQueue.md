---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueue.md
ms.openlocfilehash: df4d31c1a90808e4d289cab60c5edf9785de1182
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494705"
---
# Get-AzStorageQueue

## SYNOPSIS
저장소 큐를 나열합니다.

## 구문

### QueueName(기본값)
```
Get-AzStorageQueue [[-Name] <String>] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### QueuePrefix
```
Get-AzStorageQueue -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명
**Get-AzStorageQueue** cmdlet은 Azure Storage 계정과 연결된 스토리지 큐를 나열합니다.

## 예제

### 예제 1: 모든 Azure Storage 큐 나열
```
PS C:\>Get-AzStorageQueue
```

이 명령은 현재 Storage 계정에 대한 모든 저장소 큐 목록을 얻습니다.

### 예제 2: 와일드카드 문자를 사용하여 Azure Storage 큐 나열
```
PS C:\>Get-AzStorageQueue -Name queue*
```

이 명령은 와일드카드 문자를 사용하여 이름이 큐로 시작하는 저장소 큐 목록을 얻습니다.

### 예제 3: 큐 이름 사전을 사용하여 Azure Storage 큐 나열
```
PS C:\>Get-AzStorageQueue -Prefix "queue"
```

이 예제에서는 *Prefix* 매개 변수를 사용하여 이름이 큐로 시작하는 저장소 큐 목록을 얻습니다.

## PARAMETERS

### -Context
Azure 저장소 컨텍스트를 지정합니다.
**New-AzStorageContext** cmdlet을 사용하여 만들 수 있습니다.

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
이름을 지정합니다.
이름을 지정하지 않으면 cmdlet은 모든 큐의 목록을 얻습니다.
전체 또는 부분 이름을 지정하면 cmdlet은 이름 패턴과 일치하는 모든 큐를 얻습니다.

```yaml
Type: System.String
Parameter Sets: QueueName
Aliases: N, Queue

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Prefix
얻게 할 큐 이름에 사용되는 prefix를 지정합니다.

```yaml
Type: System.String
Parameter Sets: QueuePrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

[New-AzStorageQueue](./New-AzStorageQueue.md)

[Remove-AzStorageQueue](./Remove-AzStorageQueue.md)


