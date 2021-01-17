---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FA98E64B-D589-4653-9ACC-86573FAF4550
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageFileContent.md
ms.openlocfilehash: 3fed30a260532378274e2df815d6e4b252c018f6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348266"
---
# Set-AzStorageFileContent

## SYNOPSIS
파일의 내용을 업로드합니다.

## 구문

### ShareName(기본값)
```
Set-AzStorageFileContent [-ShareName] <String> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### 공유
```
Set-AzStorageFileContent [-Share] <CloudFileShare> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### 디렉터리
```
Set-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

## 설명
**Set-AzStorageFileContent** cmdlet은 파일의 내용을 지정된 공유의 파일에 업로드합니다.

## 예제

### 예제 1: 현재 폴더에 파일 업로드
```
PS C:\>Set-AzStorageFileContent -ShareName "ContosoShare06" -Source "DataFile37" -Path "ContosoWorkingFolder/CurrentDataFile"
```

이 명령은 현재 폴더의 DataFile37이라는 파일을 ContosoWorkingFolder 폴더의 CurrentDataFile이라는 파일로 업로드합니다.

### 예제 2: 현재 폴더에 있는 모든 파일 업로드
```
PS C:\>$CurrentFolder = (Get-Item .).FullName
PS C:\> $Container = Get-AzStorageShare -Name "ContosoShare06"
PS C:\> Get-ChildItem -Recurse | Where-Object { $_.GetType().Name -eq "FileInfo"} | ForEach-Object {
    $path=$_.FullName.Substring($Currentfolder.Length+1).Replace("\","/")
    Set-AzStorageFileContent -Share $Container -Source $_.FullName -Path $path -Force
}
```

이 예제에서는 몇 가지 일반적인 Windows PowerShell cmdlet 및 현재 cmdlet을 사용하여 현재 폴더의 모든 파일을 컨테이너 ContosoShare06의 루트 폴더에 업로드합니다.
첫 번째 명령은 현재 폴더의 이름을 사용하여 폴더의 $CurrentFolder 저장합니다.
두 번째 명령은 **Get-AzStorageShare** cmdlet을 사용하여 ContosoShare06이라는 파일 공유를 다운로드한 다음, $Container 변수에 저장합니다.
마지막 명령은 현재 폴더의 내용을 사용하고 파이프라인 연산자를 사용하여 각 폴더를 Where-Object cmdlet에 전달합니다.
해당 cmdlet은 파일이 아닌 개체를 필터한 다음 파일을 ForEach-Object cmdlet에 전달합니다.
해당 cmdlet은 각 파일에 대해 적절한 경로를 만든 다음 현재 cmdlet을 사용하여 파일을 업로드하는 스크립트 블록을 실행합니다.
결과는 이 예제에서 업로드하는 다른 파일과 관련하여 이름과 상대 위치가 동일합니다.
스크립트 블록에 대한 자세한 내용은 `Get-Help about_Script_Blocks` .를 입력합니다.

### 예제 3: Azure 파일에 로컬 파일을 업로드하고 Azure 파일의 로컬 파일 SMB 속성(파일 특성, 파일 생성 시간, 파일 마지막 쓰기 시간)을 보존합니다.
```
PS C:\>Get-AzStorageFileContent -source $localFilePath -ShareName sample -Path "dir1/file1" -PreserveSMBAttribute
```

이 예제에서는 로컬 파일을 Azure 파일에 업로드하고 Azure 파일의 로컬 파일 SMB 속성(파일 특성, 파일 생성 시간, 파일 마지막 쓰기 시간)을 보존합니다.

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

### -Context
Azure 저장소 컨텍스트를 지정합니다.
저장소 컨텍스트를 얻습니다. [New-AzStorageContext](./New-AzStorageContext.md) cmdlet을 사용 합니다.

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
이 cmdlet은 이 매개 변수가 지정하는 폴더에 파일을 업로드합니다.
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

### -Force
이 cmdlet이 기존 Azure 저장소 파일을 덮어 사용 중임

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
이 cmdlet이 만들거나 업로드하는 **AzureStorageFile** 개체를 반환합니다.

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
파일 또는 폴더의 경로를 지정합니다.
이 cmdlet은 이 매개 변수가 지정하는 파일 또는 이 매개 변수가 지정한 폴더의 파일에 콘텐츠를 업로드합니다.
폴더를 지정하는 경우 이 cmdlet은 원본 파일과 이름이 같은 파일을 만듭니다.
존재하지 않는 파일의 경로를 지정하는 경우 이 cmdlet은 해당 파일을 만들고 해당 파일에 콘텐츠를 저장합니다.
이미 있는 파일을 지정하고 _Force_ 매개 변수를 지정하는 경우 이 cmdlet은 파일의 내용을 덮어써 덮어 써야 합니다.
이미 존재하는 파일을 지정하고 _Force를_ 지정하지 않으면 이 cmdlet은 변경하지 못하고 오류를 반환합니다.
존재하지 않는 폴더의 경로를 지정하는 경우 이 cmdlet은 변경하지 못하고 오류를 반환합니다.

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

### -공유
**CloudFileShare 개체를 지정합니다.**
이 cmdlet은 이 매개 변수를 지정하여 파일 공유의 파일에 업로드합니다.
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
이 cmdlet은 이 매개 변수를 지정하여 파일 공유의 파일에 업로드합니다.

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

### -Source
이 cmdlet이 업로드하는 원본 파일을 지정합니다.
존재하지 않는 파일을 지정하면 이 cmdlet에서 오류를 반환합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FullName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### System.String

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext

## 출력

### Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile

## 참고 사항

## 관련 링크

[Remove-AzStorageDirectory](./Remove-AzStorageDirectory.md)

[New-AzStorageDirectory](./New-AzStorageDirectory.md)

[Get-AzStorageFileContent](./Get-AzStorageFileContent.md)
