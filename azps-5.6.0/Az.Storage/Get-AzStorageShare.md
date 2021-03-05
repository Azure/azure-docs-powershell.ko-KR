---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FD3A0013-4365-4E65-891C-5C50A9D5658C
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShare.md
ms.openlocfilehash: 88655ed408242794c6f23a7b170dc007a11ced50
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005040"
---
# Get-AzStorageShare

## SYNOPSIS
파일 공유 목록을 얻습니다.

## 구문

### MatchingPrefix(기본값)
```
Get-AzStorageShare [[-Prefix] <String>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### 특정
```
Get-AzStorageShare [-Name] <String> [[-SnapshotTime] <DateTimeOffset>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## 설명
**Get-AzStorageShare** cmdlet은 저장소 계정에 대한 파일 공유 목록을 제공합니다.

## 예제

### 예제 1: 파일 공유를 다운로드합니다.
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06"
```

이 명령은 ContosoShare06이라는 파일 공유를 얻습니다.

### 예제 2: 문자열로 시작하는 모든 파일 공유를 얻습니다.
```
PS C:\>Get-AzStorageShare -Prefix "Contoso"
```

이 명령은 Contoso로 시작하는 이름이 있는 모든 파일 공유를 얻습니다.

### 예제 3: 지정된 컨텍스트에서 모든 파일 공유를 얻습니다.
```
PS C:\>$Context = New-AzStorageContext -Local
PS C:\> Get-AzStorageShare -Context $Context
```

첫 번째 명령은 **New-AzStorageContext** cmdlet을 사용하여 *로컬* 매개 변수를 사용하여 컨텍스트를 만든 다음 해당 컨텍스트 개체를 $Context 저장합니다.
두 번째 명령은 에 저장된 컨텍스트 개체에 대한 파일 공유를 $Context.

### 예제 4: 특정 공유 이름 및 스냅숏타임으로 파일 공유 스냅숏 만들기
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06" -SnapshotTime "6/16/2017 9:48:41 AM +00:00"
```

이 명령은 특정 공유 이름 및 스냅숏타임이 포함된 파일 공유 스냅숏을 얻습니다.

## 매개 변수

### -ClientTimeoutPerRequest
하나의 서비스 요청에 대해 클라이언트 쪽 시간 간격(초)을 지정합니다.
지정된 간격에서 이전 호출이 실패하면 이 cmdlet에서 요청을 다시 검색합니다.
간격이 경과하기 전에 이 cmdlet에서 성공적인 응답을 받지 못하면 이 cmdlet은 오류를 반환합니다.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConcurrentTaskCount
최대 동시 네트워크 호출을 지정합니다.
이 매개 변수를 사용하여 최대 동시 네트워크 호출 수를 지정하여 로컬 CPU 및 대역폭 사용량을 제한하는 동시성 제한할 수 있습니다.
지정된 값은 절대 개수로 코어 수에 곱하지 않습니다.
이 매개 변수는 초당 100킬로비트와 같은 대역폭이 낮은 환경에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.
기본값은 10입니다.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Context
Azure Storage 컨텍스트를 지정합니다.
컨텍스트를 얻은 경우 [New-AzStorageContext](./New-AzStorageContext.md) cmdlet을 사용 합니다.

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
Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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
파일 공유의 이름을 지정합니다.
이 cmdlet은 이 매개 변수가 지정하는 파일 공유를 얻거나 존재하지 않는 파일 공유의 이름을 지정하는 경우 아무 것도 얻지 않습니다.

```yaml
Type: System.String
Parameter Sets: Specific
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Prefix
파일 공유에 대한 사전을 지정합니다.
이 cmdlet은 이 매개 변수가 지정한 도두와 일치하는 파일 공유를 얻거나, 파일 공유가 지정된된 연결과 일치하지 않으면 파일 공유가 없습니다.

```yaml
Type: System.String
Parameter Sets: MatchingPrefix
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
요청의 서버 부분에 대한 시간 제한 기간의 길이를 지정합니다.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SnapshotTime
수신할 파일 공유 스냅숏의 SnapshotTime입니다.

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: Specific
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.

## 입력

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext

## 출력

### Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare

## 참고 사항

## 관련 링크

[New-AzStorageShare](./New-AzStorageShare.md)

[Remove-AzStorageShare](./Remove-AzStorageShare.md)
