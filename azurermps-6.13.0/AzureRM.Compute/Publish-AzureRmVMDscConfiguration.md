---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: FB9ACBA2-081E-4876-A21A-F5BA11CBEDA2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/publish-azurermvmdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Publish-AzureRmVMDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Publish-AzureRmVMDscConfiguration.md
ms.openlocfilehash: 49dc91288c955de10c3dbcb84da74ffd3d71f140
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524543"
---
# Publish-AzureRmVMDscConfiguration

## SYNOPSIS
DSC 스크립트를 Azure blob storage에 업로드 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### UploadArchive (기본값)
```
Publish-AzureRmVMDscConfiguration [-ResourceGroupName] <String> [-ConfigurationPath] <String>
 [[-ContainerName] <String>] [-StorageAccountName] <String> [-StorageEndpointSuffix <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### CreateArchive
```
Publish-AzureRmVMDscConfiguration [-ConfigurationPath] <String> [[-OutputArchivePath] <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**AzureRmVMDscConfiguration** cmdlet은 Set-AzureRmVMDscExtension cmdlet을 사용 하 여 azure virtual machines에 적용할 수 있는 DSC (원하는 상태 구성) 스크립트를 azure blob storage에 업로드 합니다.

## 예제의

### 예제 1: .zip 패키지 만들기 Azure storage에 업로드
```
PS C:\> Publish-AzureRmVMDscConfiguration ".\MyConfiguration.ps1"
```

이 명령은 지정 된 스크립트와 종속 리소스 모듈에 대 한 .zip 패키지를 만들고 Azure storage에 업로드 합니다.

### 예제 2: .zip 패키지를 만들어 로컬 파일에 저장
```
PS C:\> Publish-AzureRmVMDscConfiguration ".\MyConfiguration.ps1" -OutputArchivePath ".\MyConfiguration.ps1.zip"
```

이 명령은 지정 된 스크립트와 종속 리소스 모듈에 대 한 .zip 패키지를 만들고 .\MyConfiguration.ps1.zip 라는 로컬 파일에 저장 합니다.

### 예제 3: 아카이브에 구성 추가 후 저장소에 업로드
```
PS C:\> Publish-AzureRmVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -SkipDependencyDetection
```

이 명령은 Sample.ps1 이라는 구성을 구성 보관 파일에 추가 하 여 Azure storage에 업로드 하 고 종속 리소스 모듈을 건너뜁니다.

### 예제 4: 보관에 구성 및 구성 데이터를 추가 하 고 저장소에 업로드
```
PS C:\> Publish-AzureRmVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -ConfigurationDataPath "C:\SampleData.psd1"
```

이 명령은 Azure storage에 업로드할 구성 보관 파일에 Sample.ps1 및 구성 데이터 (SampleData.psd1) 라는 구성을 추가 합니다.

### 예제 5: 보관에 구성, 구성 데이터 및 추가 콘텐츠를 추가한 다음 저장소에 업로드
```
PS C:\> Publish-AzureRmVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -AdditionalPath @("C:\ContentDir1", "C:\File.txt") -ConfigurationDataPath "C:\SampleData.psd1"
```

이 명령은 Sample.ps1 이라는 구성을 추가 하 고, 구성 데이터 SampleData.psd1을, 구성 아카이브에 대 한 추가 콘텐츠를 Azure storage에 업로드 합니다.

## 변수

### -AdditionalPath
구성 아카이브에 포함할 파일 또는 디렉토리의 경로를 지정 합니다.
구성과 함께 가상 컴퓨터에 다운로드 됩니다.

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
구성에 대 한 데이터를 지정 하는 psd1 파일의 경로를 지정 합니다.
이는 구성 아카이브에 추가 된 후 구성 기능으로 전달 됩니다.
Set-AzureRmVMDscExtension cmdlet을 통해 제공 되는 구성 데이터 경로에 의해 덮어쓰여집니다.

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
하나 이상의 구성을 포함 하는 파일의 경로를 지정 합니다.
파일은 Windows PowerShell 스크립트 (ps1) 파일 이거나 Windows PowerShell 모듈 (psm1) 파일 일 수 있습니다.

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
구성을 업로드할 Azure storage 컨테이너의 이름을 지정 합니다.

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

### -Force
사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.

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
구성 보관 파일을 작성 하는 데 대 한 로컬 .zip 파일의 경로를 지정 합니다.
이 매개 변수를 사용 하는 경우 구성 스크립트는 Azure blob storage에 업로드 되지 않습니다.

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
저장소 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.

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
이 cmdlet이 구성 보관에서 DSC 리소스 종속성을 제외 함을 나타냅니다.

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
구성 스크립트를 *ContainerName* 매개 변수에 지정 된 컨테이너에 업로드 하는 데 사용 되는 Azure 저장소 계정 이름을 지정 합니다.

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
저장소 끝점의 접미사를 지정 합니다.

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
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

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
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.
Cmdlet이 실행 되지 않습니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

### System.webserver []

## 출력

### System. 문자열

## 상속자

## 관련 링크

[Get-AzureRmVMDscExtension](./Get-AzureRmVMDscExtension.md)

[제거-AzureRmVMDscExtension](./Remove-AzureRmVMDscExtension.md)

[Set-AzureRmVMDscExtension](./Set-AzureRmVMDscExtension.md)


