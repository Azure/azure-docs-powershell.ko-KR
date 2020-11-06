---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D08DAA8B-B7BF-4167-AB16-F2723985A0B7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRMVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRMVhd.md
ms.openlocfilehash: 106f6d9ed794ac2e4595f480616fa2c64663e554
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537452"
---
# <span data-ttu-id="69524-101">Add-AzureRmVhd</span><span class="sxs-lookup"><span data-stu-id="69524-101">Add-AzureRmVhd</span></span>

## <span data-ttu-id="69524-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69524-102">SYNOPSIS</span></span>
<span data-ttu-id="69524-103">온-프레미스 가상 컴퓨터의 가상 하드 디스크를 Azure의 클라우드 저장소 계정에 있는 blob로 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="69524-103">Uploads a virtual hard disk from an on-premises virtual machine to a blob in a cloud storage account in Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69524-104">구문과</span><span class="sxs-lookup"><span data-stu-id="69524-104">SYNTAX</span></span>

```
Add-AzureRmVhd [[-ResourceGroupName] <String>] [-Destination] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfUploaderThreads] <Int32>] [[-BaseImageUriToPatch] <Uri>] [-OverWrite]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69524-105">설명은</span><span class="sxs-lookup"><span data-stu-id="69524-105">DESCRIPTION</span></span>
<span data-ttu-id="69524-106">**AzureRmVhd** cmdlet은 온-프레미스 가상 하드 디스크를 .vhd 파일 형식으로 blob 저장소 계정에 고정 가상 하드 디스크로 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="69524-106">The **Add-AzureRmVhd** cmdlet uploads on-premises virtual hard disks, in .vhd file format, to a blob storage account as fixed virtual hard disks.</span></span>
<span data-ttu-id="69524-107">지정 된 대상 URI에서 사용 될 업 로더 스레드 수를 구성 하거나 기존 blob을 덮어쓸 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="69524-107">You can configure the number of uploader threads that will be used or overwrite an existing blob in the specified destination URI.</span></span>
<span data-ttu-id="69524-108">또한 지원 되는 온-프레미스 .vhd 파일의 패치 된 버전을 업로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="69524-108">Also supported is the ability to upload a patched version of an on-premises .vhd file.</span></span>
<span data-ttu-id="69524-109">기본 가상 하드 디스크를 이미 업로드 한 경우 기본 이미지를 부모로 사용 하는 차이점 보관용 디스크를 업로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="69524-109">When a base virtual hard disk has already been uploaded, you can upload differencing disks that use the base image as the parent.</span></span>
<span data-ttu-id="69524-110">SA (공유 액세스 서명) URI도 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="69524-110">Shared access signature (SAS) URI is supported also.</span></span>

## <span data-ttu-id="69524-111">예제의</span><span class="sxs-lookup"><span data-stu-id="69524-111">EXAMPLES</span></span>

### <span data-ttu-id="69524-112">예제 1: VHD 파일 추가</span><span class="sxs-lookup"><span data-stu-id="69524-112">Example 1: Add a VHD file</span></span>
```
PS C:\> Add-AzureRmVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

<span data-ttu-id="69524-113">이 명령은 저장소 계정에 .vhd 파일을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="69524-113">This command adds a .vhd file to a storage account.</span></span>

### <span data-ttu-id="69524-114">예제 2: VHD 파일 추가 및 대상 덮어쓰기</span><span class="sxs-lookup"><span data-stu-id="69524-114">Example 2: Add a VHD file and overwrite the destination</span></span>
```
PS C:\> Add-AzureRmVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

<span data-ttu-id="69524-115">이 명령은 저장소 계정에 .vhd 파일을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="69524-115">This command adds a .vhd file to a storage account.</span></span>
<span data-ttu-id="69524-116">명령이 기존 파일을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="69524-116">The command overwrites an existing file.</span></span>

### <span data-ttu-id="69524-117">예제 3: VHD 파일 추가 및 스레드 수 지정</span><span class="sxs-lookup"><span data-stu-id="69524-117">Example 3: Add a VHD file and specify the number of threads</span></span>
```
PS C:\> Add-AzureRmVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32
```

<span data-ttu-id="69524-118">이 명령은 저장소 계정에 .vhd 파일을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="69524-118">This command adds a .vhd file to a storage account.</span></span>
<span data-ttu-id="69524-119">명령은 파일을 업로드 하는 데 사용할 스레드 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="69524-119">The command specifies the number of threads to use to upload the file.</span></span>

### <span data-ttu-id="69524-120">예제 4: VHD 파일 추가 및 SAS URI 지정</span><span class="sxs-lookup"><span data-stu-id="69524-120">Example 4: Add a VHD file and specify the SAS URI</span></span>
```
PS C:\> Add-AzureRmVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd?st=2013-01 -09T22%3A15%3A49Z&amp;se=2013-01-09T23%3A10%3A49Z&amp;sr=b&amp;sp=w&amp;sig=13T9Ow%2FRJAMmhfO%2FaP3HhKKJ6AY093SmveO SIV4%2FR7w%3D" -LocalFilePath "C:\vhd\win7baseimage.vhd"
```

<span data-ttu-id="69524-121">이 명령은 저장소 계정에 .vhd 파일을 추가 하 고 SAS URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="69524-121">This command adds a .vhd file to a storage account and specifies the SAS URI.</span></span>

## <span data-ttu-id="69524-122">변수</span><span class="sxs-lookup"><span data-stu-id="69524-122">PARAMETERS</span></span>

### <span data-ttu-id="69524-123">-BaseImageUriToPatch</span><span class="sxs-lookup"><span data-stu-id="69524-123">-BaseImageUriToPatch</span></span>
<span data-ttu-id="69524-124">Azure Blob Storage의 기본 이미지 blob에 대 한 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="69524-124">Specifies the URI to a base image blob in Azure Blob Storage.</span></span>
<span data-ttu-id="69524-125">이 매개 변수의 값으로 SA를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="69524-125">An SAS can be specified as the value for this parameter.</span></span>

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

### <span data-ttu-id="69524-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69524-126">-DefaultProfile</span></span>
<span data-ttu-id="69524-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="69524-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69524-128">-대상</span><span class="sxs-lookup"><span data-stu-id="69524-128">-Destination</span></span>
<span data-ttu-id="69524-129">Blob 저장소의 blob URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="69524-129">Specifies the URI of a blob in Blob Storage.</span></span>
<span data-ttu-id="69524-130">매개 변수는 SAS URI를 지원 하지만, 패치 시나리오는 대상에 SAS URI가 될 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="69524-130">The parameter supports SAS URI, although patching scenarios destination cannot be an SAS URI.</span></span>

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

### <span data-ttu-id="69524-131">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="69524-131">-LocalFilePath</span></span>
<span data-ttu-id="69524-132">로컬 .vhd 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="69524-132">Specifies the path of the local .vhd file.</span></span>

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

### <span data-ttu-id="69524-133">-NumberOfUploaderThreads</span><span class="sxs-lookup"><span data-stu-id="69524-133">-NumberOfUploaderThreads</span></span>
<span data-ttu-id="69524-134">.Vhd 파일을 업로드할 때 사용할 업 로더 스레드 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="69524-134">Specifies the number of uploader threads to be used when uploading the .vhd file.</span></span>

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

### <span data-ttu-id="69524-135">-OverWrite</span><span class="sxs-lookup"><span data-stu-id="69524-135">-OverWrite</span></span>
<span data-ttu-id="69524-136">이 cmdlet이 지정 된 대상 URI (있는 경우)에서 기존 blob을 덮어쓴다는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="69524-136">Indicates that this cmdlet overwrites an existing blob in the specified destination URI, if one exists.</span></span>

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

### <span data-ttu-id="69524-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69524-137">-ResourceGroupName</span></span>
<span data-ttu-id="69524-138">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="69524-138">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="69524-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69524-139">CommonParameters</span></span>
<span data-ttu-id="69524-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="69524-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69524-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69524-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69524-142">입력</span><span class="sxs-lookup"><span data-stu-id="69524-142">INPUTS</span></span>

## <span data-ttu-id="69524-143">출력</span><span class="sxs-lookup"><span data-stu-id="69524-143">OUTPUTS</span></span>

## <span data-ttu-id="69524-144">상속자</span><span class="sxs-lookup"><span data-stu-id="69524-144">NOTES</span></span>

## <span data-ttu-id="69524-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="69524-145">RELATED LINKS</span></span>

[<span data-ttu-id="69524-146">저장-AzureRmVhd</span><span class="sxs-lookup"><span data-stu-id="69524-146">Save-AzureRmVhd</span></span>](./Save-AzureRmVhd.md)


