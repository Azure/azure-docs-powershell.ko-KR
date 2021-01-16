---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: CBD157D2-37C5-491F-A806-6B39F1D0415A
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblobcopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobCopyState.md
ms.openlocfilehash: 319463dfb80cddbbffe5b7d1652a04f98e285768
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325058"
---
# Get-AzStorageBlobCopyState

## SYNOPSIS
Azure Storage Blob의 복사 상태를 얻습니다.

## 구문

### NamePipeline(기본값)
```
Get-AzStorageBlobCopyState [-Blob] <String> [-Container] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### BlobPipeline
```
Get-AzStorageBlobCopyState -CloudBlob <CloudBlob> [-WaitForComplete] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### ContainerPipeline
```
Get-AzStorageBlobCopyState -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## 설명
**Get-AzStorageBlobCopyState** cmdlet은 Azure Storage Blob의 복사 상태를 얻습니다.
복사 대상 Blob에서 실행해야 합니다.

## 예제

### 예제 1: Blob의 복사 상태 확인
```
C:\PS>Get-AzStorageBlobCopyState -Blob "ContosoPlanning2015" -Container "ContosoUploads"
```

이 명령은 ContosoUploads 컨테이너에서 ContosoPlanning2015라는 Blob의 복사 상태를 얻습니다.

### 예제 2: 파이프라인을 사용하여 Blob의 복사 상태 얻기
```
C:\PS>Get-AzStorageBlob -Blob "ContosoPlanning2015" -Container "ContosoUploads" | Get-AzStorageBlobCopyState
```

이 명령은 **Get-AzStorageBlob** cmdlet을 사용하여 ContosoUploads라는 컨테이너에서 ContosoPlanning2015라는 Blob을 얻은 다음 파이프라인 연산자를 사용하여 현재 cmdlet에 결과를 전달합니다.
**Get-AzStorageBlobCopyState** cmdlet은 해당 Blob에 대한 복사 상태를 얻습니다.

### 예제 3: 파이프라인을 사용하여 컨테이너의 Blob에 대한 복사 상태 확인
```
C:\PS>Get-AzStorageContainer -Name "ContosoUploads" | Get-AzStorageBlobCopyState -Blob "ContosoPlanning2015"
```

이 명령은 **Get-AzStorageBlob** cmdlet을 사용하여 컨테이너 이름을 지정한 다음 결과를 현재 cmdlet에 전달합니다.
**Get-AzStorageContainer** cmdlet은 해당 컨테이너에서 ContosoPlanning2015라는 Blob에 대한 복사 상태를 얻습니다.

### 예제 4: 복사 및 파이프라인을 시작하여 복사 상태 얻기
```
C:\PS> $destBlob = Start-AzStorageBlobCopy -SrcContainer "contosouploads" -SrcBlob "ContosoPlanning2015" -DestContainer "contosouploads2" -DestBlob "ContosoPlanning2015_copy"

C:\PS> $destBlob | Get-AzStorageBlobCopyState
```

첫 번째 명령은 Blob "ContosoPlanning2015"를 "ContosoPlanning2015_copy"로 복사하고 destiantion Blob 개체를 출력합니다. 두 번째 명령 파이프라인은 Destiantion Blob 개체를 Get-AzStorageBlobCopyState로 파이프라인하여 Blob 복사 상태를 얻습니다. 

## PARAMETERS

### -Blob
Blob의 이름을 지정합니다.
이 cmdlet은 이 매개 변수가 지정하는 Azure Storage Blob에 대한 Blob 복사 작업의 상태를 얻습니다.

```yaml
Type: System.String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClientTimeoutPerRequest
하나의 서비스 요청에 대해 클라이언트 쪽 시간(초)을 지정합니다.
이전 호출이 지정된 간격에서 실패하는 경우 이 cmdlet은 요청을 다시 검색합니다.
이 cmdlet이 간격이 경과하기 전에 성공적인 응답을 받지 못하면 이 cmdlet은 오류를 반환합니다.

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

### -CloudBlob
Azure Storage 클라이언트 라이브러리의 **CloudBlob** 개체를 지정합니다.
**CloudBlob 개체를 얻으면** Get-AzStorageBlob cmdlet을 사용합니다.

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CloudBlobContainer
Azure Storage 클라이언트 라이브러리에서 **CloudBlobContainer** 개체를 지정합니다.
이 cmdlet은 이 매개 변수가 지정하는 컨테이너에 있는 Blob의 복사 상태를 얻습니다.
**CloudBlobContainer** 개체를 얻습니다. Get-AzStorageContainer cmdlet을 사용합니다.

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConcurrentTaskCount
최대 동시 네트워크 호출을 지정합니다.
이 매개 변수를 사용하여 최대 동시 네트워크 호출 수를 지정하여 동시성으로 로컬 CPU 및 대역폭 사용량을 제한할 수 있습니다.
지정된 값은 절대 개수로, 코어 수에 곱하지 않습니다.
이 매개 변수는 초당 100킬로비트와 같은 낮은 대역폭 환경에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.
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

### -Container
컨테이너의 이름을 지정합니다.
이 cmdlet은 이 매개 변수가 지정하는 컨테이너의 Blob에 대한 복사 상태를 얻습니다.

```yaml
Type: System.String
Parameter Sets: NamePipeline
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Context
Azure 저장소 컨텍스트를 지정합니다.
저장소 컨텍스트를 얻습니다. New-AzStorageContext cmdlet을 사용 합니다.

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

### -ServerTimeoutPerRequest
요청에 대한 서비스 쪽 시간제한 간격(초)을 지정합니다.
지정된 간격이 서비스에서 요청을 처리하기 전에 경과하면 저장소 서비스가 오류를 반환합니다.

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

### -WaitForComplete
이 cmdlet이 복사본이 완료될 때까지 기다렸다는 것입니다.
이 매개 변수를 지정하지 않으면 이 cmdlet은 결과를 즉시 반환합니다.

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

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### Microsoft.Azure.Storage.Blob.CloudBlob

### Microsoft.Azure.Storage.Blob.CloudBlobContainer

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext

## 출력

### Microsoft.Azure.Storage.Blob.CopyState

## 참고 사항

## 관련 링크

[Start-AzStorageBlobCopy](./Start-AzStorageBlobCopy.md)

[Stop-AzStorageBlobCopy](./Stop-AzStorageBlobCopy.md)


