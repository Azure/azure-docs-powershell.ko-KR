---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D08DAA8B-B7BF-4167-AB16-F2723985A0B7
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvhd
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVhd.md
ms.openlocfilehash: 6e86ed8cde1297af54ffaf8f8c8fbc912da30e69
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981072"
---
# <span data-ttu-id="848e1-101">Add-AzVhd</span><span class="sxs-lookup"><span data-stu-id="848e1-101">Add-AzVhd</span></span>

## <span data-ttu-id="848e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="848e1-102">SYNOPSIS</span></span>
<span data-ttu-id="848e1-103">Azure의 클라우드 저장소 계정의 Blob에 온라인 가상 머신에서 가상 하드 디스크를 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="848e1-103">Uploads a virtual hard disk from an on-premises virtual machine to a blob in a cloud storage account in Azure.</span></span>

## <span data-ttu-id="848e1-104">구문</span><span class="sxs-lookup"><span data-stu-id="848e1-104">SYNTAX</span></span>

```
Add-AzVhd [[-ResourceGroupName] <String>] [-Destination] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfUploaderThreads] <Int32>] [[-BaseImageUriToPatch] <Uri>] [-OverWrite] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="848e1-105">설명</span><span class="sxs-lookup"><span data-stu-id="848e1-105">DESCRIPTION</span></span>
<span data-ttu-id="848e1-106">**Add-AzVhd** cmdlet은 .vhd 파일 형식으로 프레미스 가상 하드 디스크를 고정된 가상 하드 디스크로 Blob Storage 계정에 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="848e1-106">The **Add-AzVhd** cmdlet uploads on-premises virtual hard disks, in .vhd file format, to a blob storage account as fixed virtual hard disks.</span></span>
<span data-ttu-id="848e1-107">사용할 업로더 스레드 수를 구성하거나 지정된 대상 URI에서 기존 Blob을 덮어 덮을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="848e1-107">You can configure the number of uploader threads that will be used or overwrite an existing blob in the specified destination URI.</span></span>
<span data-ttu-id="848e1-108">또한 지원되는 것은 패치된 버전의 On-Premises .vhd 파일을 업로드하는 능력입니다.</span><span class="sxs-lookup"><span data-stu-id="848e1-108">Also supported is the ability to upload a patched version of an on-premises .vhd file.</span></span>
<span data-ttu-id="848e1-109">기본 가상 하드 디스크가 이미 업로드된 경우 기본 이미지를 부모로 사용하는 다른 디스크를 업로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="848e1-109">When a base virtual hard disk has already been uploaded, you can upload differencing disks that use the base image as the parent.</span></span>
<span data-ttu-id="848e1-110">SAS(공유 액세스 서명) URI도 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="848e1-110">Shared access signature (SAS) URI is supported also.</span></span>

## <span data-ttu-id="848e1-111">예제</span><span class="sxs-lookup"><span data-stu-id="848e1-111">EXAMPLES</span></span>

### <span data-ttu-id="848e1-112">예제 1: VHD 파일 추가</span><span class="sxs-lookup"><span data-stu-id="848e1-112">Example 1: Add a VHD file</span></span>
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

<span data-ttu-id="848e1-113">이 명령은 저장소 계정에 .vhd 파일을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="848e1-113">This command adds a .vhd file to a storage account.</span></span>

### <span data-ttu-id="848e1-114">예제 2: VHD 파일 추가 및 대상 덮어 사용</span><span class="sxs-lookup"><span data-stu-id="848e1-114">Example 2: Add a VHD file and overwrite the destination</span></span>
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

<span data-ttu-id="848e1-115">이 명령은 저장소 계정에 .vhd 파일을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="848e1-115">This command adds a .vhd file to a storage account.</span></span>
<span data-ttu-id="848e1-116">명령은 기존 파일을 덮어 덮어 덮어 니다.</span><span class="sxs-lookup"><span data-stu-id="848e1-116">The command overwrites an existing file.</span></span>

### <span data-ttu-id="848e1-117">예제 3: VHD 파일 추가 및 스레드 수 지정</span><span class="sxs-lookup"><span data-stu-id="848e1-117">Example 3: Add a VHD file and specify the number of threads</span></span>
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfUploaderThreads 32
```

<span data-ttu-id="848e1-118">이 명령은 저장소 계정에 .vhd 파일을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="848e1-118">This command adds a .vhd file to a storage account.</span></span>
<span data-ttu-id="848e1-119">명령은 파일을 업로드하는 데 사용할 스레드 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="848e1-119">The command specifies the number of threads to use to upload the file.</span></span>

### <span data-ttu-id="848e1-120">예제 4: VHD 파일 추가 및 SAS URI 지정</span><span class="sxs-lookup"><span data-stu-id="848e1-120">Example 4: Add a VHD file and specify the SAS URI</span></span>
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd?st=2013-01 -09T22%3A15%3A49Z&amp;se=2013-01-09T23%3A10%3A49Z&amp;sr=b&amp;sp=w&amp;sig=13T9Ow%2FRJAMmhfO%2FaP3HhKKJ6AY093SmveO SIV4%2FR7w%3D" -LocalFilePath "C:\vhd\win7baseimage.vhd"
```

<span data-ttu-id="848e1-121">이 명령은 저장소 계정에 .vhd 파일을 추가하고 SAS URI를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="848e1-121">This command adds a .vhd file to a storage account and specifies the SAS URI.</span></span>

## <span data-ttu-id="848e1-122">매개 변수</span><span class="sxs-lookup"><span data-stu-id="848e1-122">PARAMETERS</span></span>

### <span data-ttu-id="848e1-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="848e1-123">-AsJob</span></span>
<span data-ttu-id="848e1-124">백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="848e1-124">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="848e1-125">-BaseImageUriToPatch</span><span class="sxs-lookup"><span data-stu-id="848e1-125">-BaseImageUriToPatch</span></span>
<span data-ttu-id="848e1-126">Azure Blob Storage의 기본 이미지 Blob에 URI를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="848e1-126">Specifies the URI to a base image blob in Azure Blob Storage.</span></span>
<span data-ttu-id="848e1-127">SAS를 이 매개 변수의 값으로 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="848e1-127">An SAS can be specified as the value for this parameter.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: bs

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="848e1-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="848e1-128">-DefaultProfile</span></span>
<span data-ttu-id="848e1-129">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="848e1-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="848e1-130">-대상</span><span class="sxs-lookup"><span data-stu-id="848e1-130">-Destination</span></span>
<span data-ttu-id="848e1-131">Blob Storage에서 Blob의 URI를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="848e1-131">Specifies the URI of a blob in Blob Storage.</span></span>
<span data-ttu-id="848e1-132">매개 변수는 SAS URI를 지원하고, 패치 시나리오 대상은 SAS URI일 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="848e1-132">The parameter supports SAS URI, although patching scenarios destination cannot be an SAS URI.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: dst

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="848e1-133">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="848e1-133">-LocalFilePath</span></span>
<span data-ttu-id="848e1-134">로컬 .vhd 파일의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="848e1-134">Specifies the path of the local .vhd file.</span></span>

```yaml
Type: System.IO.FileInfo
Parameter Sets: (All)
Aliases: lf

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="848e1-135">-NumberOfUploaderThreads</span><span class="sxs-lookup"><span data-stu-id="848e1-135">-NumberOfUploaderThreads</span></span>
<span data-ttu-id="848e1-136">.vhd 파일을 업로드할 때 사용할 업로더 스레드 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="848e1-136">Specifies the number of uploader threads to be used when uploading the .vhd file.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: th

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="848e1-137">-OverWrite</span><span class="sxs-lookup"><span data-stu-id="848e1-137">-OverWrite</span></span>
<span data-ttu-id="848e1-138">이 cmdlet이 있는 경우 지정된 대상 URI에 기존 Blob을 덮어 던지는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="848e1-138">Indicates that this cmdlet overwrites an existing blob in the specified destination URI, if one exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: o

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="848e1-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="848e1-139">-ResourceGroupName</span></span>
<span data-ttu-id="848e1-140">가상 머신의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="848e1-140">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="848e1-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="848e1-141">CommonParameters</span></span>
<span data-ttu-id="848e1-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="848e1-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="848e1-143">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="848e1-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="848e1-144">입력</span><span class="sxs-lookup"><span data-stu-id="848e1-144">INPUTS</span></span>

### <span data-ttu-id="848e1-145">System.String</span><span class="sxs-lookup"><span data-stu-id="848e1-145">System.String</span></span>

### <span data-ttu-id="848e1-146">System.Uri</span><span class="sxs-lookup"><span data-stu-id="848e1-146">System.Uri</span></span>

### <span data-ttu-id="848e1-147">System.IO.FileInfo</span><span class="sxs-lookup"><span data-stu-id="848e1-147">System.IO.FileInfo</span></span>

### <span data-ttu-id="848e1-148">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="848e1-148">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="848e1-149">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="848e1-149">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="848e1-150">출력</span><span class="sxs-lookup"><span data-stu-id="848e1-150">OUTPUTS</span></span>

### <span data-ttu-id="848e1-151">Microsoft.Azure.Commands.Compute.Models.VhdUploadContext</span><span class="sxs-lookup"><span data-stu-id="848e1-151">Microsoft.Azure.Commands.Compute.Models.VhdUploadContext</span></span>

## <span data-ttu-id="848e1-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="848e1-152">NOTES</span></span>

## <span data-ttu-id="848e1-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="848e1-153">RELATED LINKS</span></span>

[<span data-ttu-id="848e1-154">Save-AzVhd</span><span class="sxs-lookup"><span data-stu-id="848e1-154">Save-AzVhd</span></span>](./Save-AzVhd.md)


