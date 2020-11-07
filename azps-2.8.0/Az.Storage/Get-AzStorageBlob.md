---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E54BFD3A-CD54-4E6B-9574-92B8D3E88FF3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlob.md
ms.openlocfilehash: dc825c5c79c3e314fc6b330c441f82543cc9fd23
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93874104"
---
# Get-AzStorageBlob

## SYNOPSIS
컨테이너의 blob을 나열 합니다.

## 구문과

### BlobName (기본값)
```
Get-AzStorageBlob [[-Blob] <String>] [-Container] <String> [-IncludeDeleted] [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### BlobPrefix
```
Get-AzStorageBlob [-Prefix <String>] [-Container] <String> [-IncludeDeleted] [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## 설명은
**AzStorageBlob** Cmdlet은 Azure 저장소 계정의 지정 된 컨테이너에 blob 목록을 표시 합니다.

## 예제의

### 예제 1: blob 이름으로 blob 가져오기
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Blob blob*
```

이 명령은 blob 이름과 와일드 카드를 사용 하 여 blob를 가져옵니다.

### 예제 2: 파이프라인을 사용 하 여 컨테이너의 blob 가져오기
```
PS C:\>Get-AzStorageContainer -Name container* | Get-AzStorageBlob -IncludeDeleted

   Container Uri: https://storageaccountname.blob.core.windows.net/container1

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime         IsDeleted 
----                 --------  ------          -----------                    ------------         ---------- ------------         --------- 
test1                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:19Z            2017-11-08 08:19:32Z True      
test1                BlockBlob 403116          application/octet-stream       2017-11-08 09:00:29Z                                 True      
test2                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:00Z                                 False
```

이 명령은 파이프라인을 사용 하 여 컨테이너에 모든 blob (삭제 된 상태의 blob 포함)를 가져옵니다.

### 예제 3: 이름 접두사로 blob 가져오기
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Prefix "blob"
```

이 명령은 이름 접두사를 사용 하 여 blob를 가져옵니다.

### 예제 4: 여러 일괄 처리에 blob 나열
```
PS C:\>$MaxReturn = 10000
PS C:\> $ContainerName = "abc"
PS C:\> $Total = 0
PS C:\> $Token = $Null
PS C:\> do
 {
     $Blobs = Get-AzStorageBlob -Container $ContainerName -MaxCount $MaxReturn  -ContinuationToken $Token
     $Total += $Blobs.Count
     if($Blobs.Length -le 0) { Break;}
     $Token = $Blobs[$blobs.Count -1].ContinuationToken;
 }
 While ($Token -ne $Null)
PS C:\> Echo "Total $Total blobs in container $ContainerName"
```

이 예제에서는 *MaxCount* 및 *ContinuationToken* 매개 변수를 사용 하 여 Azure Storage blob을 여러 일괄 처리로 나열 합니다.
처음 4 개의 명령은 예제에서 사용할 변수에 값을 할당 합니다.
다섯 번째 명령은 **AzStorageBlob** cmdlet을 사용 하 여 blob을 가져오는 **Do While** 문을 지정 합니다.
이 문에는 $Token 변수에 저장 된 연속 토큰이 포함 됩니다.
루프가 실행 되는 동안 값이 변경 $Token.
자세한 내용은을 입력 `Get-Help About_Do` 하세요.
마지막 명령은 **Echo** 명령을 사용 하 여 합계를 표시 합니다.

## 변수

### -Blob
와일드 카드 검색에 사용할 수 있는 이름 또는 이름 패턴을 지정 합니다.
Blob 이름이 지정 되지 않은 경우 cmdlet은 지정 된 컨테이너의 모든 blob을 나열 합니다.
이 매개 변수에 대 한 값이 지정 된 경우 cmdlet은 이름이이 매개 변수와 일치 하는 모든 blob를 나열 합니다.

```yaml
Type: System.String
Parameter Sets: BlobName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClientTimeoutPerRequest
한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.
이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.
이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.

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
최대 동시 네트워크 통화를 지정 합니다.
이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.
지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.
이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.
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

### -컨테이너
컨테이너의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -컨텍스트
Blob 목록을 가져오는 데 사용할 Azure storage 계정을 지정 합니다.
New-AzStorageContext cmdlet을 사용 하 여 저장소 컨텍스트를 만들 수 있습니다.

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

### -ContinuationToken
Blob 목록에 대 한 연속 토큰을 지정 합니다.
이 매개 변수와 *MaxCount* 매개 변수를 사용 하 여 여러 일괄 처리에 blob 목록을 표시 합니다.

```yaml
Type: Microsoft.Azure.Storage.Blob.BlobContinuationToken
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -IncludeDeleted
삭제 된 Blob 포함 기본적으로 blob는 삭제 된 blob를 포함 하지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxCount
이 cmdlet이 반환 하는 최대 개체 수를 지정 합니다.

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

### -접두사
가져오려는 blob 이름에 대 한 접두사를 지정 합니다.
이 매개 변수는 정규식 또는 와일드 카드 문자를 사용 하 여 검색 하는 것을 지원 하지 않습니다.
즉, 컨테이너에 "My", "MyBlob1", "MyBlob2" 이라는 blob만 있고 "-Prefix My *"를 지정 하면 cmdlet은 blob을 반환 하지 않습니다.
그러나 "-Prefix My"를 지정 하면 cmdlet은 "My", "MyBlob1", "MyBlob2"를 반환 합니다.

```yaml
Type: System.String
Parameter Sets: BlobPrefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
요청에 대 한 서비스 측 시간 제한 간격 (초)을 지정 합니다.
서비스가 요청을 처리 하기 전에 지정 된 간격이 경과 하면 저장소 서비스에서 오류를 반환 합니다.

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

### Microsoft. Azure. 일반. IStorageContext

## 출력

### WindowsAzure. ResourceModel. m b m.

## 상속자

## 관련 링크

[Get-AzStorageBlobContent](./Get-AzStorageBlobContent.md)

[제거-AzStorageBlob](./Remove-AzStorageBlob.md)

[Set-AzStorageBlobContent](./Set-AzStorageBlobContent.md)


