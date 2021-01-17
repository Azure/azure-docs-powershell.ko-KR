---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 38207027-FD76-45EE-8817-88599735C0B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFile.md
ms.openlocfilehash: 8251c18acad2da881c3215df6a2e743b6804af6e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489295"
---
# Get-AzStorageFile

## SYNOPSIS
경로에 대한 폴더 및 파일을 나열합니다.

## 구문

### ShareName(기본값)
```
Get-AzStorageFile [-ShareName] <String> [[-Path] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### 공유
```
Get-AzStorageFile [-Share] <CloudFileShare> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### 디렉터리
```
Get-AzStorageFile [-Directory] <CloudFileDirectory> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## 설명
**Get-AzStorageFile** cmdlet은 사용자가 지정한 공유 또는 디렉터리에 대한 디렉터리 및 파일을 나열합니다.
경로 매개 *변수를 지정하여* 지정된 경로에서 디렉터리 또는 파일의 인스턴스를 얻습니다.
이 cmdlet은 **AzureStorageFile** 및 **AzureStorageDirectory 개체를 반환합니다.**
**IsDirectory** 속성을 사용하여 폴더와 파일을 구분할 수 있습니다.

## 예제

### 예제 1: 공유의 목록
```
PS C:\>Get-AzStorageFile -ShareName "ContosoShare06" | where {$_.GetType().Name -eq "AzureStorageFileDirectory"}
```

이 명령은 ContosoShare06 공유에 있는 감독자만 나열합니다.
먼저 파일과 디렉터를 모두 검색하고, 파이프라인 연산자를 사용하여 **where** 연산자에 전달한 다음, 형식이 "AzureStorageFileDirectory"가 아닌 모든 개체를 삭제합니다.

### 예제 2: 파일 디렉터리 나열
```
PS C:\> Get-AzStorageFile -ShareName "ContosoShare06" -Path "ContosoWorkingFolder" | Get-AzStorageFile
```

이 명령은 ContosoShare06 공유 아래에 ContosoWorkingFolder 디렉터리의 파일 및 폴더를 나열합니다.
먼저 디렉터리 인스턴스를 얻은 다음 **Get-AzStorageFile** cmdlet에 파이프라인을 추가하여 디렉터리를 나열합니다.

## PARAMETERS

### -ClientTimeoutPerRequest
하나의 서비스 요청에 대해 클라이언트 쪽 시간 시간(초)을 지정합니다.
이전 호출이 지정된 간격 내에 실패하면 이 cmdlet은 요청을 다시 검색합니다.
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

### -ConcurrentTaskCount
최대 동시 네트워크 호출을 지정합니다.
이 매개 변수를 사용하여 최대 동시 네트워크 호출 수를 지정하여 동시성으로 로컬 CPU 및 대역폭 사용량을 제한할 수 있습니다.
지정된 값은 절대 개수로, 코어 수에 곱하지 않습니다.
이 매개 변수는 초당 100킬로비트와 같은 낮은 대역폭 환경에서 네트워크 연결 문제를 완화하는 데 도움이 될 수 있습니다.
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
Storage 컨텍스트를 얻습니다. New-AzStorageContext cmdlet을 사용 합니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareName
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

### -Directory
폴더를 **CloudFileDirectory 개체로 지정합니다.**
이 cmdlet은 이 매개 변수가 지정하는 폴더를 얻습니다.
디렉터리를 얻습니다. New-AzStorageDirectory cmdlet을 사용 합니다.
**Get-AzStorageFile** cmdlet을 사용하여 디렉터리를 얻을 수 있습니다.

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases: CloudFileDirectory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Path
폴더의 경로를 지정합니다.
*Path* 매개 변수를 생략하면 **Get-AzStorageFile은** 지정된 파일 공유 또는 디렉터리의 디렉터리 및 파일을 나열합니다.
Path 매개 *변수를 포함하면* **Get-AzStorageFile은** 지정된 경로에 디렉터리 또는 파일의 인스턴스를 반환합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
요청에 대한 서비스 쪽 시간 제한 간격(초)을 지정합니다.
지정된 간격이 서비스에서 요청을 처리하기 전에 경과하면 Storage 서비스는 오류를 반환합니다.

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

### -공유
**CloudFileShare 개체를 지정합니다.**
이 cmdlet은 이 매개 변수가 지정하는 파일 공유에서 파일 또는 디렉터리를 얻습니다.
**CloudFileShare** 개체를 얻습니다. Get-AzStorageShare cmdlet을 사용합니다.
이 개체에는 Storage 컨텍스트가 포함되어 있습니다.
이 매개 변수를 지정하는 경우 Context 매개 변수를 *지정하지* 않습니다.

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases: CloudFileShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ShareName
파일 공유의 이름을 지정합니다.
이 cmdlet은 이 매개 변수가 지정하는 파일 공유에서 파일 또는 디렉터리를 얻습니다.

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### Microsoft.Azure.Storage.File.CloudFileShare

### Microsoft.Azure.Storage.File.CloudFileDirectory

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext

## 출력

### Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile

## 참고 사항

## 관련 링크

[Get-AzStorageFileContent](./Get-AzStorageFileContent.md)

[New-AzStorageDirectory](./New-AzStorageDirectory.md)

[Remove-AzStorageDirectory](./Remove-AzStorageDirectory.md)

[Remove-AzStorageFile](./Remove-AzStorageFile.md)

[Set-AzStorageFileContent](./Set-AzStorageFileContent.md)


