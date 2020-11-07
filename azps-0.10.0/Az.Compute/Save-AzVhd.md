---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 18E1AD70-42A6-47A2-A685-6E218B6DC4BE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/save-azvhd
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Save-AzVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Save-AzVhd.md
ms.openlocfilehash: f178b6aca1cf3747bc53807290585c01b91f3c2e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876921"
---
# <span data-ttu-id="99069-101">Save-AzVhd</span><span class="sxs-lookup"><span data-stu-id="99069-101">Save-AzVhd</span></span>

## <span data-ttu-id="99069-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99069-102">SYNOPSIS</span></span>
<span data-ttu-id="99069-103">다운로드 한 .vhd 이미지를 로컬에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="99069-103">Saves downloaded .vhd images locally.</span></span>

## <span data-ttu-id="99069-104">구문과</span><span class="sxs-lookup"><span data-stu-id="99069-104">SYNTAX</span></span>

### <span data-ttu-id="99069-105">ResourceGroupParameterSetName</span><span class="sxs-lookup"><span data-stu-id="99069-105">ResourceGroupParameterSetName</span></span>
```
Save-AzVhd [-ResourceGroupName] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfThreads] <Int32>] [-OverWrite] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="99069-106">StorageKeyParameterSetName</span><span class="sxs-lookup"><span data-stu-id="99069-106">StorageKeyParameterSetName</span></span>
```
Save-AzVhd [-StorageKey] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfThreads] <Int32>] [-OverWrite] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="99069-107">설명은</span><span class="sxs-lookup"><span data-stu-id="99069-107">DESCRIPTION</span></span>
<span data-ttu-id="99069-108">**AzVhd** cmdlet은 파일에 저장 된 blob에서 .vhd 이미지를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="99069-108">The **Save-AzVhd** cmdlet saves .vhd images from a blob where they are stored to a file.</span></span>
<span data-ttu-id="99069-109">프로세스에 사용 되는 다운로더 스레드 수와 기존 파일의 대체 여부를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="99069-109">You can specify the number of downloader threads that the process uses and whether to replace a file that already exists.</span></span>

<span data-ttu-id="99069-110">이 cmdlet은 콘텐츠가 있는 그대로 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="99069-110">This cmdlet downloads content as it is.</span></span>
<span data-ttu-id="99069-111">VHD (가상 하드 디스크) 형식 변환은 적용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="99069-111">It does not apply any Virtual Hard Disk (VHD) format conversion.</span></span>

## <span data-ttu-id="99069-112">예제의</span><span class="sxs-lookup"><span data-stu-id="99069-112">EXAMPLES</span></span>

### <span data-ttu-id="99069-113">예제 1: 이미지 다운로드</span><span class="sxs-lookup"><span data-stu-id="99069-113">Example 1: Download an image</span></span>
```
PS C:\> Save-AzVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -ResourceGroupName "rgname"
```

<span data-ttu-id="99069-114">이 명령은 .vhd 파일을 다운로드 하 여 로컬 경로 C:\vhd\Win7Image.vhd.에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="99069-114">This command downloads a .vhd file, and stores it in the local path C:\vhd\Win7Image.vhd.</span></span>

### <span data-ttu-id="99069-115">예제 2: 이미지 다운로드 및 로컬 파일 덮어쓰기</span><span class="sxs-lookup"><span data-stu-id="99069-115">Example 2: Download an image and overwrite the local file</span></span>
```
PS C:\> Save-AzVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite -ResourceGroupName "rgname"
```

<span data-ttu-id="99069-116">이 명령은 .vhd 파일을 다운로드 하 여 로컬 경로에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="99069-116">This command downloads a .vhd file, and stores it in the local path.</span></span>
<span data-ttu-id="99069-117">명령에 *Overwrite* 매개 변수가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="99069-117">The command includes the *Overwrite* parameter.</span></span>
<span data-ttu-id="99069-118">따라서 C:\vhd\Win7Image.vhd 이미 있는 경우이 명령은 해당 명령을 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="99069-118">Therefore, if C:\vhd\Win7Image.vhd already exists, this command replaces it.</span></span>

### <span data-ttu-id="99069-119">예제 3: 지정 된 수의 스레드를 사용 하 여 이미지 다운로드</span><span class="sxs-lookup"><span data-stu-id="99069-119">Example 3: Download an image by using a specified number of threads</span></span>
```
PS C:\> Save-AzVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32 -ResourceGroupName "rgname"
```

<span data-ttu-id="99069-120">이 명령은 .vhd 파일을 다운로드 하 여 로컬 경로에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="99069-120">This command downloads a .vhd file, and stores it in the local path.</span></span>
<span data-ttu-id="99069-121">명령이 *Numberofthreads* 매개 변수에 대 한 32 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99069-121">The command specifies a value of 32 for the *NumberOfThreads* parameter.</span></span>
<span data-ttu-id="99069-122">따라서 cmdlet은이 작업을 위해 32 스레드를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="99069-122">Therefore, the cmdlet uses 32 threads for this action.</span></span>

### <span data-ttu-id="99069-123">예제 4: 이미지 다운로드 및 저장소 키 지정</span><span class="sxs-lookup"><span data-stu-id="99069-123">Example 4: Download an image and specify the storage key</span></span>
```
PS C:\> Save-AzVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -StorageKey "zNvcH0r5vAGmC5AbwEtpcyWCMyBd3eMDbdaa4ua6kwxq6vTZH3Y+sw==" -ResourceGroupName "rgname"
```

<span data-ttu-id="99069-124">이 명령은 .vhd 파일을 다운로드 하 고 저장소 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99069-124">This command downloads a .vhd file and specifies the storage key.</span></span>

## <span data-ttu-id="99069-125">변수</span><span class="sxs-lookup"><span data-stu-id="99069-125">PARAMETERS</span></span>

### <span data-ttu-id="99069-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="99069-126">-AsJob</span></span>
<span data-ttu-id="99069-127">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="99069-127">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="99069-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99069-128">-DefaultProfile</span></span>
<span data-ttu-id="99069-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="99069-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99069-130">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="99069-130">-LocalFilePath</span></span>
<span data-ttu-id="99069-131">저장 된 이미지의 로컬 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99069-131">Specifies the local file path of the saved image.</span></span>

```yaml
Type: FileInfo
Parameter Sets: (All)
Aliases: lf

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99069-132">-NumberOfThreads</span><span class="sxs-lookup"><span data-stu-id="99069-132">-NumberOfThreads</span></span>
<span data-ttu-id="99069-133">이 cmdlet에서 다운로드 하는 동안 사용 하는 다운로드 스레드 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99069-133">Specifies the number of download threads that this cmdlet uses during download.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: th

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99069-134">-OverWrite</span><span class="sxs-lookup"><span data-stu-id="99069-134">-OverWrite</span></span>
<span data-ttu-id="99069-135">이 cmdlet이 존재 하는 *LocalFilePath* 파일이 지정 된 파일을 대체 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="99069-135">Indicates that this cmdlet replaces the file specified by *LocalFilePath* file if it exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: o

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99069-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99069-136">-ResourceGroupName</span></span>
<span data-ttu-id="99069-137">저장소 계정의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99069-137">Specifies the name of the resource group of the storage account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99069-138">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="99069-138">-SourceUri</span></span>
<span data-ttu-id="99069-139">에서 blob의 URI (Uniform Resource Identifier)를 지정 합니다 `Azure` .</span><span class="sxs-lookup"><span data-stu-id="99069-139">Specifies the Uniform Resource Identifier (URI) of the blob in `Azure`.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: src, Source

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99069-140">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="99069-140">-StorageKey</span></span>
<span data-ttu-id="99069-141">Blob 저장소 계정의 저장소 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99069-141">Specifies the storage key of the blob storage account.</span></span>
<span data-ttu-id="99069-142">키를 지정 하지 않으면이 cmdlet은 Azure에서 *Sourceuri* 의 계정에 대 한 저장소 키를 확인 하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="99069-142">If you do not specify a key, this cmdlet attempts to determine the storage key of the account in *SourceUri* from Azure.</span></span>

```yaml
Type: String
Parameter Sets: StorageKeyParameterSetName
Aliases: sk

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99069-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99069-143">CommonParameters</span></span>
<span data-ttu-id="99069-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="99069-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99069-145">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99069-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99069-146">입력</span><span class="sxs-lookup"><span data-stu-id="99069-146">INPUTS</span></span>

### <span data-ttu-id="99069-147">않아야</span><span class="sxs-lookup"><span data-stu-id="99069-147">None</span></span>
<span data-ttu-id="99069-148">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="99069-148">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="99069-149">출력</span><span class="sxs-lookup"><span data-stu-id="99069-149">OUTPUTS</span></span>

### <span data-ttu-id="99069-150">VhdDownloadContext를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="99069-150">Microsoft.Azure.Commands.Compute.Models.VhdDownloadContext</span></span>

## <span data-ttu-id="99069-151">상속자</span><span class="sxs-lookup"><span data-stu-id="99069-151">NOTES</span></span>

## <span data-ttu-id="99069-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="99069-152">RELATED LINKS</span></span>

[<span data-ttu-id="99069-153">추가-AzVhd</span><span class="sxs-lookup"><span data-stu-id="99069-153">Add-AzVhd</span></span>](./Add-AzVhd.md)


