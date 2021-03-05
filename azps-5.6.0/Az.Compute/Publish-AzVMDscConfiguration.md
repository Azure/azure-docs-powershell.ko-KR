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
# <span data-ttu-id="90361-101">Publish-AzVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="90361-101">Publish-AzVMDscConfiguration</span></span>

## <span data-ttu-id="90361-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90361-102">SYNOPSIS</span></span>
<span data-ttu-id="90361-103">DSC 스크립트를 Azure Blob Storage에 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="90361-103">Uploads a DSC script to Azure blob storage.</span></span>

## <span data-ttu-id="90361-104">구문</span><span class="sxs-lookup"><span data-stu-id="90361-104">SYNTAX</span></span>

### <span data-ttu-id="90361-105">UploadArchive(기본값)</span><span class="sxs-lookup"><span data-stu-id="90361-105">UploadArchive (Default)</span></span>
```
Publish-AzVMDscConfiguration [-ResourceGroupName] <String> [-ConfigurationPath] <String>
 [[-ContainerName] <String>] [-StorageAccountName] <String> [-StorageEndpointSuffix <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90361-106">CreateArchive</span><span class="sxs-lookup"><span data-stu-id="90361-106">CreateArchive</span></span>
```
Publish-AzVMDscConfiguration [-ConfigurationPath] <String> [[-OutputArchivePath] <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90361-107">설명</span><span class="sxs-lookup"><span data-stu-id="90361-107">DESCRIPTION</span></span>
<span data-ttu-id="90361-108">**Publish-AzVMDscConfiguration** cmdlet은 DSC(원하는 상태 구성) 스크립트를 Azure Blob Storage에 업로드합니다. 이 스크립트는 나중에 Set-AzVMDscExtension cmdlet을 사용하여 Azure 가상 머신에 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90361-108">The **Publish-AzVMDscConfiguration** cmdlet uploads a Desired State Configuration (DSC) script to Azure blob storage, which later can be applied to Azure virtual machines using the Set-AzVMDscExtension cmdlet.</span></span>

## <span data-ttu-id="90361-109">예제</span><span class="sxs-lookup"><span data-stu-id="90361-109">EXAMPLES</span></span>

### <span data-ttu-id="90361-110">예제 1: .zip 패키지를 Azure Storage에 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="90361-110">Example 1: Create a .zip package an upload it to Azure storage</span></span>
```
PS C:\> Publish-AzVMDscConfiguration ".\MyConfiguration.ps1"
```

<span data-ttu-id="90361-111">이 명령은 주어진 스크립트 및 종속 리소스 모듈에 대한 .zip 패키지를 만들고 Azure Storage에 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="90361-111">This command creates a .zip package for the given script and any dependent resource modules and uploads it to Azure storage.</span></span>

### <span data-ttu-id="90361-112">예제 2: .zip 패키지 만들기 및 로컬 파일에 저장</span><span class="sxs-lookup"><span data-stu-id="90361-112">Example 2: Create a .zip package and store it to a local file</span></span>
```
PS C:\> Publish-AzVMDscConfiguration ".\MyConfiguration.ps1" -OutputArchivePath ".\MyConfiguration.ps1.zip"
```

<span data-ttu-id="90361-113">이 명령은 주어진 스크립트 및 종속 리소스 모듈에 대한 .zip 패키지를 만들고 해당 패키지를 로컬 파일로 저장하여 .\MyConfiguration.ps1.zip.</span><span class="sxs-lookup"><span data-stu-id="90361-113">This command creates a .zip package for the given script and any dependent resource modules and stores it in the local file that is named .\MyConfiguration.ps1.zip.</span></span>

### <span data-ttu-id="90361-114">예제 3: 보관에 구성을 추가한 다음 저장소에 업로드</span><span class="sxs-lookup"><span data-stu-id="90361-114">Example 3: Add configuration to the archive and then upload it to storage</span></span>
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -SkipDependencyDetection
```

<span data-ttu-id="90361-115">이 명령은 Sample.ps1 저장소에 업로드하기 위해 구성 보관소에 이라는 구성을 추가하고 종속 리소스 모듈을 건너뜁합니다.</span><span class="sxs-lookup"><span data-stu-id="90361-115">This command adds configuration named Sample.ps1 to the configuration archive to upload to Azure storage and skips dependent resource modules.</span></span>

### <span data-ttu-id="90361-116">예제 4: 구성 및 구성 데이터를 보관에 추가한 다음 저장소에 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="90361-116">Example 4: Add configuration and configuration data to the archive and then upload it to storage</span></span>
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -ConfigurationDataPath "C:\SampleData.psd1"
```

<span data-ttu-id="90361-117">이 명령은 Sample.ps1 1이라는 구성 및 SampleData.psd1이라는 구성을 구성 보관소에 추가하여 Azure Storage에 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="90361-117">This command adds configuration named Sample.ps1 and configuration data named SampleData.psd1 to the configuration archive to upload to Azure storage.</span></span>

### <span data-ttu-id="90361-118">예제 5: 보관에 구성, 구성 데이터 및 추가 콘텐츠를 추가한 다음 저장소에 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="90361-118">Example 5: Add configuration, configuration data, and additional content to the archive and then upload it to storage</span></span>
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -AdditionalPath @("C:\ContentDir1", "C:\File.txt") -ConfigurationDataPath "C:\SampleData.psd1"
```

<span data-ttu-id="90361-119">이 명령은 azure storage에 업로드할 Sample.ps1 구성, SampleData.psd1이라는 구성, 구성 보관소에 추가 콘텐츠를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="90361-119">This command adds configuration named Sample.ps1, configuration data SampleData.psd1, and additional content to configuration archive to upload to Azure storage.</span></span>

## <span data-ttu-id="90361-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="90361-120">PARAMETERS</span></span>

### <span data-ttu-id="90361-121">-AdditionalPath</span><span class="sxs-lookup"><span data-stu-id="90361-121">-AdditionalPath</span></span>
<span data-ttu-id="90361-122">구성 보관소에 포함할 파일 또는 디렉터리의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="90361-122">Specifies the path of a file or a directory to include in the configuration archive.</span></span>
<span data-ttu-id="90361-123">구성과 함께 가상 머신에 다운로드됩니다.</span><span class="sxs-lookup"><span data-stu-id="90361-123">It gets downloaded to the virtual machine together with the configuration.</span></span>

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

### <span data-ttu-id="90361-124">-ConfigurationDataPath</span><span class="sxs-lookup"><span data-stu-id="90361-124">-ConfigurationDataPath</span></span>
<span data-ttu-id="90361-125">구성에 대한 데이터를 지정하는 .psd1 파일의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="90361-125">Specifies the path of a .psd1 file that specifies the data for the configuration.</span></span>
<span data-ttu-id="90361-126">구성 보관소에 추가된 다음 구성 함수로 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="90361-126">This is added to the configuration archive and then passed to the configuration function.</span></span>
<span data-ttu-id="90361-127">Set-AzVMDscExtension cmdlet을 통해 제공된 구성 데이터 경로에 의해 Set-AzVMDscExtension 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90361-127">It gets overwritten by the configuration data path provided through the Set-AzVMDscExtension cmdlet</span></span>

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

### <span data-ttu-id="90361-128">-ConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="90361-128">-ConfigurationPath</span></span>
<span data-ttu-id="90361-129">하나 이상의 구성을 포함하는 파일의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="90361-129">Specifies the path of a file that contains one or more configurations.</span></span>
<span data-ttu-id="90361-130">파일은 Windows PowerShell 스크립트(.ps1) 파일 또는 Windows PowerShell 모듈(.psm1) 파일일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90361-130">The file can be a Windows PowerShell script (.ps1) file or a Windows PowerShell module (.psm1) file.</span></span>

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

### <span data-ttu-id="90361-131">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="90361-131">-ContainerName</span></span>
<span data-ttu-id="90361-132">구성이 업로드된 Azure Storage 컨테이너의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="90361-132">Specifies the name of the Azure storage container the configuration is uploaded to.</span></span>

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

### <span data-ttu-id="90361-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90361-133">-DefaultProfile</span></span>
<span data-ttu-id="90361-134">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="90361-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90361-135">-Force</span><span class="sxs-lookup"><span data-stu-id="90361-135">-Force</span></span>
<span data-ttu-id="90361-136">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="90361-136">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="90361-137">-OutputArchivePath</span><span class="sxs-lookup"><span data-stu-id="90361-137">-OutputArchivePath</span></span>
<span data-ttu-id="90361-138">구성 보관 파일을 작성할 로컬 .zip 파일의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="90361-138">Specifies the path of a local .zip file to write the configuration archive to.</span></span>
<span data-ttu-id="90361-139">이 매개 변수를 사용하는 경우 구성 스크립트가 Azure Blob Storage에 업로드되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="90361-139">When this parameter is used, the configuration script is not uploaded to Azure blob storage.</span></span>

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

### <span data-ttu-id="90361-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90361-140">-ResourceGroupName</span></span>
<span data-ttu-id="90361-141">저장소 계정을 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="90361-141">Specifies the name of the resource group that contains the storage account.</span></span>

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

### <span data-ttu-id="90361-142">-SkipDependencyDetection</span><span class="sxs-lookup"><span data-stu-id="90361-142">-SkipDependencyDetection</span></span>
<span data-ttu-id="90361-143">이 cmdlet은 구성 보관소에서 DSC 리소스 종속성 제외를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="90361-143">Indicates that this cmdlet excludes DSC resource dependencies from the configuration archive.</span></span>

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

### <span data-ttu-id="90361-144">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="90361-144">-StorageAccountName</span></span>
<span data-ttu-id="90361-145">*ContainerName* 매개 변수에서 지정한 컨테이너에 구성 스크립트를 업로드하는 데 사용되는 Azure Storage 계정 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="90361-145">Specifies the Azure storage account name that is used to upload the configuration script to the container specified by the *ContainerName* parameter.</span></span>

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

### <span data-ttu-id="90361-146">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="90361-146">-StorageEndpointSuffix</span></span>
<span data-ttu-id="90361-147">저장소 끝점에 대한 접미사를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="90361-147">Specifies the suffix for the storage end point.</span></span>

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

### <span data-ttu-id="90361-148">-확인</span><span class="sxs-lookup"><span data-stu-id="90361-148">-Confirm</span></span>
<span data-ttu-id="90361-149">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="90361-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90361-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90361-150">-WhatIf</span></span>
<span data-ttu-id="90361-151">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="90361-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90361-152">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="90361-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90361-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90361-153">CommonParameters</span></span>
<span data-ttu-id="90361-154">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="90361-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90361-155">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="90361-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90361-156">입력</span><span class="sxs-lookup"><span data-stu-id="90361-156">INPUTS</span></span>

### <span data-ttu-id="90361-157">System.String</span><span class="sxs-lookup"><span data-stu-id="90361-157">System.String</span></span>

### <span data-ttu-id="90361-158">System.String[]</span><span class="sxs-lookup"><span data-stu-id="90361-158">System.String[]</span></span>

## <span data-ttu-id="90361-159">출력</span><span class="sxs-lookup"><span data-stu-id="90361-159">OUTPUTS</span></span>

### <span data-ttu-id="90361-160">System.String</span><span class="sxs-lookup"><span data-stu-id="90361-160">System.String</span></span>

## <span data-ttu-id="90361-161">참고 사항</span><span class="sxs-lookup"><span data-stu-id="90361-161">NOTES</span></span>

## <span data-ttu-id="90361-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="90361-162">RELATED LINKS</span></span>

[<span data-ttu-id="90361-163">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="90361-163">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="90361-164">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="90361-164">Remove-AzVMDscExtension</span></span>](./Remove-AzVMDscExtension.md)

[<span data-ttu-id="90361-165">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="90361-165">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


