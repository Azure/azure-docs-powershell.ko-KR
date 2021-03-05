---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azimageconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImageConfig.md
ms.openlocfilehash: de59e8a9dc2fdcc4fa29409eaffc7f82e7d57b52
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977520"
---
# <span data-ttu-id="f381f-101">New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="f381f-101">New-AzImageConfig</span></span>

## <span data-ttu-id="f381f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f381f-102">SYNOPSIS</span></span>
<span data-ttu-id="f381f-103">구성 가능한 이미지 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f381f-103">Creates a configurable image object.</span></span>

## <span data-ttu-id="f381f-104">구문</span><span class="sxs-lookup"><span data-stu-id="f381f-104">SYNTAX</span></span>

```
New-AzImageConfig [[-Location] <String>] [[-Tag] <Hashtable>] [[-SourceVirtualMachineId] <String>]
 [[-OsDisk] <ImageOSDisk>] [-HyperVGeneration <String>] [-DataDisk <ImageDataDisk[]>] [-ZoneResilient]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f381f-105">설명</span><span class="sxs-lookup"><span data-stu-id="f381f-105">DESCRIPTION</span></span>
<span data-ttu-id="f381f-106">**New-AzImageConfig** cmdlet은 구성 가능한 이미지 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f381f-106">The **New-AzImageConfig** cmdlet creates a configurable image object.</span></span>

## <span data-ttu-id="f381f-107">예제</span><span class="sxs-lookup"><span data-stu-id="f381f-107">EXAMPLES</span></span>

### <span data-ttu-id="f381f-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="f381f-108">Example 1</span></span>
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

<span data-ttu-id="f381f-109">첫 번째 명령은 이미지 개체를 만든 다음, $imageConfig 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="f381f-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="f381f-110">다음 세 가지 명령은 os 디스크의 경로와 두 개의 데이터 디스크를 $osDiskVhdUri, $dataDiskVhdUri 1 및 $dataDiskVhdUri 2 변수에 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="f381f-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span> <span data-ttu-id="f381f-111">이 방법은 다음 명령의 가독성을 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="f381f-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="f381f-112">다음 세 가지 명령은 각각 os 디스크와 두 개의 데이터 디스크를 저장한 이미지에 $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="f381f-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="f381f-113">각 디스크의 URI는 $osDiskVhdUri, $dataDiskVhdUri 1 및 $dataDiskVhdUri 2에 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="f381f-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="f381f-114">마지막 명령은 리소스 그룹 'ResourceGroup01'에서 'ImageName01'이라는 이미지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f381f-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="f381f-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f381f-115">PARAMETERS</span></span>

### <span data-ttu-id="f381f-116">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="f381f-116">-DataDisk</span></span>
<span data-ttu-id="f381f-117">데이터 디스크 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f381f-117">Specifies the data disk object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ImageDataDisk[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f381f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f381f-118">-DefaultProfile</span></span>
<span data-ttu-id="f381f-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f381f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f381f-120">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="f381f-120">-HyperVGeneration</span></span>
<span data-ttu-id="f381f-121">이미지에서 만든 가상 머신에 대한 HyperVGeneration 형식을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f381f-121">Specifies the HyperVGeneration Type for the virtual machine created from the image.</span></span>  <span data-ttu-id="f381f-122">허용되는 값은 V1 및 V2입니다.</span><span class="sxs-lookup"><span data-stu-id="f381f-122">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="f381f-123">-Location</span><span class="sxs-lookup"><span data-stu-id="f381f-123">-Location</span></span>
<span data-ttu-id="f381f-124">위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f381f-124">Specifies a location.</span></span>

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

### <span data-ttu-id="f381f-125">-OsDisk</span><span class="sxs-lookup"><span data-stu-id="f381f-125">-OsDisk</span></span>
<span data-ttu-id="f381f-126">운영 체제 디스크를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f381f-126">Specifies the operating system Disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ImageOSDisk
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f381f-127">-SourceVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="f381f-127">-SourceVirtualMachineId</span></span>
<span data-ttu-id="f381f-128">원본 가상 머신 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f381f-128">Specifies the source virtual machine ID.</span></span>

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

### <span data-ttu-id="f381f-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="f381f-129">-Tag</span></span>
<span data-ttu-id="f381f-130">해시 테이블의 형태로 키 값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="f381f-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f381f-131">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="f381f-131">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f381f-132">-ZoneResilient</span><span class="sxs-lookup"><span data-stu-id="f381f-132">-ZoneResilient</span></span>
<span data-ttu-id="f381f-133">영역 탄력적 사용</span><span class="sxs-lookup"><span data-stu-id="f381f-133">Enable zone resilient</span></span>

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

### <span data-ttu-id="f381f-134">-확인</span><span class="sxs-lookup"><span data-stu-id="f381f-134">-Confirm</span></span>
<span data-ttu-id="f381f-135">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f381f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f381f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f381f-136">-WhatIf</span></span>
<span data-ttu-id="f381f-137">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="f381f-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f381f-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f381f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f381f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f381f-139">CommonParameters</span></span>
<span data-ttu-id="f381f-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f381f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f381f-141">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f381f-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f381f-142">입력</span><span class="sxs-lookup"><span data-stu-id="f381f-142">INPUTS</span></span>

### <span data-ttu-id="f381f-143">System.String</span><span class="sxs-lookup"><span data-stu-id="f381f-143">System.String</span></span>

### <span data-ttu-id="f381f-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="f381f-144">System.Collections.Hashtable</span></span>

### <span data-ttu-id="f381f-145">Microsoft.Azure.Management.Compute.Models.ImageOSDisk</span><span class="sxs-lookup"><span data-stu-id="f381f-145">Microsoft.Azure.Management.Compute.Models.ImageOSDisk</span></span>

### <span data-ttu-id="f381f-146">Microsoft.Azure.Management.Compute.Models.ImageDataDisk[]</span><span class="sxs-lookup"><span data-stu-id="f381f-146">Microsoft.Azure.Management.Compute.Models.ImageDataDisk[]</span></span>

## <span data-ttu-id="f381f-147">출력</span><span class="sxs-lookup"><span data-stu-id="f381f-147">OUTPUTS</span></span>

### <span data-ttu-id="f381f-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="f381f-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="f381f-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f381f-149">NOTES</span></span>

## <span data-ttu-id="f381f-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f381f-150">RELATED LINKS</span></span>
