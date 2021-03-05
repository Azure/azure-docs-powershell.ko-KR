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
# <span data-ttu-id="f20e2-101">Save-AzVhd</span><span class="sxs-lookup"><span data-stu-id="f20e2-101">Save-AzVhd</span></span>

## <span data-ttu-id="f20e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f20e2-102">SYNOPSIS</span></span>
<span data-ttu-id="f20e2-103">다운로드한 .vhd 이미지를 로컬로 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="f20e2-103">Saves downloaded .vhd images locally.</span></span>

## <span data-ttu-id="f20e2-104">구문</span><span class="sxs-lookup"><span data-stu-id="f20e2-104">SYNTAX</span></span>

### <span data-ttu-id="f20e2-105">ResourceGroupParameterSetName</span><span class="sxs-lookup"><span data-stu-id="f20e2-105">ResourceGroupParameterSetName</span></span>
```
Save-AzVhd [-ResourceGroupName] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfThreads] <Int32>] [-OverWrite] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f20e2-106">StorageKeyParameterSetName</span><span class="sxs-lookup"><span data-stu-id="f20e2-106">StorageKeyParameterSetName</span></span>
```
Save-AzVhd [-StorageKey] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo> [[-NumberOfThreads] <Int32>]
 [-OverWrite] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f20e2-107">설명</span><span class="sxs-lookup"><span data-stu-id="f20e2-107">DESCRIPTION</span></span>
<span data-ttu-id="f20e2-108">**Save-AzVhd** cmdlet은 .vhd 이미지를 Blob에서 파일에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="f20e2-108">The **Save-AzVhd** cmdlet saves .vhd images from a blob where they are stored to a file.</span></span>
<span data-ttu-id="f20e2-109">프로세스에서 사용하는 다운로더 스레드 수와 이미 존재하는 파일을 바꿀지 여부를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f20e2-109">You can specify the number of downloader threads that the process uses and whether to replace a file that already exists.</span></span>
<span data-ttu-id="f20e2-110">이 cmdlet은 콘텐츠를 현재와 같은 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="f20e2-110">This cmdlet downloads content as it is.</span></span>
<span data-ttu-id="f20e2-111">VHD(Virtual Hard Disk) 형식 변환은 적용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f20e2-111">It does not apply any Virtual Hard Disk (VHD) format conversion.</span></span>

## <span data-ttu-id="f20e2-112">예제</span><span class="sxs-lookup"><span data-stu-id="f20e2-112">EXAMPLES</span></span>

### <span data-ttu-id="f20e2-113">예제 1: 이미지 다운로드</span><span class="sxs-lookup"><span data-stu-id="f20e2-113">Example 1: Download an image</span></span>
```
PS C:\> Save-AzVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -ResourceGroupName "rgname"
```

<span data-ttu-id="f20e2-114">이 명령은 .vhd 파일을 다운로드하고 로컬 경로 C:\vhd\Win7Image.vhd에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="f20e2-114">This command downloads a .vhd file, and stores it in the local path C:\vhd\Win7Image.vhd.</span></span>

### <span data-ttu-id="f20e2-115">예제 2: 이미지 다운로드 및 로컬 파일 덮어 사용</span><span class="sxs-lookup"><span data-stu-id="f20e2-115">Example 2: Download an image and overwrite the local file</span></span>
```
PS C:\> Save-AzVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite -ResourceGroupName "rgname"
```

<span data-ttu-id="f20e2-116">이 명령은 .vhd 파일을 다운로드하고 로컬 경로에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="f20e2-116">This command downloads a .vhd file, and stores it in the local path.</span></span>
<span data-ttu-id="f20e2-117">명령에는 *덮어 덮어 사용 매개 변수가* 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="f20e2-117">The command includes the *Overwrite* parameter.</span></span>
<span data-ttu-id="f20e2-118">따라서 C:\vhd\Win7Image.vhd가 이미 있는 경우 이 명령이 대체됩니다.</span><span class="sxs-lookup"><span data-stu-id="f20e2-118">Therefore, if C:\vhd\Win7Image.vhd already exists, this command replaces it.</span></span>

### <span data-ttu-id="f20e2-119">예제 3: 지정된 수의 스레드를 사용하여 이미지 다운로드</span><span class="sxs-lookup"><span data-stu-id="f20e2-119">Example 3: Download an image by using a specified number of threads</span></span>
```
PS C:\> Save-AzVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32 -ResourceGroupName "rgname"
```

<span data-ttu-id="f20e2-120">이 명령은 .vhd 파일을 다운로드하고 로컬 경로에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="f20e2-120">This command downloads a .vhd file, and stores it in the local path.</span></span>
<span data-ttu-id="f20e2-121">명령은 *NumberOfThreads* 매개 변수에 대한 값을 32로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f20e2-121">The command specifies a value of 32 for the *NumberOfThreads* parameter.</span></span>
<span data-ttu-id="f20e2-122">따라서 cmdlet은 이 동작에 32개 스레드를 사용하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f20e2-122">Therefore, the cmdlet uses 32 threads for this action.</span></span>

### <span data-ttu-id="f20e2-123">예제 4: 이미지 다운로드 및 저장소 키 지정</span><span class="sxs-lookup"><span data-stu-id="f20e2-123">Example 4: Download an image and specify the storage key</span></span>
```
PS C:\> Save-AzVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -StorageKey "zNvcH0r5vAGmC5AbwEtpcyWCMyBd3eMDbdaa4ua6kwxq6vTZH3Y+sw==" -ResourceGroupName "rgname"
```

<span data-ttu-id="f20e2-124">이 명령은 .vhd 파일을 다운로드하고 저장소 키를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f20e2-124">This command downloads a .vhd file and specifies the storage key.</span></span>

## <span data-ttu-id="f20e2-125">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f20e2-125">PARAMETERS</span></span>

### <span data-ttu-id="f20e2-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f20e2-126">-AsJob</span></span>
<span data-ttu-id="f20e2-127">백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="f20e2-127">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="f20e2-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f20e2-128">-DefaultProfile</span></span>
<span data-ttu-id="f20e2-129">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f20e2-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f20e2-130">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="f20e2-130">-LocalFilePath</span></span>
<span data-ttu-id="f20e2-131">저장된 이미지의 로컬 파일 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f20e2-131">Specifies the local file path of the saved image.</span></span>

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

### <span data-ttu-id="f20e2-132">-NumberOfThreads</span><span class="sxs-lookup"><span data-stu-id="f20e2-132">-NumberOfThreads</span></span>
<span data-ttu-id="f20e2-133">다운로드하는 동안 이 cmdlet에서 사용하는 다운로드 스레드 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f20e2-133">Specifies the number of download threads that this cmdlet uses during download.</span></span>

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

### <span data-ttu-id="f20e2-134">-OverWrite</span><span class="sxs-lookup"><span data-stu-id="f20e2-134">-OverWrite</span></span>
<span data-ttu-id="f20e2-135">이 cmdlet이 있는 경우 *LocalFilePath* 파일에 의해 지정된 파일을 대체합니다.</span><span class="sxs-lookup"><span data-stu-id="f20e2-135">Indicates that this cmdlet replaces the file specified by *LocalFilePath* file if it exists.</span></span>

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

### <span data-ttu-id="f20e2-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f20e2-136">-ResourceGroupName</span></span>
<span data-ttu-id="f20e2-137">저장소 계정의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f20e2-137">Specifies the name of the resource group of the storage account.</span></span>

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

### <span data-ttu-id="f20e2-138">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="f20e2-138">-SourceUri</span></span>
<span data-ttu-id="f20e2-139">에서 Blob의 URI(균일한 리소스 식별자)를 `Azure` 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f20e2-139">Specifies the Uniform Resource Identifier (URI) of the blob in `Azure`.</span></span>

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

### <span data-ttu-id="f20e2-140">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="f20e2-140">-StorageKey</span></span>
<span data-ttu-id="f20e2-141">Blob Storage 계정의 저장소 키를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f20e2-141">Specifies the storage key of the blob storage account.</span></span>
<span data-ttu-id="f20e2-142">키를 지정하지 않으면 이 cmdlet은 *Azure에서 SourceUri에서* 계정의 저장소 키를 확인하려고 시도합니다.</span><span class="sxs-lookup"><span data-stu-id="f20e2-142">If you do not specify a key, this cmdlet attempts to determine the storage key of the account in *SourceUri* from Azure.</span></span>

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

### <span data-ttu-id="f20e2-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f20e2-143">CommonParameters</span></span>
<span data-ttu-id="f20e2-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f20e2-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f20e2-145">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f20e2-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f20e2-146">입력</span><span class="sxs-lookup"><span data-stu-id="f20e2-146">INPUTS</span></span>

### <span data-ttu-id="f20e2-147">System.String</span><span class="sxs-lookup"><span data-stu-id="f20e2-147">System.String</span></span>

### <span data-ttu-id="f20e2-148">System.Uri</span><span class="sxs-lookup"><span data-stu-id="f20e2-148">System.Uri</span></span>

## <span data-ttu-id="f20e2-149">출력</span><span class="sxs-lookup"><span data-stu-id="f20e2-149">OUTPUTS</span></span>

### <span data-ttu-id="f20e2-150">Microsoft.Azure.Commands.Compute.Models.VhdDownloadContext</span><span class="sxs-lookup"><span data-stu-id="f20e2-150">Microsoft.Azure.Commands.Compute.Models.VhdDownloadContext</span></span>

## <span data-ttu-id="f20e2-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f20e2-151">NOTES</span></span>

## <span data-ttu-id="f20e2-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f20e2-152">RELATED LINKS</span></span>

[<span data-ttu-id="f20e2-153">Add-AzVhd</span><span class="sxs-lookup"><span data-stu-id="f20e2-153">Add-AzVhd</span></span>](./Add-AzVhd.md)


