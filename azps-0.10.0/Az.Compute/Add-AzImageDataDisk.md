---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azimagedatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzImageDataDisk.md
ms.openlocfilehash: b6c1a7e8947a079a864aae31d12aedf244ecb81b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875249"
---
# <span data-ttu-id="0874a-101">Add-AzImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="0874a-101">Add-AzImageDataDisk</span></span>

## <span data-ttu-id="0874a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0874a-102">SYNOPSIS</span></span>
<span data-ttu-id="0874a-103">이미지 obejct에 데이터 디스크를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="0874a-103">Adds a data disk to an image obejct.</span></span>

## <span data-ttu-id="0874a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0874a-104">SYNTAX</span></span>

```
Add-AzImageDataDisk [-Image] <PSImage> [[-Lun] <Int32>] [[-BlobUri] <String>] [[-Caching] <CachingTypes>]
 [-DiskSizeGB <Int32>] [-StorageAccountType <StorageAccountTypes>] [-SnapshotId <String>]
 [-ManagedDiskId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0874a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0874a-105">DESCRIPTION</span></span>
<span data-ttu-id="0874a-106">**Add-AzImageDataDisk** cmdlet은 image 개체에 데이터 디스크를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="0874a-106">The **Add-AzImageDataDisk** cmdlet adds a data disk to an image object.</span></span>

## <span data-ttu-id="0874a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0874a-107">EXAMPLES</span></span>

### <span data-ttu-id="0874a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="0874a-108">Example 1</span></span>
```
PS C:\> $imageConfig = New-AzImageConfig -Location 'West US';
PS C:\> $osDiskVhdUri = "https://contoso.blob.core.windows.net/test/os.vhd"
PS C:\> $dataDiskVhdUri1 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $dataDiskVhdUri2 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> Set-AzImageOsDisk -Image $imageConfig -OsType 'Windows' -OsState 'Generalized' -BlobUri $osDiskVhdUri;
PS C:\> Add-AzImageDataDisk -Image $imageConfig -Lun 1 -BlobUri $dataDiskVhdUri1;
PS C:\> Add-AzImageDataDisk -Image $imageConfig -Lun 2 -BlobUri $dataDiskVhdUri2;
PS C:\> New-AzImage -Image $imageConfig -ImageName 'ImageName01' -ResourceGroupName 'ResourceGroup01';
```

<span data-ttu-id="0874a-109">첫 번째 명령은 image 개체를 만든 다음 $imageConfig 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0874a-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="0874a-110">다음 세 개의 명령은 운영 체제 디스크의 경로와 두 개의 데이터 디스크를 $osDiskVhdUri, $dataDiskVhdUri 1 및 $dataDiskVhdUri 2 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="0874a-110">The next three commands assign paths of operating system disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="0874a-111">이 방법은 다음 명령에 대 한 읽기 전용입니다.</span><span class="sxs-lookup"><span data-stu-id="0874a-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="0874a-112">다음 세 개의 명령은 각각 운영 체제 디스크와 두 개의 데이터 디스크를 $imageConfig에 저장 된 이미지에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="0874a-112">The next three commands each adds an operating system disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="0874a-113">각 디스크의 URI는 $osDiskVhdUri, $dataDiskVhdUri 1 및 $dataDiskVhdUri 2에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0874a-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="0874a-114">마지막 명령은 리소스 그룹 ResourceGroup01에 ImageName01 이라는 이미지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0874a-114">The final command creates an image named ImageName01 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="0874a-115">변수</span><span class="sxs-lookup"><span data-stu-id="0874a-115">PARAMETERS</span></span>

### <span data-ttu-id="0874a-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="0874a-116">-BlobUri</span></span>
<span data-ttu-id="0874a-117">Blob의 URI로 링크를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0874a-117">Specifies the link, as a URI, of the blob.</span></span>

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

### <span data-ttu-id="0874a-118">-캐싱</span><span class="sxs-lookup"><span data-stu-id="0874a-118">-Caching</span></span>
<span data-ttu-id="0874a-119">디스크의 캐싱 모드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0874a-119">Specifies the caching mode of the disk.</span></span>

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

### <span data-ttu-id="0874a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0874a-120">-DefaultProfile</span></span>
<span data-ttu-id="0874a-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0874a-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0874a-122">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="0874a-122">-DiskSizeGB</span></span>
<span data-ttu-id="0874a-123">디스크 크기를 기가바이트 (GB) 단위로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0874a-123">Specifies the size of the disk in Gigabytes (GB).</span></span>

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

### <span data-ttu-id="0874a-124">-이미지</span><span class="sxs-lookup"><span data-stu-id="0874a-124">-Image</span></span>
<span data-ttu-id="0874a-125">로컬 이미지 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0874a-125">Specifies a local image object.</span></span>

```yaml
Type: PSImage
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0874a-126">-Lun</span><span class="sxs-lookup"><span data-stu-id="0874a-126">-Lun</span></span>
<span data-ttu-id="0874a-127">LUN (논리 단위 번호)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0874a-127">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="0874a-128">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="0874a-128">-ManagedDiskId</span></span>
<span data-ttu-id="0874a-129">관리 디스크의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0874a-129">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="0874a-130">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="0874a-130">-SnapshotId</span></span>
<span data-ttu-id="0874a-131">스냅숏의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0874a-131">Specifies the ID of a snapshot.</span></span>

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

### <span data-ttu-id="0874a-132">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="0874a-132">-StorageAccountType</span></span>
<span data-ttu-id="0874a-133">데이터 이미지 디스크의 저장소 계정 유형</span><span class="sxs-lookup"><span data-stu-id="0874a-133">The Storage Account type of the data image disk</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0874a-134">-확인</span><span class="sxs-lookup"><span data-stu-id="0874a-134">-Confirm</span></span>
<span data-ttu-id="0874a-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0874a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0874a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0874a-136">-WhatIf</span></span>
<span data-ttu-id="0874a-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0874a-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0874a-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0874a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0874a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0874a-139">CommonParameters</span></span>
<span data-ttu-id="0874a-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0874a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0874a-141">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0874a-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0874a-142">입력</span><span class="sxs-lookup"><span data-stu-id="0874a-142">INPUTS</span></span>

### <span data-ttu-id="0874a-143">Microsoft. 관리. 이미지</span><span class="sxs-lookup"><span data-stu-id="0874a-143">Microsoft.Azure.Management.Compute.Models.Image</span></span>
<span data-ttu-id="0874a-144">시스템. i l l 시스템. Null 허용 `1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[System. l l l, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="0874a-144">System.Int32 System.String System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="0874a-145">출력</span><span class="sxs-lookup"><span data-stu-id="0874a-145">OUTPUTS</span></span>

### <span data-ttu-id="0874a-146">Microsoft. 관리. 이미지</span><span class="sxs-lookup"><span data-stu-id="0874a-146">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="0874a-147">상속자</span><span class="sxs-lookup"><span data-stu-id="0874a-147">NOTES</span></span>

## <span data-ttu-id="0874a-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0874a-148">RELATED LINKS</span></span>

