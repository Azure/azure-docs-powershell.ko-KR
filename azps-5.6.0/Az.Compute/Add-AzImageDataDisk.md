---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azimagedatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzImageDataDisk.md
ms.openlocfilehash: a5876f705749d1391540bffdf537899e29b9560d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981168"
---
# <span data-ttu-id="e2a16-101">Add-AzImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="e2a16-101">Add-AzImageDataDisk</span></span>

## <span data-ttu-id="e2a16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2a16-102">SYNOPSIS</span></span>
<span data-ttu-id="e2a16-103">이미지 개체에 데이터 디스크를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e2a16-103">Adds a data disk to an image object.</span></span>

## <span data-ttu-id="e2a16-104">구문</span><span class="sxs-lookup"><span data-stu-id="e2a16-104">SYNTAX</span></span>

```
Add-AzImageDataDisk [-Image] <PSImage> [[-Lun] <Int32>] [[-BlobUri] <String>] [[-Caching] <CachingTypes>]
 [-DiskSizeGB <Int32>] [-StorageAccountType <String>] [-SnapshotId <String>] [-ManagedDiskId <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e2a16-105">설명</span><span class="sxs-lookup"><span data-stu-id="e2a16-105">DESCRIPTION</span></span>
<span data-ttu-id="e2a16-106">**Add-AzImageDataDisk** cmdlet은 이미지 개체에 데이터 디스크를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e2a16-106">The **Add-AzImageDataDisk** cmdlet adds a data disk to an image object.</span></span>

## <span data-ttu-id="e2a16-107">예제</span><span class="sxs-lookup"><span data-stu-id="e2a16-107">EXAMPLES</span></span>

### <span data-ttu-id="e2a16-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="e2a16-108">Example 1</span></span>
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

<span data-ttu-id="e2a16-109">첫 번째 명령은 이미지 개체를 만든 다음, $imageConfig 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="e2a16-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="e2a16-110">다음 세 가지 명령은 운영 체제 디스크의 경로와 두 개의 데이터 디스크를 $osDiskVhdUri, $dataDiskVhdUri 1 및 $dataDiskVhdUri 2 변수에 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="e2a16-110">The next three commands assign paths of operating system disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="e2a16-111">이 방법은 다음 명령의 가독성을 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="e2a16-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="e2a16-112">다음 세 가지 명령은 각각 운영 체제 디스크와 두 개의 데이터 디스크를 저장한 이미지에 $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="e2a16-112">The next three commands each adds an operating system disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="e2a16-113">각 디스크의 URI는 $osDiskVhdUri, $dataDiskVhdUri 1 및 $dataDiskVhdUri 2에 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="e2a16-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="e2a16-114">마지막 명령은 ResourceGroup01 리소스 그룹에서 ImageName01이라는 이미지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e2a16-114">The final command creates an image named ImageName01 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="e2a16-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e2a16-115">PARAMETERS</span></span>

### <span data-ttu-id="e2a16-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="e2a16-116">-BlobUri</span></span>
<span data-ttu-id="e2a16-117">Blob의 링크를 URI로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e2a16-117">Specifies the link, as a URI, of the blob.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2a16-118">-캐싱</span><span class="sxs-lookup"><span data-stu-id="e2a16-118">-Caching</span></span>
<span data-ttu-id="e2a16-119">디스크의 캐싱 모드를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e2a16-119">Specifies the caching mode of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2a16-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2a16-120">-DefaultProfile</span></span>
<span data-ttu-id="e2a16-121">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e2a16-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2a16-122">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="e2a16-122">-DiskEncryptionSetId</span></span>
<span data-ttu-id="e2a16-123">고객 관리 디스크 암호화 집합의 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e2a16-123">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="e2a16-124">이는 관리 디스크에만 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e2a16-124">This can only be specified for managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2a16-125">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="e2a16-125">-DiskSizeGB</span></span>
<span data-ttu-id="e2a16-126">기가바이트(GB)의 디스크 크기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e2a16-126">Specifies the size of the disk in Gigabytes (GB).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2a16-127">-Image</span><span class="sxs-lookup"><span data-stu-id="e2a16-127">-Image</span></span>
<span data-ttu-id="e2a16-128">로컬 이미지 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e2a16-128">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2a16-129">-Lun</span><span class="sxs-lookup"><span data-stu-id="e2a16-129">-Lun</span></span>
<span data-ttu-id="e2a16-130">LUN(논리 단위 번호)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e2a16-130">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2a16-131">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="e2a16-131">-ManagedDiskId</span></span>
<span data-ttu-id="e2a16-132">관리 디스크의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e2a16-132">Specifies the ID of a managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2a16-133">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="e2a16-133">-SnapshotId</span></span>
<span data-ttu-id="e2a16-134">스냅숏의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e2a16-134">Specifies the ID of a snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2a16-135">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="e2a16-135">-StorageAccountType</span></span>
<span data-ttu-id="e2a16-136">데이터 이미지 디스크의 Storage 계정 유형</span><span class="sxs-lookup"><span data-stu-id="e2a16-136">The Storage Account type of the data image disk</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2a16-137">-확인</span><span class="sxs-lookup"><span data-stu-id="e2a16-137">-Confirm</span></span>
<span data-ttu-id="e2a16-138">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e2a16-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2a16-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2a16-139">-WhatIf</span></span>
<span data-ttu-id="e2a16-140">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e2a16-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e2a16-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e2a16-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2a16-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2a16-142">CommonParameters</span></span>
<span data-ttu-id="e2a16-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e2a16-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2a16-144">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e2a16-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2a16-145">입력</span><span class="sxs-lookup"><span data-stu-id="e2a16-145">INPUTS</span></span>

### <span data-ttu-id="e2a16-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="e2a16-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="e2a16-147">System.Int32</span><span class="sxs-lookup"><span data-stu-id="e2a16-147">System.Int32</span></span>

### <span data-ttu-id="e2a16-148">System.String</span><span class="sxs-lookup"><span data-stu-id="e2a16-148">System.String</span></span>

### <span data-ttu-id="e2a16-149">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="e2a16-149">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="e2a16-150">출력</span><span class="sxs-lookup"><span data-stu-id="e2a16-150">OUTPUTS</span></span>

### <span data-ttu-id="e2a16-151">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="e2a16-151">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="e2a16-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e2a16-152">NOTES</span></span>

## <span data-ttu-id="e2a16-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e2a16-153">RELATED LINKS</span></span>
