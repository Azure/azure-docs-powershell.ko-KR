---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 18E1AD70-42A6-47A2-A685-6E218B6DC4BE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Save-AzureRmVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Save-AzureRmVhd.md
ms.openlocfilehash: cc43308f0e0051a050b3983968d9c86f67ec66b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537372"
---
# <span data-ttu-id="bc001-101">Save-AzureRmVhd</span><span class="sxs-lookup"><span data-stu-id="bc001-101">Save-AzureRmVhd</span></span>

## <span data-ttu-id="bc001-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc001-102">SYNOPSIS</span></span>
<span data-ttu-id="bc001-103">다운로드 한 .vhd 이미지를 로컬에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc001-103">Saves downloaded .vhd images locally.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc001-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bc001-104">SYNTAX</span></span>

### <span data-ttu-id="bc001-105">ResourceGroupParameterSetName</span><span class="sxs-lookup"><span data-stu-id="bc001-105">ResourceGroupParameterSetName</span></span>
```
Save-AzureRmVhd [-ResourceGroupName] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfThreads] <Int32>] [-OverWrite] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc001-106">StorageKeyParameterSetName</span><span class="sxs-lookup"><span data-stu-id="bc001-106">StorageKeyParameterSetName</span></span>
```
Save-AzureRmVhd [-StorageKey] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfThreads] <Int32>] [-OverWrite] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc001-107">설명은</span><span class="sxs-lookup"><span data-stu-id="bc001-107">DESCRIPTION</span></span>
<span data-ttu-id="bc001-108">**AzureRmVhd** cmdlet은 파일에 저장 된 blob에서 .vhd 이미지를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc001-108">The **Save-AzureRmVhd** cmdlet saves .vhd images from a blob where they are stored to a file.</span></span>
<span data-ttu-id="bc001-109">프로세스에 사용 되는 다운로더 스레드 수와 기존 파일의 대체 여부를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bc001-109">You can specify the number of downloader threads that the process uses and whether to replace a file that already exists.</span></span>

<span data-ttu-id="bc001-110">이 cmdlet은 콘텐츠가 있는 그대로 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc001-110">This cmdlet downloads content as it is.</span></span>
<span data-ttu-id="bc001-111">VHD (가상 하드 디스크) 형식 변환은 적용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bc001-111">It does not apply any Virtual Hard Disk (VHD) format conversion.</span></span>

## <span data-ttu-id="bc001-112">예제의</span><span class="sxs-lookup"><span data-stu-id="bc001-112">EXAMPLES</span></span>

### <span data-ttu-id="bc001-113">예제 1: 이미지 다운로드</span><span class="sxs-lookup"><span data-stu-id="bc001-113">Example 1: Download an image</span></span>
```
PS C:\> Save-AzureRmVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

<span data-ttu-id="bc001-114">이 명령은 .vhd 파일을 다운로드 하 여 로컬 경로 C:\vhd\Win7Image.vhd.에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc001-114">This command downloads a .vhd file, and stores it in the local path C:\vhd\Win7Image.vhd.</span></span>

### <span data-ttu-id="bc001-115">예제 2: 이미지 다운로드 및 로컬 파일 덮어쓰기</span><span class="sxs-lookup"><span data-stu-id="bc001-115">Example 2: Download an image and overwrite the local file</span></span>
```
PS C:\> Save-AzureRmVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

<span data-ttu-id="bc001-116">이 명령은 .vhd 파일을 다운로드 하 여 로컬 경로에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc001-116">This command downloads a .vhd file, and stores it in the local path.</span></span>
<span data-ttu-id="bc001-117">명령에 *Overwrite* 매개 변수가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bc001-117">The command includes the *Overwrite* parameter.</span></span>
<span data-ttu-id="bc001-118">따라서 C:\vhd\Win7Image.vhd 이미 있는 경우이 명령은 해당 명령을 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="bc001-118">Therefore, if C:\vhd\Win7Image.vhd already exists, this command replaces it.</span></span>

### <span data-ttu-id="bc001-119">예제 3: 지정 된 수의 스레드를 사용 하 여 이미지 다운로드</span><span class="sxs-lookup"><span data-stu-id="bc001-119">Example 3: Download an image by using a specified number of threads</span></span>
```
PS C:\> Save-AzureRmVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32
```

<span data-ttu-id="bc001-120">이 명령은 .vhd 파일을 다운로드 하 여 로컬 경로에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc001-120">This command downloads a .vhd file, and stores it in the local path.</span></span>
<span data-ttu-id="bc001-121">명령이 *Numberofthreads* 매개 변수에 대 한 32 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc001-121">The command specifies a value of 32 for the *NumberOfThreads* parameter.</span></span>
<span data-ttu-id="bc001-122">따라서 cmdlet은이 작업을 위해 32 스레드를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc001-122">Therefore, the cmdlet uses 32 threads for this action.</span></span>

### <span data-ttu-id="bc001-123">예제 4: 이미지 다운로드 및 저장소 키 지정</span><span class="sxs-lookup"><span data-stu-id="bc001-123">Example 4: Download an image and specify the storage key</span></span>
```
PS C:\> Save-AzureRmVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -StorageKey "zNvcH0r5vAGmC5AbwEtpcyWCMyBd3eMDbdaa4ua6kwxq6vTZH3Y+sw=="
```

<span data-ttu-id="bc001-124">이 명령은 .vhd 파일을 다운로드 하 고 저장소 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc001-124">This command downloads a .vhd file and specifies the storage key.</span></span>

## <span data-ttu-id="bc001-125">변수</span><span class="sxs-lookup"><span data-stu-id="bc001-125">PARAMETERS</span></span>

### <span data-ttu-id="bc001-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc001-126">-DefaultProfile</span></span>
<span data-ttu-id="bc001-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bc001-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc001-128">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="bc001-128">-LocalFilePath</span></span>
<span data-ttu-id="bc001-129">저장 된 이미지의 로컬 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc001-129">Specifies the local file path of the saved image.</span></span>

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

### <span data-ttu-id="bc001-130">-NumberOfThreads</span><span class="sxs-lookup"><span data-stu-id="bc001-130">-NumberOfThreads</span></span>
<span data-ttu-id="bc001-131">이 cmdlet에서 다운로드 하는 동안 사용 하는 다운로드 스레드 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc001-131">Specifies the number of download threads that this cmdlet uses during download.</span></span>

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

### <span data-ttu-id="bc001-132">-OverWrite</span><span class="sxs-lookup"><span data-stu-id="bc001-132">-OverWrite</span></span>
<span data-ttu-id="bc001-133">이 cmdlet이 존재 하는 *LocalFilePath* 파일이 지정 된 파일을 대체 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="bc001-133">Indicates that this cmdlet replaces the file specified by *LocalFilePath* file if it exists.</span></span>

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

### <span data-ttu-id="bc001-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc001-134">-ResourceGroupName</span></span>
<span data-ttu-id="bc001-135">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc001-135">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="bc001-136">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="bc001-136">-SourceUri</span></span>
<span data-ttu-id="bc001-137">에서 blob의 URI (Uniform Resource Identifier)를 지정 합니다 `Azure` .</span><span class="sxs-lookup"><span data-stu-id="bc001-137">Specifies the Uniform Resource Identifier (URI) of the blob in `Azure`.</span></span>

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

### <span data-ttu-id="bc001-138">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="bc001-138">-StorageKey</span></span>
<span data-ttu-id="bc001-139">Blob 저장소 계정의 저장소 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc001-139">Specifies the storage key of the blob storage account.</span></span>
<span data-ttu-id="bc001-140">키를 지정 하지 않으면이 cmdlet은 Azure에서 *Sourceuri* 의 계정에 대 한 저장소 키를 확인 하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc001-140">If you do not specify a key, this cmdlet attempts to determine the storage key of the account in *SourceUri* from Azure.</span></span>

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

### <span data-ttu-id="bc001-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc001-141">CommonParameters</span></span>
<span data-ttu-id="bc001-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc001-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc001-143">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc001-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc001-144">입력</span><span class="sxs-lookup"><span data-stu-id="bc001-144">INPUTS</span></span>

## <span data-ttu-id="bc001-145">출력</span><span class="sxs-lookup"><span data-stu-id="bc001-145">OUTPUTS</span></span>

## <span data-ttu-id="bc001-146">상속자</span><span class="sxs-lookup"><span data-stu-id="bc001-146">NOTES</span></span>

## <span data-ttu-id="bc001-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bc001-147">RELATED LINKS</span></span>

[<span data-ttu-id="bc001-148">추가-AzureRmVhd</span><span class="sxs-lookup"><span data-stu-id="bc001-148">Add-AzureRmVhd</span></span>](./Add-AzureRMVhd.md)


