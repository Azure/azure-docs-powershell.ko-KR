---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: FB9ACBA2-081E-4876-A21A-F5BA11CBEDA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/publish-azvmdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Publish-AzVMDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Publish-AzVMDscConfiguration.md
ms.openlocfilehash: d099feea5efe52d8bcc6a0067550a7c4ae9bbc3a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876977"
---
# <span data-ttu-id="ed457-101">Publish-AzVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="ed457-101">Publish-AzVMDscConfiguration</span></span>

## <span data-ttu-id="ed457-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed457-102">SYNOPSIS</span></span>
<span data-ttu-id="ed457-103">DSC 스크립트를 Azure blob storage에 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed457-103">Uploads a DSC script to Azure blob storage.</span></span>

## <span data-ttu-id="ed457-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ed457-104">SYNTAX</span></span>

### <span data-ttu-id="ed457-105">UploadArchive (기본값)</span><span class="sxs-lookup"><span data-stu-id="ed457-105">UploadArchive (Default)</span></span>
```
Publish-AzVMDscConfiguration [-ResourceGroupName] <String> [-ConfigurationPath] <String>
 [[-ContainerName] <String>] [-StorageAccountName] <String> [-StorageEndpointSuffix <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed457-106">CreateArchive</span><span class="sxs-lookup"><span data-stu-id="ed457-106">CreateArchive</span></span>
```
Publish-AzVMDscConfiguration [-ConfigurationPath] <String> [[-OutputArchivePath] <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed457-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ed457-107">DESCRIPTION</span></span>
<span data-ttu-id="ed457-108">**AzVMDscConfiguration** cmdlet은 Set-AzVMDscExtension cmdlet을 사용 하 여 azure virtual machines에 적용할 수 있는 DSC (원하는 상태 구성) 스크립트를 azure blob storage에 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed457-108">The **Publish-AzVMDscConfiguration** cmdlet uploads a Desired State Configuration (DSC) script to Azure blob storage, which later can be applied to Azure virtual machines using the Set-AzVMDscExtension cmdlet.</span></span>

## <span data-ttu-id="ed457-109">예제의</span><span class="sxs-lookup"><span data-stu-id="ed457-109">EXAMPLES</span></span>

### <span data-ttu-id="ed457-110">예제 1: .zip 패키지 만들기 Azure storage에 업로드</span><span class="sxs-lookup"><span data-stu-id="ed457-110">Example 1: Create a .zip package an upload it to Azure storage</span></span>
```
PS C:\> Publish-AzVMDscConfiguration ".\MyConfiguration.ps1"
```

<span data-ttu-id="ed457-111">이 명령은 지정 된 스크립트와 종속 리소스 모듈에 대 한 .zip 패키지를 만들고 Azure storage에 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed457-111">This command creates a .zip package for the given script and any dependent resource modules and uploads it to Azure storage.</span></span>

### <span data-ttu-id="ed457-112">예제 2: .zip 패키지를 만들어 로컬 파일에 저장</span><span class="sxs-lookup"><span data-stu-id="ed457-112">Example 2: Create a .zip package and store it to a local file</span></span>
```
PS C:\> Publish-AzVMDscConfiguration ".\MyConfiguration.ps1" -OutputArchivePath ".\MyConfiguration.ps1.zip"
```

<span data-ttu-id="ed457-113">이 명령은 지정 된 스크립트와 종속 리소스 모듈에 대 한 .zip 패키지를 만들고 .\MyConfiguration.ps1.zip 라는 로컬 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed457-113">This command creates a .zip package for the given script and any dependent resource modules and stores it in the local file that is named .\MyConfiguration.ps1.zip.</span></span>

### <span data-ttu-id="ed457-114">예제 3: 아카이브에 구성 추가 후 저장소에 업로드</span><span class="sxs-lookup"><span data-stu-id="ed457-114">Example 3: Add configuration to the archive and then upload it to storage</span></span>
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -SkipDependencyDetection
```

<span data-ttu-id="ed457-115">이 명령은 Sample.ps1 이라는 구성을 구성 보관 파일에 추가 하 여 Azure storage에 업로드 하 고 종속 리소스 모듈을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="ed457-115">This command adds configuration named Sample.ps1 to the configuration archive to upload to Azure storage and skips dependent resource modules.</span></span>

### <span data-ttu-id="ed457-116">예제 4: 보관에 구성 및 구성 데이터를 추가 하 고 저장소에 업로드</span><span class="sxs-lookup"><span data-stu-id="ed457-116">Example 4: Add configuration and configuration data to the archive and then upload it to storage</span></span>
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -ConfigurationDataPath "C:\SampleData.psd1"
```

<span data-ttu-id="ed457-117">이 명령은 Azure storage에 업로드할 구성 보관 파일에 Sample.ps1 및 구성 데이터 (SampleData.psd1) 라는 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed457-117">This command adds configuration named Sample.ps1 and configuration data named SampleData.psd1 to the configuration archive to upload to Azure storage.</span></span>

### <span data-ttu-id="ed457-118">예제 5: 보관에 구성, 구성 데이터 및 추가 콘텐츠를 추가한 다음 저장소에 업로드</span><span class="sxs-lookup"><span data-stu-id="ed457-118">Example 5: Add configuration, configuration data, and additional content to the archive and then upload it to storage</span></span>
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -AdditionalPath @("C:\ContentDir1", "C:\File.txt") -ConfigurationDataPath "C:\SampleData.psd1"
```

<span data-ttu-id="ed457-119">이 명령은 Sample.ps1 이라는 구성을 추가 하 고, 구성 데이터 SampleData.psd1을, 구성 아카이브에 대 한 추가 콘텐츠를 Azure storage에 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed457-119">This command adds configuration named Sample.ps1, configuration data SampleData.psd1, and additional content to configuration archive to upload to Azure storage.</span></span>

## <span data-ttu-id="ed457-120">변수</span><span class="sxs-lookup"><span data-stu-id="ed457-120">PARAMETERS</span></span>

### <span data-ttu-id="ed457-121">-AdditionalPath</span><span class="sxs-lookup"><span data-stu-id="ed457-121">-AdditionalPath</span></span>
<span data-ttu-id="ed457-122">구성 아카이브에 포함할 파일 또는 디렉토리의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed457-122">Specifies the path of a file or a directory to include in the configuration archive.</span></span>
<span data-ttu-id="ed457-123">구성과 함께 가상 컴퓨터에 다운로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ed457-123">It gets downloaded to the virtual machine together with the configuration.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed457-124">-ConfigurationDataPath</span><span class="sxs-lookup"><span data-stu-id="ed457-124">-ConfigurationDataPath</span></span>
<span data-ttu-id="ed457-125">구성에 대 한 데이터를 지정 하는 psd1 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed457-125">Specifies the path of a .psd1 file that specifies the data for the configuration.</span></span>
<span data-ttu-id="ed457-126">이는 구성 아카이브에 추가 된 후 구성 기능으로 전달 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ed457-126">This is added to the configuration archive and then passed to the configuration function.</span></span>
<span data-ttu-id="ed457-127">Set-AzVMDscExtension cmdlet을 통해 제공 되는 구성 데이터 경로에 의해 덮어쓰여집니다.</span><span class="sxs-lookup"><span data-stu-id="ed457-127">It gets overwritten by the configuration data path provided through the Set-AzVMDscExtension cmdlet</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed457-128">-ConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="ed457-128">-ConfigurationPath</span></span>
<span data-ttu-id="ed457-129">하나 이상의 구성을 포함 하는 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed457-129">Specifies the path of a file that contains one or more configurations.</span></span>
<span data-ttu-id="ed457-130">파일은 Windows PowerShell 스크립트 (ps1) 파일 이거나 Windows PowerShell 모듈 (psm1) 파일 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ed457-130">The file can be a Windows PowerShell script (.ps1) file or a Windows PowerShell module (.psm1) file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed457-131">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="ed457-131">-ContainerName</span></span>
<span data-ttu-id="ed457-132">구성을 업로드할 Azure storage 컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed457-132">Specifies the name of the Azure storage container the configuration is uploaded to.</span></span>

```yaml
Type: String
Parameter Sets: UploadArchive
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed457-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed457-133">-DefaultProfile</span></span>
<span data-ttu-id="ed457-134">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ed457-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed457-135">-Force</span><span class="sxs-lookup"><span data-stu-id="ed457-135">-Force</span></span>
<span data-ttu-id="ed457-136">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed457-136">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ed457-137">-OutputArchivePath</span><span class="sxs-lookup"><span data-stu-id="ed457-137">-OutputArchivePath</span></span>
<span data-ttu-id="ed457-138">구성 보관 파일을 작성 하는 데 대 한 로컬 .zip 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed457-138">Specifies the path of a local .zip file to write the configuration archive to.</span></span>
<span data-ttu-id="ed457-139">이 매개 변수를 사용 하는 경우 구성 스크립트는 Azure blob storage에 업로드 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ed457-139">When this parameter is used, the configuration script is not uploaded to Azure blob storage.</span></span>

```yaml
Type: String
Parameter Sets: CreateArchive
Aliases: ConfigurationArchivePath

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed457-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed457-140">-ResourceGroupName</span></span>
<span data-ttu-id="ed457-141">저장소 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed457-141">Specifies the name of the resource group that contains the storage account.</span></span>

```yaml
Type: String
Parameter Sets: UploadArchive
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed457-142">-SkipDependencyDetection</span><span class="sxs-lookup"><span data-stu-id="ed457-142">-SkipDependencyDetection</span></span>
<span data-ttu-id="ed457-143">이 cmdlet이 구성 보관에서 DSC 리소스 종속성을 제외 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ed457-143">Indicates that this cmdlet excludes DSC resource dependencies from the configuration archive.</span></span>

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

### <span data-ttu-id="ed457-144">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ed457-144">-StorageAccountName</span></span>
<span data-ttu-id="ed457-145">구성 스크립트를 *ContainerName* 매개 변수에 지정 된 컨테이너에 업로드 하는 데 사용 되는 Azure 저장소 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed457-145">Specifies the Azure storage account name that is used to upload the configuration script to the container specified by the *ContainerName* parameter.</span></span>

```yaml
Type: String
Parameter Sets: UploadArchive
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed457-146">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="ed457-146">-StorageEndpointSuffix</span></span>
<span data-ttu-id="ed457-147">저장소 끝점의 접미사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed457-147">Specifies the suffix for the storage end point.</span></span>

```yaml
Type: String
Parameter Sets: UploadArchive
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed457-148">-확인</span><span class="sxs-lookup"><span data-stu-id="ed457-148">-Confirm</span></span>
<span data-ttu-id="ed457-149">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed457-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed457-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed457-150">-WhatIf</span></span>
<span data-ttu-id="ed457-151">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ed457-151">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="ed457-152">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ed457-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed457-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed457-153">CommonParameters</span></span>
<span data-ttu-id="ed457-154">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed457-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed457-155">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed457-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed457-156">입력</span><span class="sxs-lookup"><span data-stu-id="ed457-156">INPUTS</span></span>

### <span data-ttu-id="ed457-157">이름</span><span class="sxs-lookup"><span data-stu-id="ed457-157">String</span></span>
<span data-ttu-id="ed457-158">' ConfigurationPath ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed457-158">Parameter 'ConfigurationPath' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="ed457-159">출력</span><span class="sxs-lookup"><span data-stu-id="ed457-159">OUTPUTS</span></span>

### <span data-ttu-id="ed457-160">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ed457-160">System.String</span></span>

## <span data-ttu-id="ed457-161">상속자</span><span class="sxs-lookup"><span data-stu-id="ed457-161">NOTES</span></span>

## <span data-ttu-id="ed457-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ed457-162">RELATED LINKS</span></span>

[<span data-ttu-id="ed457-163">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="ed457-163">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="ed457-164">제거-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="ed457-164">Remove-AzVMDscExtension</span></span>](./Remove-AzVMDscExtension.md)

[<span data-ttu-id="ed457-165">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="ed457-165">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


