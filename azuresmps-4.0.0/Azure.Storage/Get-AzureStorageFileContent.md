---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: ''
schema: 2.0.0
ms.openlocfilehash: c945838d7d237fb37610d3763525b0ecac838fbb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93524028"
---
# Get-AzureStorageFileContent

## SYNOPSIS
파일의 내용을 다운로드 합니다.

## 구문과

### ShareName (기본값)
```
Get-AzureStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### 공유
```
Get-AzureStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### 디렉토리로
```
Get-AzureStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### 파일
```
Get-AzureStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## 설명은
**AzureStorageFileContent** cmdlet은 파일의 콘텐츠를 다운로드 한 다음 지정 된 대상에 저장 합니다.
이 cmdlet은 파일의 내용을 반환 하지 않습니다.

## 예제의

### 예제 1: 폴더에서 파일 다운로드
```
PS C:\>Get-AzureStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

이 명령은 파일 공유 ContosoShare06에서 현재 폴더로 ContosoWorkingFolder 폴더의 CurrentDataFile 파일을 다운로드 합니다.

## 변수

### -CheckMd5
존재 하지 않는 파일의 경로를 지정 하면이 cmdlet이 해당 파일을 만들고 새 파일에 내용을 저장 합니다.
이미 존재 하는 파일의 경로를 지정 하 고 *Force* 매개 변수를 지정 하면 cmdlet이 파일을 덮어씁니다.
기존 파일의 경로를 지정 하 고 *Force* 를 지정 하지 않으면 계속 하기 전에 cmdlet에서 메시지가 표시 됩니다.

폴더의 경로를 지정 하는 경우이 cmdlet은 Azure 저장소 파일의 이름을 가진 파일을 만들려고 시도 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClientTimeoutPerRequest
존재 하지 않는 파일의 경로를 지정 하면이 cmdlet이 해당 파일을 만들고 새 파일에 내용을 저장 합니다.
이미 존재 하는 파일의 경로를 지정 하 고 *Force* 매개 변수를 지정 하면 cmdlet이 파일을 덮어씁니다.
기존 파일의 경로를 지정 하 고 *Force* 를 지정 하지 않으면 계속 하기 전에 cmdlet에서 메시지가 표시 됩니다.

폴더의 경로를 지정 하는 경우이 cmdlet은 Azure 저장소 파일의 이름을 가진 파일을 만들려고 시도 합니다.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConcurrentTaskCount
존재 하지 않는 파일의 경로를 지정 하면이 cmdlet이 해당 파일을 만들고 새 파일에 내용을 저장 합니다.
이미 존재 하는 파일의 경로를 지정 하 고 *Force* 매개 변수를 지정 하면 cmdlet이 파일을 덮어씁니다.
기존 파일의 경로를 지정 하 고 *Force* 를 지정 하지 않으면 계속 하기 전에 cmdlet에서 메시지가 표시 됩니다.

폴더의 경로를 지정 하는 경우이 cmdlet은 Azure 저장소 파일의 이름을 가진 파일을 만들려고 시도 합니다.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -컨텍스트
존재 하지 않는 파일의 경로를 지정 하면이 cmdlet이 해당 파일을 만들고 새 파일에 내용을 저장 합니다.
이미 존재 하는 파일의 경로를 지정 하 고 *Force* 매개 변수를 지정 하면 cmdlet이 파일을 덮어씁니다.
기존 파일의 경로를 지정 하 고 *Force* 를 지정 하지 않으면 계속 하기 전에 cmdlet에서 메시지가 표시 됩니다.

폴더의 경로를 지정 하는 경우이 cmdlet은 Azure 저장소 파일의 이름을 가진 파일을 만들려고 시도 합니다.

```yaml
Type: IStorageContext
Parameter Sets: ShareName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -대상
대상 경로를 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 위치에 파일 콘텐츠를 다운로드 합니다.

존재 하지 않는 파일의 경로를 지정 하면이 cmdlet이 해당 파일을 만들고 새 파일에 내용을 저장 합니다.
이미 존재 하는 파일의 경로를 지정 하 고 *Force* 매개 변수를 지정 하면 cmdlet이 파일을 덮어씁니다.
기존 파일의 경로를 지정 하 고 *Force* 를 지정 하지 않으면 계속 하기 전에 cmdlet에서 메시지가 표시 됩니다.

폴더의 경로를 지정 하는 경우이 cmdlet은 Azure 저장소 파일의 이름을 가진 파일을 만들려고 시도 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -디렉터리
폴더를 **Cloudfiledirectory** 개체로 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 폴더의 파일에 대 한 콘텐츠를 가져옵니다.
디렉터리를 가져오려면 New-AzureStorageDirectory cmdlet을 사용 합니다.
또한 Get-AzureStorageFile cmdlet을 사용 하 여 디렉터리를 얻을 수 있습니다.

```yaml
Type: CloudFileDirectory
Parameter Sets: Directory
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -파일
파일을 **cloudfile** 개체로 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 파일을 가져옵니다.
**Cloudfile** 개체를 얻으려면 Get-AzureStorageFile cmdlet을 사용 합니다.

```yaml
Type: CloudFile
Parameter Sets: File
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Force
존재 하지 않는 파일의 경로를 지정 하면이 cmdlet이 해당 파일을 만들고 새 파일에 내용을 저장 합니다.
이미 존재 하는 파일의 경로를 지정 하 고 *Force* 매개 변수를 지정 하면 cmdlet이 파일을 덮어씁니다.
기존 파일의 경로를 지정 하 고 *Force* 를 지정 하지 않으면 계속 하기 전에 cmdlet에서 메시지가 표시 됩니다.

폴더의 경로를 지정 하는 경우이 cmdlet은 Azure 저장소 파일의 이름을 가진 파일을 만들려고 시도 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
존재 하지 않는 파일의 경로를 지정 하면이 cmdlet이 해당 파일을 만들고 새 파일에 내용을 저장 합니다.
이미 존재 하는 파일의 경로를 지정 하 고 *Force* 매개 변수를 지정 하면 cmdlet이 파일을 덮어씁니다.
기존 파일의 경로를 지정 하 고 *Force* 를 지정 하지 않으면 계속 하기 전에 cmdlet에서 메시지가 표시 됩니다.

폴더의 경로를 지정 하는 경우이 cmdlet은 Azure 저장소 파일의 이름을 가진 파일을 만들려고 시도 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
파일의 경로를 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 파일의 콘텐츠를 가져옵니다.
파일이 없는 경우이 cmdlet은 오류를 반환 합니다.

```yaml
Type: String
Parameter Sets: ShareName, Share, Directory
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
존재 하지 않는 파일의 경로를 지정 하면이 cmdlet이 해당 파일을 만들고 새 파일에 내용을 저장 합니다.
이미 존재 하는 파일의 경로를 지정 하 고 *Force* 매개 변수를 지정 하면 cmdlet이 파일을 덮어씁니다.
기존 파일의 경로를 지정 하 고 *Force* 를 지정 하지 않으면 계속 하기 전에 cmdlet에서 메시지가 표시 됩니다.

폴더의 경로를 지정 하는 경우이 cmdlet은 Azure 저장소 파일의 이름을 가진 파일을 만들려고 시도 합니다.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -공유
**Cloudfileshare** 되지 않는 개체를 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 공유에서 파일의 콘텐츠를 다운로드 합니다.
**Cloudfileshare** 되지 않는 개체를 가져오려면 Get-AzureStorageShare cmdlet을 사용 합니다.
이 개체는 저장소 컨텍스트를 포함 합니다.
이 매개 변수를 지정 하는 경우 *컨텍스트* 매개 변수를 지정 하지 마세요.

```yaml
Type: CloudFileShare
Parameter Sets: Share
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ShareName
파일 공유의 이름을 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 공유에서 파일의 콘텐츠를 다운로드 합니다.

```yaml
Type: String
Parameter Sets: ShareName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.
Cmdlet이 실행 되지 않습니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

## 상속자

## 관련 링크

[Get-AzureStorageFile](./Get-AzureStorageFile.md)

[Set-AzureStorageFileContent](./Set-AzureStorageFileContent.md)


