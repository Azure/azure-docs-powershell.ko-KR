---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: FB9ACBA2-081E-4876-A21A-F5BA11CBEDA2
online version: https://docs.microsoft.com/powershell/module/az.compute/publish-azvmdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Publish-AzVMDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Publish-AzVMDscConfiguration.md
ms.openlocfilehash: a57ed6bb12a1357ebd8d9b4f090bd1d551f3c554
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988395"
---
# Publish-AzVMDscConfiguration

## SYNOPSIS
DSC 스크립트를 Azure Blob Storage에 업로드합니다.

## 구문

### UploadArchive(기본값)
```
Publish-AzVMDscConfiguration [-ResourceGroupName] <String> [-ConfigurationPath] <String>
 [[-ContainerName] <String>] [-StorageAccountName] <String> [-StorageEndpointSuffix <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### CreateArchive
```
Publish-AzVMDscConfiguration [-ConfigurationPath] <String> [[-OutputArchivePath] <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명
**Publish-AzVMDscConfiguration** cmdlet은 DSC(원하는 상태 구성) 스크립트를 Azure Blob Storage에 업로드합니다. 이 스크립트는 나중에 Set-AzVMDscExtension cmdlet을 사용하여 Azure 가상 머신에 적용할 수 있습니다.

## 예제

### 예제 1: .zip 패키지를 Azure Storage에 업로드합니다.
```
PS C:\> Publish-AzVMDscConfiguration ".\MyConfiguration.ps1"
```

이 명령은 주어진 스크립트 및 종속 리소스 모듈에 대한 .zip 패키지를 만들고 Azure Storage에 업로드합니다.

### 예제 2: .zip 패키지 만들기 및 로컬 파일에 저장
```
PS C:\> Publish-AzVMDscConfiguration ".\MyConfiguration.ps1" -OutputArchivePath ".\MyConfiguration.ps1.zip"
```

이 명령은 주어진 스크립트 및 종속 리소스 모듈에 대한 .zip 패키지를 만들고 해당 패키지를 로컬 파일로 저장하여 .\MyConfiguration.ps1.zip.

### 예제 3: 보관에 구성을 추가한 다음 저장소에 업로드
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -SkipDependencyDetection
```

이 명령은 Sample.ps1 저장소에 업로드하기 위해 구성 보관소에 이라는 구성을 추가하고 종속 리소스 모듈을 건너뜁합니다.

### 예제 4: 구성 및 구성 데이터를 보관에 추가한 다음 저장소에 업로드합니다.
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -ConfigurationDataPath "C:\SampleData.psd1"
```

이 명령은 Sample.ps1 1이라는 구성 및 SampleData.psd1이라는 구성을 구성 보관소에 추가하여 Azure Storage에 업로드합니다.

### 예제 5: 보관에 구성, 구성 데이터 및 추가 콘텐츠를 추가한 다음 저장소에 업로드합니다.
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -AdditionalPath @("C:\ContentDir1", "C:\File.txt") -ConfigurationDataPath "C:\SampleData.psd1"
```

이 명령은 azure storage에 업로드할 Sample.ps1 구성, SampleData.psd1이라는 구성, 구성 보관소에 추가 콘텐츠를 추가합니다.

## 매개 변수

### -AdditionalPath
구성 보관소에 포함할 파일 또는 디렉터리의 경로를 지정합니다.
구성과 함께 가상 머신에 다운로드됩니다.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConfigurationDataPath
구성에 대한 데이터를 지정하는 .psd1 파일의 경로를 지정합니다.
구성 보관소에 추가된 다음 구성 함수로 전달됩니다.
Set-AzVMDscExtension cmdlet을 통해 제공된 구성 데이터 경로에 의해 Set-AzVMDscExtension 됩니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConfigurationPath
하나 이상의 구성을 포함하는 파일의 경로를 지정합니다.
파일은 Windows PowerShell 스크립트(.ps1) 파일 또는 Windows PowerShell 모듈(.psm1) 파일일 수 있습니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ContainerName
구성이 업로드된 Azure Storage 컨테이너의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -Force
사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.

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

### -OutputArchivePath
구성 보관 파일을 작성할 로컬 .zip 파일의 경로를 지정합니다.
이 매개 변수를 사용하는 경우 구성 스크립트가 Azure Blob Storage에 업로드되지 않습니다.

```yaml
Type: System.String
Parameter Sets: CreateArchive
Aliases: ConfigurationArchivePath

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
저장소 계정을 포함하는 리소스 그룹의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SkipDependencyDetection
이 cmdlet은 구성 보관소에서 DSC 리소스 종속성 제외를 나타냅니다.

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

### -StorageAccountName
*ContainerName* 매개 변수에서 지정한 컨테이너에 구성 스크립트를 업로드하는 데 사용되는 Azure Storage 계정 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageEndpointSuffix
저장소 끝점에 대한 접미사를 지정합니다.

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -확인
cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.

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
cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.
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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## 입력

### System.String

### System.String[]

## 출력

### System.String

## 참고 사항

## 관련 링크

[Get-AzVMDscExtension](./Get-AzVMDscExtension.md)

[Remove-AzVMDscExtension](./Remove-AzVMDscExtension.md)

[Set-AzVMDscExtension](./Set-AzVMDscExtension.md)


