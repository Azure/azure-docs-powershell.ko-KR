---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 38207027-FD76-45EE-8817-88599735C0B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFile.md
ms.openlocfilehash: 8251c18acad2da881c3215df6a2e743b6804af6e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216174"
---
# Get-AzStorageFile

## SYNOPSIS
경로에 대 한 디렉터리 및 파일을 나열 합니다.

## 구문과

### ShareName (기본값)
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

### 디렉토리로
```
Get-AzStorageFile [-Directory] <CloudFileDirectory> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## 설명은
**AzStorageFile** cmdlet은 사용자가 지정 하는 공유 또는 디렉터리에 대 한 디렉터리 및 파일을 나열 합니다.
*Path* 매개 변수를 지정 하 여 지정 된 경로에 있는 디렉터리 또는 파일의 인스턴스를 가져옵니다.
이 cmdlet은 **AzureStorageFile** 및 **azurestoragedirectory** 개체를 반환 합니다.
**Isdirectory** 속성을 사용 하 여 폴더와 파일을 구별할 수 있습니다.

## 예제의

### 예제 1: 공유의 디렉터리 나열
```
PS C:\>Get-AzStorageFile -ShareName "ContosoShare06" | where {$_.GetType().Name -eq "AzureStorageFileDirectory"}
```

이 명령은 공유 ContosoShare06의 디렉터리만 나열 합니다.
먼저 파일과 디렉터리를 모두 검색 하 고 파이프라인 연산자를 사용 하 여 **where** 연산자에 전달한 다음 형식이 "AzureStorageFileDirectory"가 아닌 개체를 삭제 합니다.

### 예제 2: 파일 디렉터리 나열
```
PS C:\> Get-AzStorageFile -ShareName "ContosoShare06" -Path "ContosoWorkingFolder" | Get-AzStorageFile
```

이 명령은 디렉터리 ContosoWorkingFolder의 share ContosoShare06에 있는 파일 및 폴더를 나열 합니다.
먼저 디렉터리 인스턴스를 가져온 다음 **AzStorageFile** cmdlet으로이를 파이프라인 하 여 디렉터리를 나열 합니다.

## 변수

### -ClientTimeoutPerRequest
한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.
이전 호출이 지정 된 간격 내에 실패 하는 경우이 cmdlet은 요청을 다시 시도 합니다.
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
이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 완화 하는 데 도움이 될 수 있습니다.
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

### -컨텍스트
Azure 저장소 컨텍스트를 지정 합니다.
저장소 컨텍스트를 얻으려면 New-AzStorageContext cmdlet을 사용 합니다.

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

### -디렉터리
폴더를 **Cloudfiledirectory** 개체로 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 폴더를 가져옵니다.
디렉터리를 가져오려면 New-AzStorageDirectory cmdlet을 사용 합니다.
**Get-AzStorageFile** cmdlet을 사용 하 여 디렉터리를 가져올 수도 있습니다.

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
폴더의 경로를 지정 합니다.
*Path* 매개 변수를 생략 하면 **AzStorageFile** 에서 지정 된 파일 공유 또는 디렉터리의 디렉터리와 파일을 나열 합니다.
*Path* 매개 변수를 포함 하는 경우 **AzStorageFile** 는 지정 된 경로에 있는 디렉터리 또는 파일의 인스턴스를 반환 합니다.

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
요청에 대 한 서비스 쪽 시간 제한 간격 (초)을 지정 합니다.
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

### -공유
**Cloudfileshare** 되지 않는 개체를 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 파일 공유에서 파일 또는 디렉터리를 가져옵니다.
**Cloudfileshare** 되지 않는 개체를 가져오려면 Get-AzStorageShare cmdlet을 사용 합니다.
이 개체는 저장소 컨텍스트를 포함 합니다.
이 매개 변수를 지정 하는 경우 *컨텍스트* 매개 변수를 지정 하지 마세요.

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
파일 공유의 이름을 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 파일 공유에서 파일 또는 디렉터리를 가져옵니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### Microsoft. c m m. c a c 파일 공유

### Microsoft. c l i 파일 디렉터리

### Microsoft. Azure. 일반. IStorageContext

## 출력

### WindowsAzure. ResourceModel를 AzureStorageFile로 저장 합니다.

## 상속자

## 관련 링크

[Get-AzStorageFileContent](./Get-AzStorageFileContent.md)

[새로운 AzStorageDirectory](./New-AzStorageDirectory.md)

[제거-AzStorageDirectory](./Remove-AzStorageDirectory.md)

[제거-AzStorageFile](./Remove-AzStorageFile.md)

[Set-AzStorageFileContent](./Set-AzStorageFileContent.md)


