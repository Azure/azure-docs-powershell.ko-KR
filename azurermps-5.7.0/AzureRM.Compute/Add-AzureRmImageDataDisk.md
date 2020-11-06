---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmImageDataDisk.md
ms.openlocfilehash: 13f98e0e0b34e4e192f108e20bcb6f52047b7611
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531763"
---
# <span data-ttu-id="65a77-101">Add-AzureRmImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="65a77-101">Add-AzureRmImageDataDisk</span></span>

## <span data-ttu-id="65a77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65a77-102">SYNOPSIS</span></span>
<span data-ttu-id="65a77-103">Image 개체에 데이터 디스크를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="65a77-103">Adds a data disk to an image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65a77-104">구문과</span><span class="sxs-lookup"><span data-stu-id="65a77-104">SYNTAX</span></span>

```
Add-AzureRmImageDataDisk [-Image] <Image> [[-Lun] <Int32>] [[-BlobUri] <String>] [[-Caching] <CachingTypes>]
 [-DiskSizeGB <Int32>] [-StorageAccountType <StorageAccountTypes>] [-SnapshotId <String>]
 [-ManagedDiskId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65a77-105">설명은</span><span class="sxs-lookup"><span data-stu-id="65a77-105">DESCRIPTION</span></span>
<span data-ttu-id="65a77-106">**Add-AzureRmImageDataDisk** cmdlet은 image 개체에 데이터 디스크를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="65a77-106">The **Add-AzureRmImageDataDisk** cmdlet adds a data disk to an image object.</span></span>

## <span data-ttu-id="65a77-107">예제의</span><span class="sxs-lookup"><span data-stu-id="65a77-107">EXAMPLES</span></span>

### <span data-ttu-id="65a77-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="65a77-108">Example 1</span></span>
```
PS C:\> $imageConfig = New-AzureRmImageConfig -Location 'West US';
PS C:\> $osDiskVhdUri = "https://contoso.blob.core.windows.net/test/os.vhd"
PS C:\> $dataDiskVhdUri1 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $dataDiskVhdUri2 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> Set-AzureRmImageOsDisk -Image $imageConfig -OsType 'Windows' -OsState 'Generalized' -BlobUri $osDiskVhdUri;
PS C:\> Add-AzureRmImageDataDisk -Image $imageConfig -Lun 1 -BlobUri $dataDiskVhdUri1;
PS C:\> Add-AzureRmImageDataDisk -Image $imageConfig -Lun 2 -BlobUri $dataDiskVhdUri2;
PS C:\> New-AzureRmImage -Image $imageConfig -ImageName 'ImageName01' -ResourceGroupName 'ResourceGroup01';
```

<span data-ttu-id="65a77-109">첫 번째 명령은 image 개체를 만든 다음 $imageConfig 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="65a77-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="65a77-110">다음 세 개의 명령은 운영 체제 디스크의 경로와 두 개의 데이터 디스크를 $osDiskVhdUri, $dataDiskVhdUri 1 및 $dataDiskVhdUri 2 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="65a77-110">The next three commands assign paths of operating system disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="65a77-111">이 방법은 다음 명령에 대 한 읽기 전용입니다.</span><span class="sxs-lookup"><span data-stu-id="65a77-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="65a77-112">다음 세 개의 명령은 각각 운영 체제 디스크와 두 개의 데이터 디스크를 $imageConfig에 저장 된 이미지에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="65a77-112">The next three commands each adds an operating system disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="65a77-113">각 디스크의 URI는 $osDiskVhdUri, $dataDiskVhdUri 1 및 $dataDiskVhdUri 2에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="65a77-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="65a77-114">마지막 명령은 리소스 그룹 ResourceGroup01에 ImageName01 이라는 이미지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="65a77-114">The final command creates an image named ImageName01 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="65a77-115">변수</span><span class="sxs-lookup"><span data-stu-id="65a77-115">PARAMETERS</span></span>

### <span data-ttu-id="65a77-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="65a77-116">-BlobUri</span></span>
<span data-ttu-id="65a77-117">Blob의 URI로 링크를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65a77-117">Specifies the link, as a URI, of the blob.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65a77-118">-캐싱</span><span class="sxs-lookup"><span data-stu-id="65a77-118">-Caching</span></span>
<span data-ttu-id="65a77-119">디스크의 캐싱 모드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65a77-119">Specifies the caching mode of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65a77-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="65a77-120">-DiskSizeGB</span></span>
<span data-ttu-id="65a77-121">디스크 크기를 기가바이트 (GB) 단위로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65a77-121">Specifies the size of the disk in Gigabytes (GB).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65a77-122">-이미지</span><span class="sxs-lookup"><span data-stu-id="65a77-122">-Image</span></span>
<span data-ttu-id="65a77-123">로컬 이미지 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65a77-123">Specifies a local image object.</span></span>

```yaml
Type: Image
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65a77-124">-Lun</span><span class="sxs-lookup"><span data-stu-id="65a77-124">-Lun</span></span>
<span data-ttu-id="65a77-125">LUN (논리 단위 번호)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65a77-125">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65a77-126">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="65a77-126">-ManagedDiskId</span></span>
<span data-ttu-id="65a77-127">관리 디스크의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65a77-127">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="65a77-128">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="65a77-128">-SnapshotId</span></span>
<span data-ttu-id="65a77-129">스냅숏의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65a77-129">Specifies the ID of a snapshot.</span></span>

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

### <span data-ttu-id="65a77-130">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="65a77-130">-StorageAccountType</span></span>
<span data-ttu-id="65a77-131">데이터 이미지 디스크의 저장소 계정 유형</span><span class="sxs-lookup"><span data-stu-id="65a77-131">The Storage Account type of the data image disk</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65a77-132">-확인</span><span class="sxs-lookup"><span data-stu-id="65a77-132">-Confirm</span></span>
<span data-ttu-id="65a77-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="65a77-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65a77-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65a77-134">-WhatIf</span></span>
<span data-ttu-id="65a77-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="65a77-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="65a77-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="65a77-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65a77-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65a77-137">CommonParameters</span></span>
<span data-ttu-id="65a77-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="65a77-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65a77-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65a77-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65a77-140">입력</span><span class="sxs-lookup"><span data-stu-id="65a77-140">INPUTS</span></span>

### <span data-ttu-id="65a77-141">Microsoft. 관리. 이미지</span><span class="sxs-lookup"><span data-stu-id="65a77-141">Microsoft.Azure.Management.Compute.Models.Image</span></span>
<span data-ttu-id="65a77-142">시스템. i l l 시스템. Null 허용 `1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[System. l l l, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="65a77-142">System.Int32 System.String System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="65a77-143">출력</span><span class="sxs-lookup"><span data-stu-id="65a77-143">OUTPUTS</span></span>

### <span data-ttu-id="65a77-144">Microsoft. 관리. 이미지</span><span class="sxs-lookup"><span data-stu-id="65a77-144">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="65a77-145">상속자</span><span class="sxs-lookup"><span data-stu-id="65a77-145">NOTES</span></span>

## <span data-ttu-id="65a77-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="65a77-146">RELATED LINKS</span></span>
