---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D08DAA8B-B7BF-4167-AB16-F2723985A0B7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvhd
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVhd.md
ms.openlocfilehash: 2277aac2d863a696cb04af06eafd78b07227db72
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869162"
---
# <span data-ttu-id="2ec61-101">Add-AzVhd</span><span class="sxs-lookup"><span data-stu-id="2ec61-101">Add-AzVhd</span></span>

## <span data-ttu-id="2ec61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ec61-102">SYNOPSIS</span></span>
<span data-ttu-id="2ec61-103">온-프레미스 가상 컴퓨터의 가상 하드 디스크를 Azure의 클라우드 저장소 계정에 있는 blob로 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ec61-103">Uploads a virtual hard disk from an on-premises virtual machine to a blob in a cloud storage account in Azure.</span></span>

## <span data-ttu-id="2ec61-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2ec61-104">SYNTAX</span></span>

```
Add-AzVhd [[-ResourceGroupName] <String>] [-Destination] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfUploaderThreads] <Int32>] [[-BaseImageUriToPatch] <Uri>] [-OverWrite] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ec61-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2ec61-105">DESCRIPTION</span></span>
<span data-ttu-id="2ec61-106">**AzVhd** cmdlet은 온-프레미스 가상 하드 디스크를 .vhd 파일 형식으로 blob 저장소 계정에 고정 가상 하드 디스크로 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ec61-106">The **Add-AzVhd** cmdlet uploads on-premises virtual hard disks, in .vhd file format, to a blob storage account as fixed virtual hard disks.</span></span>
<span data-ttu-id="2ec61-107">지정 된 대상 URI에서 사용 될 업 로더 스레드 수를 구성 하거나 기존 blob을 덮어쓸 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ec61-107">You can configure the number of uploader threads that will be used or overwrite an existing blob in the specified destination URI.</span></span>
<span data-ttu-id="2ec61-108">또한 지원 되는 온-프레미스 .vhd 파일의 패치 된 버전을 업로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ec61-108">Also supported is the ability to upload a patched version of an on-premises .vhd file.</span></span>
<span data-ttu-id="2ec61-109">기본 가상 하드 디스크를 이미 업로드 한 경우 기본 이미지를 부모로 사용 하는 차이점 보관용 디스크를 업로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ec61-109">When a base virtual hard disk has already been uploaded, you can upload differencing disks that use the base image as the parent.</span></span>
<span data-ttu-id="2ec61-110">SA (공유 액세스 서명) URI도 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ec61-110">Shared access signature (SAS) URI is supported also.</span></span>

## <span data-ttu-id="2ec61-111">예제의</span><span class="sxs-lookup"><span data-stu-id="2ec61-111">EXAMPLES</span></span>

### <span data-ttu-id="2ec61-112">예제 1: VHD 파일 추가</span><span class="sxs-lookup"><span data-stu-id="2ec61-112">Example 1: Add a VHD file</span></span>
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

<span data-ttu-id="2ec61-113">이 명령은 저장소 계정에 .vhd 파일을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ec61-113">This command adds a .vhd file to a storage account.</span></span>

### <span data-ttu-id="2ec61-114">예제 2: VHD 파일 추가 및 대상 덮어쓰기</span><span class="sxs-lookup"><span data-stu-id="2ec61-114">Example 2: Add a VHD file and overwrite the destination</span></span>
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

<span data-ttu-id="2ec61-115">이 명령은 저장소 계정에 .vhd 파일을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ec61-115">This command adds a .vhd file to a storage account.</span></span>
<span data-ttu-id="2ec61-116">명령이 기존 파일을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="2ec61-116">The command overwrites an existing file.</span></span>

### <span data-ttu-id="2ec61-117">예제 3: VHD 파일 추가 및 스레드 수 지정</span><span class="sxs-lookup"><span data-stu-id="2ec61-117">Example 3: Add a VHD file and specify the number of threads</span></span>
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfUploaderThreads 32
```

<span data-ttu-id="2ec61-118">이 명령은 저장소 계정에 .vhd 파일을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ec61-118">This command adds a .vhd file to a storage account.</span></span>
<span data-ttu-id="2ec61-119">명령은 파일을 업로드 하는 데 사용할 스레드 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ec61-119">The command specifies the number of threads to use to upload the file.</span></span>

### <span data-ttu-id="2ec61-120">예제 4: VHD 파일 추가 및 SAS URI 지정</span><span class="sxs-lookup"><span data-stu-id="2ec61-120">Example 4: Add a VHD file and specify the SAS URI</span></span>
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd?st=2013-01 -09T22%3A15%3A49Z&amp;se=2013-01-09T23%3A10%3A49Z&amp;sr=b&amp;sp=w&amp;sig=13T9Ow%2FRJAMmhfO%2FaP3HhKKJ6AY093SmveO SIV4%2FR7w%3D" -LocalFilePath "C:\vhd\win7baseimage.vhd"
```

<span data-ttu-id="2ec61-121">이 명령은 저장소 계정에 .vhd 파일을 추가 하 고 SAS URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ec61-121">This command adds a .vhd file to a storage account and specifies the SAS URI.</span></span>

## <span data-ttu-id="2ec61-122">변수</span><span class="sxs-lookup"><span data-stu-id="2ec61-122">PARAMETERS</span></span>

### <span data-ttu-id="2ec61-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2ec61-123">-AsJob</span></span>
<span data-ttu-id="2ec61-124">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ec61-124">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="2ec61-125">-BaseImageUriToPatch</span><span class="sxs-lookup"><span data-stu-id="2ec61-125">-BaseImageUriToPatch</span></span>
<span data-ttu-id="2ec61-126">Azure Blob Storage의 기본 이미지 blob에 대 한 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ec61-126">Specifies the URI to a base image blob in Azure Blob Storage.</span></span>
<span data-ttu-id="2ec61-127">이 매개 변수의 값으로 SA를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ec61-127">An SAS can be specified as the value for this parameter.</span></span>

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

### <span data-ttu-id="2ec61-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ec61-128">-DefaultProfile</span></span>
<span data-ttu-id="2ec61-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2ec61-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ec61-130">-대상</span><span class="sxs-lookup"><span data-stu-id="2ec61-130">-Destination</span></span>
<span data-ttu-id="2ec61-131">Blob 저장소의 blob URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ec61-131">Specifies the URI of a blob in Blob Storage.</span></span>
<span data-ttu-id="2ec61-132">매개 변수는 SAS URI를 지원 하지만, 패치 시나리오는 대상에 SAS URI가 될 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="2ec61-132">The parameter supports SAS URI, although patching scenarios destination cannot be an SAS URI.</span></span>

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

### <span data-ttu-id="2ec61-133">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="2ec61-133">-LocalFilePath</span></span>
<span data-ttu-id="2ec61-134">로컬 .vhd 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ec61-134">Specifies the path of the local .vhd file.</span></span>

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

### <span data-ttu-id="2ec61-135">-NumberOfUploaderThreads</span><span class="sxs-lookup"><span data-stu-id="2ec61-135">-NumberOfUploaderThreads</span></span>
<span data-ttu-id="2ec61-136">.Vhd 파일을 업로드할 때 사용할 업 로더 스레드 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ec61-136">Specifies the number of uploader threads to be used when uploading the .vhd file.</span></span>

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

### <span data-ttu-id="2ec61-137">-OverWrite</span><span class="sxs-lookup"><span data-stu-id="2ec61-137">-OverWrite</span></span>
<span data-ttu-id="2ec61-138">이 cmdlet이 지정 된 대상 URI (있는 경우)에서 기존 blob을 덮어쓴다는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="2ec61-138">Indicates that this cmdlet overwrites an existing blob in the specified destination URI, if one exists.</span></span>

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

### <span data-ttu-id="2ec61-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ec61-139">-ResourceGroupName</span></span>
<span data-ttu-id="2ec61-140">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ec61-140">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="2ec61-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ec61-141">CommonParameters</span></span>
<span data-ttu-id="2ec61-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ec61-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ec61-143">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ec61-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ec61-144">입력</span><span class="sxs-lookup"><span data-stu-id="2ec61-144">INPUTS</span></span>

### <span data-ttu-id="2ec61-145">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2ec61-145">System.String</span></span>

### <span data-ttu-id="2ec61-146">시스템 Uri</span><span class="sxs-lookup"><span data-stu-id="2ec61-146">System.Uri</span></span>

### <span data-ttu-id="2ec61-147">시스템. o. FileInfo</span><span class="sxs-lookup"><span data-stu-id="2ec61-147">System.IO.FileInfo</span></span>

### <span data-ttu-id="2ec61-148">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e])</span><span class="sxs-lookup"><span data-stu-id="2ec61-148">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="2ec61-149">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="2ec61-149">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2ec61-150">출력</span><span class="sxs-lookup"><span data-stu-id="2ec61-150">OUTPUTS</span></span>

### <span data-ttu-id="2ec61-151">VhdUploadContext를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ec61-151">Microsoft.Azure.Commands.Compute.Models.VhdUploadContext</span></span>

## <span data-ttu-id="2ec61-152">상속자</span><span class="sxs-lookup"><span data-stu-id="2ec61-152">NOTES</span></span>

## <span data-ttu-id="2ec61-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2ec61-153">RELATED LINKS</span></span>

[<span data-ttu-id="2ec61-154">저장-AzVhd</span><span class="sxs-lookup"><span data-stu-id="2ec61-154">Save-AzVhd</span></span>](./Save-AzVhd.md)


