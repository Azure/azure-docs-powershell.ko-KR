---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 18E1AD70-42A6-47A2-A685-6E218B6DC4BE
online version: https://docs.microsoft.com/powershell/module/az.compute/save-azvhd
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVhd.md
ms.openlocfilehash: 4a88fe1e4bc18aaa31222b2f5d8e2a90629984d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972096"
---
# Save-AzVhd

## SYNOPSIS
다운로드한 .vhd 이미지를 로컬로 저장합니다.

## 구문

### ResourceGroupParameterSetName
```
Save-AzVhd [-ResourceGroupName] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfThreads] <Int32>] [-OverWrite] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### StorageKeyParameterSetName
```
Save-AzVhd [-StorageKey] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo> [[-NumberOfThreads] <Int32>]
 [-OverWrite] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Save-AzVhd** cmdlet은 .vhd 이미지를 Blob에서 파일에 저장합니다.
프로세스에서 사용하는 다운로더 스레드 수와 이미 존재하는 파일을 바꿀지 여부를 지정할 수 있습니다.
이 cmdlet은 콘텐츠를 현재와 같은 다운로드합니다.
VHD(Virtual Hard Disk) 형식 변환은 적용되지 않습니다.

## 예제

### 예제 1: 이미지 다운로드
```
PS C:\> Save-AzVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -ResourceGroupName "rgname"
```

이 명령은 .vhd 파일을 다운로드하고 로컬 경로 C:\vhd\Win7Image.vhd에 저장합니다.

### 예제 2: 이미지 다운로드 및 로컬 파일 덮어 사용
```
PS C:\> Save-AzVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite -ResourceGroupName "rgname"
```

이 명령은 .vhd 파일을 다운로드하고 로컬 경로에 저장합니다.
명령에는 *덮어 덮어 사용 매개 변수가* 포함됩니다.
따라서 C:\vhd\Win7Image.vhd가 이미 있는 경우 이 명령이 대체됩니다.

### 예제 3: 지정된 수의 스레드를 사용하여 이미지 다운로드
```
PS C:\> Save-AzVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32 -ResourceGroupName "rgname"
```

이 명령은 .vhd 파일을 다운로드하고 로컬 경로에 저장합니다.
명령은 *NumberOfThreads* 매개 변수에 대한 값을 32로 지정합니다.
따라서 cmdlet은 이 동작에 32개 스레드를 사용하게 됩니다.

### 예제 4: 이미지 다운로드 및 저장소 키 지정
```
PS C:\> Save-AzVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -StorageKey "zNvcH0r5vAGmC5AbwEtpcyWCMyBd3eMDbdaa4ua6kwxq6vTZH3Y+sw==" -ResourceGroupName "rgname"
```

이 명령은 .vhd 파일을 다운로드하고 저장소 키를 지정합니다.

## 매개 변수

### -AsJob
백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.

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

### -DefaultProfile
Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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

### -LocalFilePath
저장된 이미지의 로컬 파일 경로를 지정합니다.

```yaml
Type: System.IO.FileInfo
Parameter Sets: (All)
Aliases: lf

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NumberOfThreads
다운로드하는 동안 이 cmdlet에서 사용하는 다운로드 스레드 수를 지정합니다.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: th

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OverWrite
이 cmdlet이 있는 경우 *LocalFilePath* 파일에 의해 지정된 파일을 대체합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: o

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
저장소 계정의 리소스 그룹의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SourceUri
에서 Blob의 URI(균일한 리소스 식별자)를 `Azure` 지정합니다.

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: src, Source

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageKey
Blob Storage 계정의 저장소 키를 지정합니다.
키를 지정하지 않으면 이 cmdlet은 *Azure에서 SourceUri에서* 계정의 저장소 키를 확인하려고 시도합니다.

```yaml
Type: System.String
Parameter Sets: StorageKeyParameterSetName
Aliases: sk

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## 입력

### System.String

### System.Uri

## 출력

### Microsoft.Azure.Commands.Compute.Models.VhdDownloadContext

## 참고 사항

## 관련 링크

[Add-AzVhd](./Add-AzVhd.md)


