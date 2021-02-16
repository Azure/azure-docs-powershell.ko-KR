---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
ms.openlocfilehash: 3c90e02194fa761bbb0fc00e11ea09d03ca00c1c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176657"
---
# Get-AzStorageFileContent

## SYNOPSIS
파일의 내용을 다운로드합니다.

## 구문

### ShareName(기본값)
```
Get-AzStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [-PreserveSMBAttribute] [<CommonParameters>]
```

### 공유
```
Get-AzStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### 디렉터리
```
Get-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [-PreserveSMBAttribute] [<CommonParameters>]
```

### 파일
```
Get-AzStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

## 설명
**Get-AzStorageFileContent** cmdlet은 파일의 내용을 다운로드한 다음 지정한 대상에 저장합니다.
이 cmdlet은 파일의 내용을 반환하지 않습니다.

## 예제

### 예제 1: 폴더에서 파일 다운로드
```
PS C:\>Get-AzStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

이 명령은 ContosoWorkingFolder 폴더의 CurrentDataFile이라는 파일을 파일 공유 ContosoShare06에서 현재 폴더로 다운로드합니다.

### 예제 2: 샘플 파일 공유에서 파일을 다운로드합니다.
```
PS C:\>Get-AzStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzStorageFileContent
```

이 예제에서는 샘플 파일 공유에서 파일을 다운로드합니다.

### 예제 3: 로컬 파일에 Azure 파일을 다운로드하고 로컬 파일에서 Azure 파일 SMB 속성(파일 특성, 파일 생성 시간, 파일 마지막 쓰기 시간)을 보존합니다.
```
PS C:\>Get-AzStorageFileContent -ShareName sample -Path "dir1/file1" -Destination $localFilePath -PreserveSMBAttribute
```

이 예제에서는 Azure 파일을 로컬 파일에 다운로드하고 로컬 파일의 Azure 파일 SMB 속성(파일 특성, 파일 생성 시간, 파일 마지막 쓰기 시간)을 제공합니다.

## PARAMETERS

### -AsJob
백그라운드에서 cmdlet을 실행합니다.

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

### -CheckMd5
다운로드한 파일의 Md5 합계를 확인할지 여부를 지정합니다.

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

### -ClientTimeoutPerRequest
하나의 서비스 요청에 대해 클라이언트 쪽 시간(초)을 지정합니다. 이전 호출이 지정된 간격에서 실패하는 경우 이 cmdlet은 요청을 다시 검색합니다. 이 cmdlet이 간격이 경과하기 전에 성공적인 응답을 받지 못하면 이 cmdlet은 오류를 반환합니다.

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
최대 동시 네트워크 호출을 지정합니다. 이 매개 변수를 사용하여 최대 동시 네트워크 호출 수를 지정하여 동시성으로 로컬 CPU 및 대역폭 사용량을 제한할 수 있습니다. 지정된 값은 절대 개수로, 코어 수에 곱하지 않습니다. 이 매개 변수는 초당 100킬로비트와 같은 낮은 대역폭 환경에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다. 기본값은 10입니다.

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
Azure Storage 컨텍스트를 지정합니다. 컨텍스트를 얻습니다. New-AzStorageContext cmdlet을 사용 합니다.

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

### -Destination
대상 경로를 지정합니다.
이 cmdlet은 이 매개 변수가 지정하는 위치에 파일 콘텐츠를 다운로드합니다.
존재하지 않는 파일의 경로를 지정하는 경우 이 cmdlet은 해당 파일을 만들고 새 파일에 콘텐츠를 저장합니다.
이미 존재하는 파일의 경로를 지정하고 *Force* 매개 변수를 지정하면 cmdlet이 파일을 덮어써 덮어써야 합니다.
기존 파일의 경로를 지정하고 *Force를* 지정하지 않으면 cmdlet에서 계속하기 전에 프롬프트를 표시합니다.
폴더의 경로를 지정하는 경우 이 cmdlet은 Azure 저장소 파일의 이름이 있는 파일을 만들 시도합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Directory
폴더를 **CloudFileDirectory 개체로 지정합니다.**
이 cmdlet은 이 매개 변수가 지정하는 폴더의 파일에 대한 콘텐츠를 얻습니다.
디렉터리를 얻습니다. New-AzStorageDirectory cmdlet을 사용 합니다.
또한 Get-AzStorageFile cmdlet을 사용하여 디렉터리를 얻을 수 있습니다.

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

### -File
파일을 **CloudFile 개체로 지정합니다.**
이 cmdlet은 이 매개 변수가 지정하는 파일을 얻습니다.
**CloudFile** 개체를 얻습니다. Get-AzStorageFile cmdlet을 사용합니다.

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: File
Aliases: CloudFile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Force
존재하지 않는 파일의 경로를 지정하는 경우 이 cmdlet은 해당 파일을 만들고 새 파일에 콘텐츠를 저장합니다.
이미 존재하는 파일의 경로를 지정하고 *Force* 매개 변수를 지정하면 cmdlet이 파일을 덮어써 덮어써야 합니다.
기존 파일의 경로를 지정하고 *Force를* 지정하지 않으면 cmdlet에서 계속하기 전에 프롬프트를 표시합니다.
폴더의 경로를 지정하는 경우 이 cmdlet은 Azure 저장소 파일의 이름이 있는 파일을 만들 시도합니다.

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

### -PassThru
이 cmdlet이 다운로드한 **AzureStorageFile** 개체를 반환합니다.

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

### -Path
파일의 경로를 지정합니다.
이 cmdlet은 이 매개 변수가 지정하는 파일을 제공합니다.
파일이 없는 경우 이 cmdlet은 오류를 반환합니다.

```yaml
Type: System.String
Parameter Sets: ShareName, Share, Directory
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PreserveSMBAttribute
원본 파일 SMB 속성(파일 특성, 파일 생성 시간, 파일 마지막 쓰기 시간)을 대상 파일에 보관합니다. 이 매개 변수는 Windows에서만 사용할 수 있습니다.

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

### -ServerTimeoutPerRequest
요청에 대한 서비스 쪽 시간제한 간격(초)을 지정합니다. 지정된 간격이 서비스에서 요청을 처리하기 전에 경과하면 저장소 서비스가 오류를 반환합니다.

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
이 cmdlet은 이 매개 변수가 지정한 공유에서 파일의 내용을 다운로드합니다.
**CloudFileShare** 개체를 얻습니다. Get-AzStorageShare cmdlet을 사용합니다.
이 개체에는 저장소 컨텍스트가 포함되어 있습니다.
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
이 cmdlet은 이 매개 변수가 지정한 공유에서 파일의 내용을 다운로드합니다.

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

### -Confirm
cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
cmdlet이 실행되는 경우의 결과 표시
cmdlet이 실행되지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### Microsoft.Azure.Storage.File.CloudFileShare

### Microsoft.Azure.Storage.File.CloudFileDirectory

### Microsoft.Azure.Storage.File.CloudFile

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext

## 출력

### Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile

## 참고 사항

## 관련 링크

[Get-AzStorageFile](./Get-AzStorageFile.md)

[Set-AzStorageFileContent](./Set-AzStorageFileContent.md)


