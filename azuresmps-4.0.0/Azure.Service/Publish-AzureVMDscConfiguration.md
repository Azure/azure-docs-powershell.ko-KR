---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 956B60BE-D978-4682-BA11-4EE9296B77B4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2d21d1b9609c160bdb2b4b3b8477a4b1b9bea991
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045882"
---
# <span data-ttu-id="ebeda-101">Publish-AzureVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="ebeda-101">Publish-AzureVMDscConfiguration</span></span>

## <span data-ttu-id="ebeda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ebeda-102">SYNOPSIS</span></span>
<span data-ttu-id="ebeda-103">Azure blob storage에 원하는 상태 구성 스크립트를 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebeda-103">Publishes a desired state configuration script to Azure blob storage.</span></span>

## <span data-ttu-id="ebeda-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ebeda-104">SYNTAX</span></span>

### <span data-ttu-id="ebeda-105">UploadArchive (기본값)</span><span class="sxs-lookup"><span data-stu-id="ebeda-105">UploadArchive (Default)</span></span>
```
Publish-AzureVMDscConfiguration [-ConfigurationPath] <String> [-ContainerName <String>] [-Force]
 [-StorageContext <AzureStorageContext>] [-StorageEndpointSuffix <String>] [-SkipDependencyDetection]
 [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>] [-PassThru] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ebeda-106">CreateArchive</span><span class="sxs-lookup"><span data-stu-id="ebeda-106">CreateArchive</span></span>
```
Publish-AzureVMDscConfiguration [-ConfigurationPath] <String> [-Force] [-ConfigurationArchivePath <String>]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>] [-PassThru]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ebeda-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ebeda-107">DESCRIPTION</span></span>
<span data-ttu-id="ebeda-108">**AzureVMDscConfiguration** Cmdlet은 **Set-AzureVMDscExtension** cmdlet을 사용 하 여 azure 가상 컴퓨터에 적용할 수 있는 azure blob 저장소에 원하는 상태 구성 스크립트를 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebeda-108">The **Publish-AzureVMDscConfiguration** cmdlet publishes a desired state configuration script to Azure blob storage, which later can be applied to Azure virtual machines using the **Set-AzureVMDscExtension** cmdlet.</span></span>

## <span data-ttu-id="ebeda-109">예제의</span><span class="sxs-lookup"><span data-stu-id="ebeda-109">EXAMPLES</span></span>

### <span data-ttu-id="ebeda-110">예제 1: 상태 구성 스크립트를 blob 저장소에 게시</span><span class="sxs-lookup"><span data-stu-id="ebeda-110">Example 1: Publish a state configuration script to blob storage</span></span>
```
PS C:\> Publish-AzureVMDscConfiguration .\MyConfiguration.ps1
```

<span data-ttu-id="ebeda-111">이 명령은 지정 된 스크립트와 종속 리소스 모듈에 대 한 .zip 패키지를 만들고 Azure storage에 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebeda-111">This command creates a .zip package for the given script and any dependent resource modules and uploads it to Azure storage.</span></span>

### <span data-ttu-id="ebeda-112">예제 2: 로컬 파일에 상태 구성 스크립트 게시</span><span class="sxs-lookup"><span data-stu-id="ebeda-112">Example 2: Publish a state configuration script to a local file</span></span>
```
PS C:\> Publish-AzureVMDscConfiguration .\MyConfiguration.ps1 -ConfigurationArchivePath .\MyConfiguration.ps1.zip
```

<span data-ttu-id="ebeda-113">이 명령은 지정 된 스크립트와 종속 리소스 모듈에 대 한 .zip 패키지를 만들고 로컬 파일 .\MyConfiguration.ps1.zip에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebeda-113">This command creates a .zip package for the given script and any dependent resource modules and stores it in the local file .\MyConfiguration.ps1.zip.</span></span>

## <span data-ttu-id="ebeda-114">변수</span><span class="sxs-lookup"><span data-stu-id="ebeda-114">PARAMETERS</span></span>

### <span data-ttu-id="ebeda-115">-AdditionalPath</span><span class="sxs-lookup"><span data-stu-id="ebeda-115">-AdditionalPath</span></span>
<span data-ttu-id="ebeda-116">추가 경로의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebeda-116">Specifies an array of additional paths.</span></span>

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

### <span data-ttu-id="ebeda-117">-ConfigurationArchivePath</span><span class="sxs-lookup"><span data-stu-id="ebeda-117">-ConfigurationArchivePath</span></span>
<span data-ttu-id="ebeda-118">이 cmdlet가 구성 보관 함을 기록 하는 로컬 .zip 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebeda-118">Specifies the path of a local .zip file that this cmdlet writes the configuration archive.</span></span>
<span data-ttu-id="ebeda-119">이 매개 변수를 사용 하는 경우 구성 스크립트는 Azure blob storage에 업로드 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ebeda-119">The configuration script is not uploaded to Azure blob storage if you use this parameter.</span></span>

```yaml
Type: String
Parameter Sets: CreateArchive
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebeda-120">-ConfigurationDataPath</span><span class="sxs-lookup"><span data-stu-id="ebeda-120">-ConfigurationDataPath</span></span>
<span data-ttu-id="ebeda-121">구성 데이터 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebeda-121">Specifies a configuration data path.</span></span>

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

### <span data-ttu-id="ebeda-122">-ConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="ebeda-122">-ConfigurationPath</span></span>
<span data-ttu-id="ebeda-123">하나 이상의 구성을 포함 하는 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebeda-123">Specifies the path of a file that contains one or more configurations.</span></span>
<span data-ttu-id="ebeda-124">파일은 Windows PowerShell 스크립트 (ps1 파일), 모듈 (psm1 파일) 또는 각 모듈을 별도의 디렉터리에 있는 Windows PowerShell 모듈 집합을 포함 하는 보관 (.zip 파일) 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ebeda-124">The file can be a Windows PowerShell script (.ps1 file), module (.psm1 file), or an archive (.zip file) that contains a set of Windows PowerShell modules, with each module in a separate directory.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ebeda-125">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="ebeda-125">-ContainerName</span></span>
<span data-ttu-id="ebeda-126">구성을 업로드할 Azure storage 컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebeda-126">Specifies the name of the Azure storage container the configuration is uploaded to.</span></span>

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

### <span data-ttu-id="ebeda-127">-Force</span><span class="sxs-lookup"><span data-stu-id="ebeda-127">-Force</span></span>
<span data-ttu-id="ebeda-128">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebeda-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ebeda-129">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ebeda-129">-InformationAction</span></span>
<span data-ttu-id="ebeda-130">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebeda-130">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ebeda-131">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ebeda-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ebeda-132">하기로</span><span class="sxs-lookup"><span data-stu-id="ebeda-132">Continue</span></span>
- <span data-ttu-id="ebeda-133">숨기기</span><span class="sxs-lookup"><span data-stu-id="ebeda-133">Ignore</span></span>
- <span data-ttu-id="ebeda-134">Inquire</span><span class="sxs-lookup"><span data-stu-id="ebeda-134">Inquire</span></span>
- <span data-ttu-id="ebeda-135">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ebeda-135">SilentlyContinue</span></span>
- <span data-ttu-id="ebeda-136">중지가</span><span class="sxs-lookup"><span data-stu-id="ebeda-136">Stop</span></span>
- <span data-ttu-id="ebeda-137">대기</span><span class="sxs-lookup"><span data-stu-id="ebeda-137">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebeda-138">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ebeda-138">-InformationVariable</span></span>
<span data-ttu-id="ebeda-139">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebeda-139">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebeda-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ebeda-140">-PassThru</span></span>
<span data-ttu-id="ebeda-141">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebeda-141">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ebeda-142">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ebeda-142">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ebeda-143">-프로필</span><span class="sxs-lookup"><span data-stu-id="ebeda-143">-Profile</span></span>
<span data-ttu-id="ebeda-144">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebeda-144">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ebeda-145">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="ebeda-145">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebeda-146">-SkipDependencyDetection</span><span class="sxs-lookup"><span data-stu-id="ebeda-146">-SkipDependencyDetection</span></span>
<span data-ttu-id="ebeda-147">이 cmdlet이 종속성 검색을 생략 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ebeda-147">Indicates that this cmdlet skips dependency detection.</span></span>

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

### <span data-ttu-id="ebeda-148">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="ebeda-148">-StorageContext</span></span>
<span data-ttu-id="ebeda-149">구성 스크립트를 *ContainerName* 매개 변수에 지정 된 컨테이너에 업로드 하는 데 사용 되는 보안 설정을 제공 하는 Azure storage 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebeda-149">Specifies the Azure storage context that provides the security settings used to upload the configuration script to the container specified by the *ContainerName* parameter.</span></span>
<span data-ttu-id="ebeda-150">이 컨텍스트는 컨테이너에 대 한 쓰기 액세스를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebeda-150">This context provides write access to the container.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: UploadArchive
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebeda-151">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="ebeda-151">-StorageEndpointSuffix</span></span>
<span data-ttu-id="ebeda-152">저장소 끝점의 접미사를 지정 합니다 (예 core.contoso.net).</span><span class="sxs-lookup"><span data-stu-id="ebeda-152">Specifies the suffix for the storage end-point, for instance, core.contoso.net</span></span>

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

### <span data-ttu-id="ebeda-153">-확인</span><span class="sxs-lookup"><span data-stu-id="ebeda-153">-Confirm</span></span>
<span data-ttu-id="ebeda-154">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebeda-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebeda-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebeda-155">-WhatIf</span></span>
<span data-ttu-id="ebeda-156">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ebeda-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ebeda-157">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ebeda-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ebeda-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebeda-158">CommonParameters</span></span>
<span data-ttu-id="ebeda-159">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebeda-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebeda-160">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebeda-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebeda-161">입력</span><span class="sxs-lookup"><span data-stu-id="ebeda-161">INPUTS</span></span>

## <span data-ttu-id="ebeda-162">출력</span><span class="sxs-lookup"><span data-stu-id="ebeda-162">OUTPUTS</span></span>

## <span data-ttu-id="ebeda-163">상속자</span><span class="sxs-lookup"><span data-stu-id="ebeda-163">NOTES</span></span>

## <span data-ttu-id="ebeda-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ebeda-164">RELATED LINKS</span></span>

[<span data-ttu-id="ebeda-165">Set-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="ebeda-165">Set-AzureVMDscExtension</span></span>](./Set-AzureVMDscExtension.md)


