---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azimageosdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzImageOsDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzImageOsDisk.md
ms.openlocfilehash: 45f3e8f76e6f8ff3a5684fbd8f9ebf42e7a8e252
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495939"
---
# <span data-ttu-id="07beb-101">Set-AzImageOsDisk</span><span class="sxs-lookup"><span data-stu-id="07beb-101">Set-AzImageOsDisk</span></span>

## <span data-ttu-id="07beb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07beb-102">SYNOPSIS</span></span>
<span data-ttu-id="07beb-103">이미지 개체에 대한 운영 체제 디스크 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="07beb-103">Sets the operating system disk properties on an image object.</span></span>

## <span data-ttu-id="07beb-104">구문</span><span class="sxs-lookup"><span data-stu-id="07beb-104">SYNTAX</span></span>

```
Set-AzImageOsDisk [-Image] <PSImage> [[-OsType] <OperatingSystemTypes>]
 [[-OsState] <OperatingSystemStateTypes>] [[-BlobUri] <String>] [-Caching <CachingTypes>] [-DiskSizeGB <Int32>]
 [-StorageAccountType <String>] [-SnapshotId <String>] [-ManagedDiskId <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="07beb-105">설명</span><span class="sxs-lookup"><span data-stu-id="07beb-105">DESCRIPTION</span></span>
<span data-ttu-id="07beb-106">**Set-AzImageOsDisk** cmdlet은 이미지 개체에 운영 체제 디스크 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="07beb-106">The **Set-AzImageOsDisk** cmdlet sets the operating system disk properties on an image object.</span></span>

## <span data-ttu-id="07beb-107">예제</span><span class="sxs-lookup"><span data-stu-id="07beb-107">EXAMPLES</span></span>

### <span data-ttu-id="07beb-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="07beb-108">Example 1</span></span>
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

<span data-ttu-id="07beb-109">첫 번째 명령은 이미지 개체를 만든 다음 이미지 $imageConfig 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="07beb-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="07beb-110">다음 세 명령은 os 디스크의 경로와 두 개의 데이터 디스크를 $osDiskVhdUri, $dataDiskVhdUri 1 및 $dataDiskVhdUri 2 변수에 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="07beb-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="07beb-111">이 방법은 다음 명령의 가독성에만 해당됩니다.</span><span class="sxs-lookup"><span data-stu-id="07beb-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="07beb-112">다음 세 명령은 각각 os 디스크와 2개의 데이터 디스크를 각 디스크에 저장된 이미지에 $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="07beb-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="07beb-113">각 디스크의 URI는 $osDiskVhdUri, $dataDiskVhdUri 1 및 $dataDiskVhdUri 2에 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="07beb-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="07beb-114">마지막 명령은 리소스 그룹 'ResourceGroup01'에 'ImageName01'이라는 이미지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="07beb-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="07beb-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="07beb-115">PARAMETERS</span></span>

### <span data-ttu-id="07beb-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="07beb-116">-BlobUri</span></span>
<span data-ttu-id="07beb-117">Blob의 URI를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="07beb-117">Specifies the Uri of the blob.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07beb-118">-캐싱</span><span class="sxs-lookup"><span data-stu-id="07beb-118">-Caching</span></span>
<span data-ttu-id="07beb-119">디스크의 캐싱 모드를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="07beb-119">Specifies the caching mode of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07beb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07beb-120">-DefaultProfile</span></span>
<span data-ttu-id="07beb-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="07beb-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07beb-122">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="07beb-122">-DiskEncryptionSetId</span></span>
<span data-ttu-id="07beb-123">고객 관리 디스크 암호화 집합의 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="07beb-123">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="07beb-124">관리 디스크에만 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07beb-124">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="07beb-125">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="07beb-125">-DiskSizeGB</span></span>
<span data-ttu-id="07beb-126">디스크 크기를 GB로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="07beb-126">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="07beb-127">-Image</span><span class="sxs-lookup"><span data-stu-id="07beb-127">-Image</span></span>
<span data-ttu-id="07beb-128">로컬 이미지 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="07beb-128">Specifies a local image object.</span></span>

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

### <span data-ttu-id="07beb-129">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="07beb-129">-ManagedDiskId</span></span>
<span data-ttu-id="07beb-130">관리 디스크의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="07beb-130">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="07beb-131">-OsState</span><span class="sxs-lookup"><span data-stu-id="07beb-131">-OsState</span></span>
<span data-ttu-id="07beb-132">OS 상태를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="07beb-132">Specifies the OS state.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Generalized, Specialized

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07beb-133">-OsType</span><span class="sxs-lookup"><span data-stu-id="07beb-133">-OsType</span></span>
<span data-ttu-id="07beb-134">OS 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="07beb-134">Specifies the OS type.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07beb-135">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="07beb-135">-SnapshotId</span></span>
<span data-ttu-id="07beb-136">스냅숏의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="07beb-136">Specifies the ID of a snapshot.</span></span>

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

### <span data-ttu-id="07beb-137">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="07beb-137">-StorageAccountType</span></span>
<span data-ttu-id="07beb-138">Os 이미지 디스크의 Storage 계정 유형</span><span class="sxs-lookup"><span data-stu-id="07beb-138">The Storage Account type of Os Image Disk</span></span>

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

### <span data-ttu-id="07beb-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="07beb-139">-Confirm</span></span>
<span data-ttu-id="07beb-140">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="07beb-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07beb-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07beb-141">-WhatIf</span></span>
<span data-ttu-id="07beb-142">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="07beb-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="07beb-143">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="07beb-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07beb-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07beb-144">CommonParameters</span></span>
<span data-ttu-id="07beb-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="07beb-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07beb-146">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="07beb-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07beb-147">입력</span><span class="sxs-lookup"><span data-stu-id="07beb-147">INPUTS</span></span>

### <span data-ttu-id="07beb-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="07beb-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="07beb-149">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="07beb-149">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="07beb-150">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="07beb-150">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="07beb-151">System.String</span><span class="sxs-lookup"><span data-stu-id="07beb-151">System.String</span></span>

### <span data-ttu-id="07beb-152">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="07beb-152">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="07beb-153">System.Int32</span><span class="sxs-lookup"><span data-stu-id="07beb-153">System.Int32</span></span>

## <span data-ttu-id="07beb-154">출력</span><span class="sxs-lookup"><span data-stu-id="07beb-154">OUTPUTS</span></span>

### <span data-ttu-id="07beb-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="07beb-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="07beb-156">참고 사항</span><span class="sxs-lookup"><span data-stu-id="07beb-156">NOTES</span></span>

## <span data-ttu-id="07beb-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="07beb-157">RELATED LINKS</span></span>
