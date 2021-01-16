---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: FB9ACBA2-081E-4876-A21A-F5BA11CBEDA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/publish-azvmdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Publish-AzVMDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Publish-AzVMDscConfiguration.md
ms.openlocfilehash: 94dac11a3c26adaac93b4e36c2dda3df513d4076
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330129"
---
# Publish-AzVMDscConfiguration

## SYNOPSIS
Azure Blob Storage에 DSC 스크립트를 업로드합니다.

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
**Publish-AzVMDscConfiguration** cmdlet은 DSC(필요한 상태 구성) 스크립트를 Azure Blob Storage에 업로드합니다. 나중에 Set-AzVMDscExtension cmdlet을 사용하여 Azure 가상 머신에 적용할 수 있습니다.

## 예제

### 예제 1: Azure Storage에 업로드하는 .zip 패키지 만들기
```
PS C:\> Publish-AzVMDscConfiguration ".\MyConfiguration.ps1"
```

이 명령은 주어진 스크립트 및 종속 리소스 모듈에 대한 .zip 패키지를 만들고 Azure Storage에 업로드합니다.

### 예제 2: .zip 패키지 만들기 및 로컬 파일에 저장
```
PS C:\> Publish-AzVMDscConfiguration ".\MyConfiguration.ps1" -OutputArchivePath ".\MyConfiguration.ps1.zip"
```

이 명령은 지정한 스크립트 및 종속 리소스 모듈에 대한 .zip 패키지를 만들고 해당 모듈의 이름이 지정되는 로컬 파일에 .\MyConfiguration.ps1.zip.

### 예제 3: 보관에 구성을 추가한 다음 저장소에 업로드
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -SkipDependencyDetection
```

이 명령은 Azure 저장소에 Sample.ps1 업로드하기 위해 구성 보관함으로 이름이 지정되는 구성을 추가하고 종속 리소스 모듈을 건너뜁습니다.

### 예제 4: 보관에 구성 및 구성 데이터를 추가한 다음 저장소에 업로드
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -ConfigurationDataPath "C:\SampleData.psd1"
```

이 명령은 azure Sample.ps1 업로드할 SampleData.psd1이라는 이름의 구성 및 구성 데이터를 구성 보관에 추가합니다.

### 예제 5: 구성, 구성 데이터 및 추가 콘텐츠를 보관에 추가한 다음 저장소에 업로드
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -AdditionalPath @("C:\ContentDir1", "C:\File.txt") -ConfigurationDataPath "C:\SampleData.psd1"
```

이 명령은 azure storage에 업로드할 Sample.ps1 구성 데이터 SampleData.psd1로 명명된 구성 및 추가 콘텐츠를 구성 보관에 추가합니다.

## PARAMETERS

### -AdditionalPath
구성 보관 파일에 포함할 파일 또는 디렉터리의 경로를 지정합니다.
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
이 기능은 구성 보관에 추가된 다음 구성 함수에 전달됩니다.
Set-AzVMDscExtension cmdlet을 통해 제공되는 구성 데이터 경로에 의해 덮어됩니다.

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
하나 이상의 구성이 포함된 파일의 경로를 지정합니다.
이 파일은 Windows PowerShell 스크립트(.ps1) 파일 또는 Windows PowerShell 모듈(.psm1) 파일일 수 있습니다.

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
구성이 업로드된 Azure 저장소 컨테이너의 이름을 지정합니다.

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
구성 보관 파일을 쓸 로컬 .zip 파일의 경로를 지정합니다.
이 매개 변수를 사용하면 구성 스크립트가 Azure Blob Storage에 업로드되지 않습니다.

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
이 cmdlet이 구성 보관 파일에서 DSC 리소스 종속성 제외를 나타냅니다.

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
*ContainerName* 매개 변수로 지정된 컨테이너에 구성 스크립트를 업로드하는 데 사용되는 Azure Storage 계정 이름을 지정합니다.

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

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


