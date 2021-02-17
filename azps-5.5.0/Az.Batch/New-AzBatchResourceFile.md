---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchresourcefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
ms.openlocfilehash: 43cbf86ca473b6984ee2190b1d10df61b6d32e64
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205208"
---
# New-AzBatchResourceFile

## SYNOPSIS
에서 사용할 리소스 파일을 `New-AzBatchTask` 만듭니다.

## 구문

### HttpUrl(기본값)
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

## 설명
에서 사용할 리소스 파일을 `New-AzBatchTask` 만듭니다.

## 예제

### 예제 1: 단일 파일을 포인터로 하는 HTTP URL에서 리소스 파일 만들기
```
PS C:\> $file = New-AzBatchResourceFile -HttpUrl "https://testacct.blob.core.windows.net/" -FilePath "file1"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

HTTP URL `PSResourceFile` 참조를 만듭니다.

### 예제 2: Azure Storage 컨테이너 URL에서 리소스 파일 만들기
```
PS C:\> $file = New-AzBatchResourceFile -StorageContainerUrl "https://testacct.blob.core.windows.net/mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

Azure `PSResourceFile` Storage 컨테이너 URL을 참조하는 것을 만듭니다. 컨테이너의 모든 파일은 지정된 폴더에 다운로드됩니다.

### 예제 3: 자동 저장소 컨테이너 이름에서 리소스 파일 만들기
```
PS C:\> $file = New-AzBatchResourceFile -AutoStorageContainerName "mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

자동 저장소 `PSResourceFile` 컨테이너 이름을 참조하는 이름을 만듭니다. 컨테이너의 모든 파일은 지정된 폴더에 다운로드됩니다.

## PARAMETERS

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
Azure Storage 컨테이너에서 Blob을 다운로드할 때 사용할 Blob Prefix를 얻습니다.
이름이 지정된 prefix로 시작하는 Blob만 다운로드됩니다.
이 prefix는 부분 파일 이름 또는 하위디렉트일 수 있습니다.
지정하지 않은 경우 컨테이너의 모든 파일이 다운로드됩니다.

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

### -FileMode
8진수 형식의 파일 사용 권한 모드 특성을 얻습니다.
이 속성은 리소스 파일이 Linux 노드에 다운로드된 경우만 적용할 수 있습니다.
Linux 노드에 대해 이 속성을 지정하지 않으면 기본값은 0770입니다.

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
태스크의 작업 디렉터리를 상대로 파일을 다운로드할 계산 노드의 위치입니다. HttpUrl 매개 변수를 지정하는 경우 FilePath가 필요하며 파일 이름을 포함하여 파일을 다운로드할 경로를 설명합니다. 그렇지 않은 경우 AutoStorageContainerName 또는 StorageContainerUrl 매개 변수가 지정된 경우 FilePath는 선택 사항이며 파일을 다운로드할 디렉터리입니다. FilePath가 디렉터리로 사용되는 경우 입력 데이터와 연결된 모든 디렉터리 구조가 전체로 유지되고 지정된 FilePath 디렉터리에 추가됩니다. 지정된 상대 경로는 작업의 작업 디렉터리를 끊을 수 없습니다(예: '..'를 사용하여).

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
URL이 Azure Blob Storage인 경우 익명 액세스를 사용하여 읽을 수 있어야 합니다. 즉, Batch 서비스는 Blob을 다운로드할 때 자격 증명을 제시하지 않습니다.
Azure Storage에서 Blob에 대한 이러한 URL을 얻을 수 있는 두 가지 방법은 Blob에 대한 읽기 권한을 부여하는 SAS(공유 액세스 서명)를 포함하거나 Blob 또는 해당 컨테이너에 대한 ACL을 설정하여 공용 액세스를 허용하는 것입니다.

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
Azure Blob Storage 내의 Blob 컨테이너의 URL입니다.
이 URL은 익명 액세스를 사용하여 읽을 수 있어야 합니다. 즉, Batch 서비스는 컨테이너에서 Blob을 다운로드할 때 자격 증명을 제시하지 않습니다.
Azure Storage에서 컨테이너에 대한 이러한 URL을 얻을 수 있는 두 가지 방법은 컨테이너에 대한 읽기 권한을 부여하는 SAS(공유 액세스 서명)를 포함하거나 공용 액세스를 허용하도록 컨테이너에 대한 ACL을 설정하는 것입니다.

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### 없음

## 출력

### Microsoft.Azure.Commands.Batch. Models.PSResourceFile

## 참고 사항

## 관련 링크

[New-AzBatchTask](./New-AzBatchTask.md)