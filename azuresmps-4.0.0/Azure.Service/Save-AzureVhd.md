---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E4660D0A-26CB-488C-9A29-3ED94A0DCDA2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4e62cb7ed272a5c0d5ff4ff0ecbafe30a0c5ee9e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045461"
---
# <span data-ttu-id="6b85b-101">Save-AzureVhd</span><span class="sxs-lookup"><span data-stu-id="6b85b-101">Save-AzureVhd</span></span>

## <span data-ttu-id="6b85b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b85b-102">SYNOPSIS</span></span>
<span data-ttu-id="6b85b-103">.Vhd 이미지를 다운로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b85b-103">Enables download of .vhd images.</span></span>

## <span data-ttu-id="6b85b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6b85b-104">SYNTAX</span></span>

```
Save-AzureVhd [-Source] <Uri> [-LocalFilePath] <FileInfo> [[-NumberOfThreads] <Int32>] [[-StorageKey] <String>]
 [-OverWrite] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="6b85b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6b85b-105">DESCRIPTION</span></span>
<span data-ttu-id="6b85b-106">**저장-azurevhd** cmdlet을 사용 하면 파일에 저장 된 blob에서 .vhd 이미지를 다운로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b85b-106">The **Save-AzureVhd** cmdlet enables download of .vhd images from a blob where they are stored to a file.</span></span>
<span data-ttu-id="6b85b-107">지정 된 파일 경로에 이미 존재 하는 파일을 사용 하거나 덮어쓰는 다운로더 스레드 수를 지정 하 여 다운로드 프로세스를 구성 하는 매개 변수가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b85b-107">It has parameters to configure the download process by specifying the number of downloader threads that are used or overwriting the file which already exists in the specified file path.</span></span>

<span data-ttu-id="6b85b-108">**저장-AzureVhd** 는 vhd 형식 변환을 수행 하지 않으며 blob이 그대로 다운로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b85b-108">**Save-AzureVhd** does not do any VHD format conversion and the blob is downloaded as it is.</span></span>

## <span data-ttu-id="6b85b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="6b85b-109">EXAMPLES</span></span>

### <span data-ttu-id="6b85b-110">예제 1: VHD 파일 다운로드</span><span class="sxs-lookup"><span data-stu-id="6b85b-110">Example 1: Download a VHD file</span></span>
```
PS C:\> Save-AzureVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

<span data-ttu-id="6b85b-111">이 명령은 .vhd 파일을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b85b-111">This command downloads a .vhd file.</span></span>

### <span data-ttu-id="6b85b-112">예제 2: VHD 파일 다운로드 및 로컬 파일 덮어쓰기</span><span class="sxs-lookup"><span data-stu-id="6b85b-112">Example 2: Download a VHD file and overwrite the local file</span></span>
```
PS C:\> Save-AzureVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

<span data-ttu-id="6b85b-113">이 명령은 .vhd 파일을 다운로드 하 고 대상 경로의 모든 파일을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="6b85b-113">This command downloads a .vhd file and overwrites any file in the destination path.</span></span>

### <span data-ttu-id="6b85b-114">예제 3: VHD 파일 다운로드 및 스레드 수 지정</span><span class="sxs-lookup"><span data-stu-id="6b85b-114">Example 3: Download a VHD file and specify the number of threads</span></span>
```
PS C:\> Save-AzureVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32
```

<span data-ttu-id="6b85b-115">이 명령은 .vhd 파일을 다운로드 하 고 스레드 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b85b-115">This command downloads a .vhd file and specifies the number of threads.</span></span>

### <span data-ttu-id="6b85b-116">예제 4: VHD 파일 다운로드 및 저장소 키 지정</span><span class="sxs-lookup"><span data-stu-id="6b85b-116">Example 4: Download a VHD file and specify the storage key</span></span>
```
PS C:\> Save-AzureVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -StorageKey "zNvcH0r5vAGmC5AbwEtpcyWCMyBd3eMDbdaa4ua6kwxq6vTZH3Y+sw=="
```

<span data-ttu-id="6b85b-117">이 명령은 .vhd 파일을 다운로드 하 고 저장소 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b85b-117">This command downloads a .vhd file and specifies the storage key.</span></span>

## <span data-ttu-id="6b85b-118">변수</span><span class="sxs-lookup"><span data-stu-id="6b85b-118">PARAMETERS</span></span>

### <span data-ttu-id="6b85b-119">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="6b85b-119">-InformationAction</span></span>
<span data-ttu-id="6b85b-120">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b85b-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6b85b-121">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6b85b-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6b85b-122">하기로</span><span class="sxs-lookup"><span data-stu-id="6b85b-122">Continue</span></span>
- <span data-ttu-id="6b85b-123">숨기기</span><span class="sxs-lookup"><span data-stu-id="6b85b-123">Ignore</span></span>
- <span data-ttu-id="6b85b-124">Inquire</span><span class="sxs-lookup"><span data-stu-id="6b85b-124">Inquire</span></span>
- <span data-ttu-id="6b85b-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6b85b-125">SilentlyContinue</span></span>
- <span data-ttu-id="6b85b-126">중지가</span><span class="sxs-lookup"><span data-stu-id="6b85b-126">Stop</span></span>
- <span data-ttu-id="6b85b-127">대기</span><span class="sxs-lookup"><span data-stu-id="6b85b-127">Suspend</span></span>

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

### <span data-ttu-id="6b85b-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6b85b-128">-InformationVariable</span></span>
<span data-ttu-id="6b85b-129">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b85b-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="6b85b-130">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="6b85b-130">-LocalFilePath</span></span>
<span data-ttu-id="6b85b-131">로컬 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b85b-131">Specifies the local file path.</span></span>

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

### <span data-ttu-id="6b85b-132">-NumberOfThreads</span><span class="sxs-lookup"><span data-stu-id="6b85b-132">-NumberOfThreads</span></span>
<span data-ttu-id="6b85b-133">이 cmdlet에서 다운로드 하는 동안 사용 하는 다운로드 스레드 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b85b-133">Specifies the number of download threads that this cmdlet uses during download.</span></span>

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

### <span data-ttu-id="6b85b-134">-OverWrite</span><span class="sxs-lookup"><span data-stu-id="6b85b-134">-OverWrite</span></span>
<span data-ttu-id="6b85b-135">이 cmdlet이 존재 하는 *LocalFilePath* 파일이 지정 된 파일을 삭제 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b85b-135">Specifies that this cmdlet deletes the file specified by *LocalFilePath* file if it exists.</span></span>

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

### <span data-ttu-id="6b85b-136">-프로필</span><span class="sxs-lookup"><span data-stu-id="6b85b-136">-Profile</span></span>
<span data-ttu-id="6b85b-137">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b85b-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6b85b-138">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="6b85b-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6b85b-139">-원본</span><span class="sxs-lookup"><span data-stu-id="6b85b-139">-Source</span></span>
<span data-ttu-id="6b85b-140">Blob에 대 한 URI (Uniform Resource Identifier)를 지정 합니다 `Azure` .</span><span class="sxs-lookup"><span data-stu-id="6b85b-140">Specifies the Uniform Resource Identifier (URI) to the blob in `Azure`.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: src

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b85b-141">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="6b85b-141">-StorageKey</span></span>
<span data-ttu-id="6b85b-142">Blob 저장소 계정의 저장소 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b85b-142">Specifies the storage key of the blob storage account.</span></span>
<span data-ttu-id="6b85b-143">이를 제공 하지 않으면 **-AzureVhd를 저장** 하 여 Azure에서 *sourceuri* 의 계정에 대 한 저장소 키를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b85b-143">If it is not provided, **Save-AzureVhd** attempts to determine the storage key of the account in *SourceUri* from Azure.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: sk

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b85b-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b85b-144">CommonParameters</span></span>
<span data-ttu-id="6b85b-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b85b-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b85b-146">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b85b-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b85b-147">입력</span><span class="sxs-lookup"><span data-stu-id="6b85b-147">INPUTS</span></span>

## <span data-ttu-id="6b85b-148">출력</span><span class="sxs-lookup"><span data-stu-id="6b85b-148">OUTPUTS</span></span>

## <span data-ttu-id="6b85b-149">상속자</span><span class="sxs-lookup"><span data-stu-id="6b85b-149">NOTES</span></span>

## <span data-ttu-id="6b85b-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6b85b-150">RELATED LINKS</span></span>

[<span data-ttu-id="6b85b-151">-AzureVhd 추가</span><span class="sxs-lookup"><span data-stu-id="6b85b-151">Add-AzureVhd</span></span>](./Add-AzureVhd.md)


