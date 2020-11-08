---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 99DC239C-EA68-4830-9345-762CD6A3F68C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 320b95add2806f48121151a71bdf36a572fa05a1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045718"
---
# <span data-ttu-id="d8eaf-101">Add-AzureVhd</span><span class="sxs-lookup"><span data-stu-id="d8eaf-101">Add-AzureVhd</span></span>

## <span data-ttu-id="d8eaf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8eaf-102">SYNOPSIS</span></span>
<span data-ttu-id="d8eaf-103">온-프레미스 컴퓨터의 VHD 파일을 Azure의 클라우드 저장소 계정에 있는 blob에 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8eaf-103">Uploads a VHD file from an on-premise computer to a blob in a cloud storage account in Azure.</span></span>

## <span data-ttu-id="d8eaf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d8eaf-104">SYNTAX</span></span>

```
Add-AzureVhd [-Destination] <Uri> [-LocalFilePath] <FileInfo> [[-NumberOfUploaderThreads] <Int32>]
 [[-BaseImageUriToPatch] <Uri>] [-OverWrite] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="d8eaf-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d8eaf-105">DESCRIPTION</span></span>
<span data-ttu-id="d8eaf-106">Vhd (가상 하드 디스크) 이미지에서 blob 저장소 계정에 대 한 **추가-azurevhd** cmdlet 업로드를 고정 된 .vhd 이미지로 변환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8eaf-106">The **Add-AzureVhd** cmdlet uploads on premise Virtual hard disk (VHD) images to a blob storage account as fixed .vhd images.</span></span>
<span data-ttu-id="d8eaf-107">이 파일에는 지정 된 대상 URI에 이미 존재 하는 blob을 사용 하거나 덮어쓰는 업 로더 스레드 수를 지정 하는 등 업로드 프로세스를 구성 하는 매개 변수가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8eaf-107">It has parameters to configure the upload process such as specifying the number of uploader threads that will be used or overwriting a blob which already exists in the specified destination URI.</span></span>
<span data-ttu-id="d8eaf-108">온-프레미스 VHD 이미지의 경우 패치 시나리오가 지원 되므로 이미 업로드 한 기본 이미지를 업로드할 필요 없이 diff 디스크 이미지를 업로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8eaf-108">For on premise VHD images, patching scenario is also supported so that diff disk images can be uploaded without having to upload the already uploaded base images.</span></span> <span data-ttu-id="d8eaf-109">SA (공유 액세스 서명) URI도 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d8eaf-109">Shared Access Signature (SAS) URI is also supported.</span></span>

## <span data-ttu-id="d8eaf-110">예제의</span><span class="sxs-lookup"><span data-stu-id="d8eaf-110">EXAMPLES</span></span>

### <span data-ttu-id="d8eaf-111">예제 1: VHD 파일 추가</span><span class="sxs-lookup"><span data-stu-id="d8eaf-111">Example 1: Add a VHD file</span></span>
```
PS C:\> Add-AzureVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

<span data-ttu-id="d8eaf-112">이 명령은 저장소 계정에 .vhd 파일을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8eaf-112">This command adds a .vhd file to a storage account.</span></span>

### <span data-ttu-id="d8eaf-113">예제 2: VHD 파일 추가 및 대상 덮어쓰기</span><span class="sxs-lookup"><span data-stu-id="d8eaf-113">Example 2: Add a VHD file and overwrite the destination</span></span>
```
PS C:\> Add-AzureVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

<span data-ttu-id="d8eaf-114">이 명령은 저장소 계정에 .vhd 파일을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8eaf-114">This command adds a .vhd file to a storage account.</span></span>

### <span data-ttu-id="d8eaf-115">예제 3: VHD 파일 추가 및 스레드 수 지정</span><span class="sxs-lookup"><span data-stu-id="d8eaf-115">Example 3: Add a VHD file and specify the number of threads</span></span>
```
PS C:\> Add-AzureVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32
```

<span data-ttu-id="d8eaf-116">이 명령은 저장소 계정에 .vhd 파일을 추가 하 고 파일을 업로드 하는 데 사용할 스레드 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8eaf-116">This command adds a .vhd file to a storage account and specifies the number of threads to use to upload the file.</span></span>

### <span data-ttu-id="d8eaf-117">예제 4: VHD 파일 추가 및 SAS URI 지정</span><span class="sxs-lookup"><span data-stu-id="d8eaf-117">Example 4: Add a VHD file and specify the SAS URI</span></span>
```
PS C:\> Add-AzureVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd?st=2013-01-09T22%3A15%3A49Z&amp;se=2013-01-09T23%3A10%3A49Z&amp;sr=b&amp;sp=w&amp;sig=13T9Ow%2FRJAMmhfO%2FaP3HhKKJ6AY093SmveOSIV4%2FR7w%3D" -LocalFilePath "C:\vhd\win7baseimage.vhd"
```

<span data-ttu-id="d8eaf-118">이 명령은 저장소 계정에 .vhd 파일을 추가 하 고 SAS URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8eaf-118">This command adds a .vhd file to a storage account and specifies the SAS URI.</span></span>

## <span data-ttu-id="d8eaf-119">변수</span><span class="sxs-lookup"><span data-stu-id="d8eaf-119">PARAMETERS</span></span>

### <span data-ttu-id="d8eaf-120">-BaseImageUriToPatch</span><span class="sxs-lookup"><span data-stu-id="d8eaf-120">-BaseImageUriToPatch</span></span>
<span data-ttu-id="d8eaf-121">Azure Blob Storage의 기본 이미지 blob에 대 한 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8eaf-121">Specifies an URI to a base image blob in Azure Blob Storage.</span></span>
<span data-ttu-id="d8eaf-122">URI 입력의 SA도 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d8eaf-122">SAS in URI input is supported as well.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: bs

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8eaf-123">-대상</span><span class="sxs-lookup"><span data-stu-id="d8eaf-123">-Destination</span></span>
<span data-ttu-id="d8eaf-124">Microsoft Azure Blob 저장소의 blob에 대 한 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8eaf-124">Specifies a URI to a blob in Microsoft Azure Blob Storage.</span></span>
<span data-ttu-id="d8eaf-125">URI 입력의 SA가 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d8eaf-125">SAS in URI input is supported.</span></span>
<span data-ttu-id="d8eaf-126">그러나 패치 시나리오에서 대상은 SAS URI 일 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d8eaf-126">However, in patching scenarios the destination cannot be a SAS URI.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: dst

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8eaf-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="d8eaf-127">-InformationAction</span></span>
<span data-ttu-id="d8eaf-128">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8eaf-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d8eaf-129">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d8eaf-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d8eaf-130">하기로</span><span class="sxs-lookup"><span data-stu-id="d8eaf-130">Continue</span></span>
- <span data-ttu-id="d8eaf-131">숨기기</span><span class="sxs-lookup"><span data-stu-id="d8eaf-131">Ignore</span></span>
- <span data-ttu-id="d8eaf-132">Inquire</span><span class="sxs-lookup"><span data-stu-id="d8eaf-132">Inquire</span></span>
- <span data-ttu-id="d8eaf-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d8eaf-133">SilentlyContinue</span></span>
- <span data-ttu-id="d8eaf-134">중지가</span><span class="sxs-lookup"><span data-stu-id="d8eaf-134">Stop</span></span>
- <span data-ttu-id="d8eaf-135">대기</span><span class="sxs-lookup"><span data-stu-id="d8eaf-135">Suspend</span></span>

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

### <span data-ttu-id="d8eaf-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d8eaf-136">-InformationVariable</span></span>
<span data-ttu-id="d8eaf-137">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8eaf-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d8eaf-138">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="d8eaf-138">-LocalFilePath</span></span>
<span data-ttu-id="d8eaf-139">로컬 .vhd 파일의 파일 경로를 분류 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8eaf-139">Species the file path of the local .vhd file.</span></span>

```yaml
Type: FileInfo
Parameter Sets: (All)
Aliases: lf

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8eaf-140">-NumberOfUploaderThreads</span><span class="sxs-lookup"><span data-stu-id="d8eaf-140">-NumberOfUploaderThreads</span></span>
<span data-ttu-id="d8eaf-141">업로드에 사용할 스레드 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8eaf-141">Specifies the number of threads to use for upload.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: th

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8eaf-142">-OverWrite</span><span class="sxs-lookup"><span data-stu-id="d8eaf-142">-OverWrite</span></span>
<span data-ttu-id="d8eaf-143">이 cmdlet이 지정 된 대상 URI (있는 경우)의 기존 blob을 삭제 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8eaf-143">Specifies that this cmdlet deletes the existing blob in the specified destination URI if it exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: o

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8eaf-144">-프로필</span><span class="sxs-lookup"><span data-stu-id="d8eaf-144">-Profile</span></span>
<span data-ttu-id="d8eaf-145">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8eaf-145">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d8eaf-146">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="d8eaf-146">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d8eaf-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8eaf-147">CommonParameters</span></span>
<span data-ttu-id="d8eaf-148">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8eaf-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8eaf-149">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8eaf-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8eaf-150">입력</span><span class="sxs-lookup"><span data-stu-id="d8eaf-150">INPUTS</span></span>

## <span data-ttu-id="d8eaf-151">출력</span><span class="sxs-lookup"><span data-stu-id="d8eaf-151">OUTPUTS</span></span>

## <span data-ttu-id="d8eaf-152">상속자</span><span class="sxs-lookup"><span data-stu-id="d8eaf-152">NOTES</span></span>

## <span data-ttu-id="d8eaf-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d8eaf-153">RELATED LINKS</span></span>

[<span data-ttu-id="d8eaf-154">-AzureVhd 저장</span><span class="sxs-lookup"><span data-stu-id="d8eaf-154">Save-AzureVhd</span></span>](./Save-AzureVhd.md)


