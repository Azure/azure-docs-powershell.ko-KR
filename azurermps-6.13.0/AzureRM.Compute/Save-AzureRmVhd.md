---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 18E1AD70-42A6-47A2-A685-6E218B6DC4BE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/save-azurermvhd
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Save-AzureRmVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Save-AzureRmVhd.md
ms.openlocfilehash: db2148be139130f5963214c5e66809a3e66a22ed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532076"
---
# Save-AzureRmVhd

## SYNOPSIS
다운로드 한 .vhd 이미지를 로컬에 저장 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### ResourceGroupParameterSetName
```
Save-AzureRmVhd [-ResourceGroupName] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfThreads] <Int32>] [-OverWrite] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### StorageKeyParameterSetName
```
Save-AzureRmVhd [-StorageKey] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfThreads] <Int32>] [-OverWrite] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
**AzureRmVhd** cmdlet은 파일에 저장 된 blob에서 .vhd 이미지를 저장 합니다.
프로세스에 사용 되는 다운로더 스레드 수와 기존 파일의 대체 여부를 지정할 수 있습니다.
이 cmdlet은 콘텐츠가 있는 그대로 다운로드 합니다.
VHD (가상 하드 디스크) 형식 변환은 적용 되지 않습니다.

## 예제의

### 예제 1: 이미지 다운로드
```
PS C:\> Save-AzureRmVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -ResourceGroupName "rgname"
```

이 명령은 .vhd 파일을 다운로드 하 여 로컬 경로 C:\vhd\Win7Image.vhd.에 저장 합니다.

### 예제 2: 이미지 다운로드 및 로컬 파일 덮어쓰기
```
PS C:\> Save-AzureRmVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite -ResourceGroupName "rgname"
```

이 명령은 .vhd 파일을 다운로드 하 여 로컬 경로에 저장 합니다.
명령에 *Overwrite* 매개 변수가 포함 됩니다.
따라서 C:\vhd\Win7Image.vhd 이미 있는 경우이 명령은 해당 명령을 바꿉니다.

### 예제 3: 지정 된 수의 스레드를 사용 하 여 이미지 다운로드
```
PS C:\> Save-AzureRmVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32 -ResourceGroupName "rgname"
```

이 명령은 .vhd 파일을 다운로드 하 여 로컬 경로에 저장 합니다.
명령이 *Numberofthreads* 매개 변수에 대 한 32 값을 지정 합니다.
따라서 cmdlet은이 작업을 위해 32 스레드를 사용 합니다.

### 예제 4: 이미지 다운로드 및 저장소 키 지정
```
PS C:\> Save-AzureRmVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -StorageKey "zNvcH0r5vAGmC5AbwEtpcyWCMyBd3eMDbdaa4ua6kwxq6vTZH3Y+sw==" -ResourceGroupName "rgname"
```

이 명령은 .vhd 파일을 다운로드 하 고 저장소 키를 지정 합니다.

## 변수

### -AsJob
백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.

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
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LocalFilePath
저장 된 이미지의 로컬 파일 경로를 지정 합니다.

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
이 cmdlet에서 다운로드 하는 동안 사용 하는 다운로드 스레드 수를 지정 합니다.

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
이 cmdlet이 존재 하는 *LocalFilePath* 파일이 지정 된 파일을 대체 함을 나타냅니다.

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
저장소 계정의 리소스 그룹 이름을 지정 합니다.

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
에서 blob의 URI (Uniform Resource Identifier)를 지정 합니다 `Azure` .

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
Blob 저장소 계정의 저장소 키를 지정 합니다.
키를 지정 하지 않으면이 cmdlet은 Azure에서 *Sourceuri* 의 계정에 대 한 저장소 키를 확인 하려고 합니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

### 시스템 Uri

## 출력

### VhdDownloadContext를 계산 합니다.

## 상속자

## 관련 링크

[추가-AzureRmVhd](./Add-AzureRMVhd.md)


