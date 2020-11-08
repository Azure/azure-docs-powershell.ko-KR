---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchresourcefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
ms.openlocfilehash: 43cbf86ca473b6984ee2190b1d10df61b6d32e64
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042439"
---
# New-AzBatchResourceFile

## SYNOPSIS
에서 사용 하도록 리소스 파일을 만듭니다 `New-AzBatchTask` .

## 구문과

### HttpUrl (기본값)
```
New-AzBatchResourceFile -HttpUrl <String> -FilePath <String> [-FileMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### StorageContainerUrl
```
New-AzBatchResourceFile [-FilePath <String>] [-FileMode <String>] [-BlobPrefix <String>]
 -StorageContainerUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### AutoStorageContainerName
```
New-AzBatchResourceFile [-FilePath <String>] [-FileMode <String>] -AutoStorageContainerName <String>
 [-BlobPrefix <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
에서 사용 하도록 리소스 파일을 만듭니다 `New-AzBatchTask` .

## 예제의

### 예제 1: 단일 파일을 가리키는 HTTP URL에서 리소스 파일 만들기
```
PS C:\> $file = New-AzBatchResourceFile -HttpUrl "https://testacct.blob.core.windows.net/" -FilePath "file1"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

`PSResourceFile`HTTP url 참조를 만듭니다.

### 예제 2: Azure Storage 컨테이너 URL에서 리소스 파일 만들기
```
PS C:\> $file = New-AzBatchResourceFile -StorageContainerUrl "https://testacct.blob.core.windows.net/mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

`PSResourceFile`Azure 저장소 컨테이너 URL 참조를 만듭니다. 컨테이너의 모든 파일이 지정 된 폴더에 다운로드 됩니다.

### 예제 3: 자동 저장소 컨테이너 이름에서 리소스 파일 만들기
```
PS C:\> $file = New-AzBatchResourceFile -AutoStorageContainerName "mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

`PSResourceFile`자동 저장소 컨테이너 이름을 참조 하 여 만듭니다. 컨테이너의 모든 파일이 지정 된 폴더에 다운로드 됩니다.

## 변수

### -AutoStorageContainerName
자동 저장소 계정의 저장소 컨테이너 이름입니다.

```yaml
Type: System.String
Parameter Sets: AutoStorageContainerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BlobPrefix
Azure Storage 컨테이너에서 blob을 다운로드할 때 사용할 blob 접두사를 가져옵니다.
이름이 지정 된 접두사로 시작 하는 blob만 다운로드 됩니다.
이 접두사는 부분적인 파일 이름 또는 하위 디렉터리인 수 있습니다.
접두사를 지정 하지 않으면 컨테이너의 모든 파일이 다운로드 됩니다.

```yaml
Type: System.String
Parameter Sets: StorageContainerUrl, AutoStorageContainerName
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
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FileMode
파일 사용 권한 모드 특성을 8 진수 형식으로 가져옵니다.
이 속성은 리소스 파일이 Linux 노드에 다운로드 된 경우에만 적용 됩니다.
이 속성이 Linux 노드에 대해 지정 되지 않은 경우 기본값은 0770입니다.

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

### -FilePath
작업의 작업 디렉터리를 기준으로 파일을 다운로드할 계산 노드의 위치입니다. HttpUrl 매개 변수를 지정 하면 FilePath가 필요 하며 파일 이름을 포함 하 여 파일이 다운로드 되는 경로를 설명 합니다. 그렇지 않고 AutoStorageContainerName 또는 StorageContainerUrl 매개 변수를 지정 하는 경우 FilePath는 선택 사항이 며 파일을 다운로드할 디렉터리입니다. FilePath가 디렉터리로 사용 되는 경우 입력 데이터와 이미 연결 된 디렉터리 구조는 full에 유지 되 고 지정 된 FilePath 디렉터리에 추가 됩니다. 지정 된 상대 경로는 작업의 작업 디렉터리를 분리할 수 없습니다 (예: '. ' 사용).

```yaml
Type: System.String
Parameter Sets: HttpUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: StorageContainerUrl, AutoStorageContainerName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HttpUrl
다운로드할 파일의 URL입니다.
URL이 Azure Blob Storage 인 경우 익명 액세스를 사용 하 여 읽을 수 있어야 합니다. 즉, 일괄 처리 서비스는 blob을 다운로드할 때 자격 증명을 제공 하지 않습니다.
Azure storage에서 blob에 대 한 이러한 URL을 가져오는 데는 다음 두 가지 방법이 있습니다. blob에 대 한 읽기 권한을 부여 하는 SA (공유 액세스 서명)를 포함 하거나 blob 또는 해당 컨테이너의 ACL을 설정 하 여 공용 액세스를 허용 합니다.

```yaml
Type: System.String
Parameter Sets: HttpUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageContainerUrl
Azure Blob Storage 내의 blob 컨테이너에 대 한 URL입니다.
이 URL은 읽기 가능 하 고 익명 액세스를 사용 하 여 목록에 표시할 수 있어야 합니다. 즉, 일괄 처리 서비스는 컨테이너에서 blob을 다운로드할 때 자격 증명을 제공 하지 않습니다.
Azure storage에서 컨테이너에 대 한 URL을 가져오는 데 사용할 수 있는 두 가지 방법이 있습니다. 컨테이너에 대 한 읽기 권한을 부여 하는 SA (공유 액세스 서명)를 포함 하거나 컨테이너에 대 한 ACL을 설정 하 여 공용 액세스를 허용 합니다.

```yaml
Type: System.String
Parameter Sets: StorageContainerUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### 않아야

## 출력

### Microsoft.Azure.Commands.Batch. PSResourceFile

## 상속자

## 관련 링크

[새로운 AzBatchTask](./New-AzBatchTask.md)