---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azimageconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImageConfig.md
ms.openlocfilehash: 56834ad267b4ac60613afc4dbd08499eae212512
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493837"
---
# <span data-ttu-id="4ce81-101">New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="4ce81-101">New-AzImageConfig</span></span>

## <span data-ttu-id="4ce81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ce81-102">SYNOPSIS</span></span>
<span data-ttu-id="4ce81-103">구성 가능한 이미지 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4ce81-103">Creates a configurable image object.</span></span>

## <span data-ttu-id="4ce81-104">구문</span><span class="sxs-lookup"><span data-stu-id="4ce81-104">SYNTAX</span></span>

```
New-AzImageConfig [[-Location] <String>] [[-Tag] <Hashtable>] [[-SourceVirtualMachineId] <String>]
 [[-OsDisk] <ImageOSDisk>] [-HyperVGeneration <String>] [-DataDisk <ImageDataDisk[]>] [-ZoneResilient]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ce81-105">설명</span><span class="sxs-lookup"><span data-stu-id="4ce81-105">DESCRIPTION</span></span>
<span data-ttu-id="4ce81-106">**New-AzImageConfig** cmdlet은 구성 가능한 이미지 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4ce81-106">The **New-AzImageConfig** cmdlet creates a configurable image object.</span></span>

## <span data-ttu-id="4ce81-107">예제</span><span class="sxs-lookup"><span data-stu-id="4ce81-107">EXAMPLES</span></span>

### <span data-ttu-id="4ce81-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="4ce81-108">Example 1</span></span>
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

<span data-ttu-id="4ce81-109">첫 번째 명령은 이미지 개체를 만든 다음 이미지 $imageConfig 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="4ce81-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="4ce81-110">다음 세 명령은 os 디스크의 경로와 두 개의 데이터 디스크를 $osDiskVhdUri, $dataDiskVhdUri 1 및 $dataDiskVhdUri 2 변수에 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="4ce81-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span> <span data-ttu-id="4ce81-111">이 방법은 다음 명령의 가독성에만 해당됩니다.</span><span class="sxs-lookup"><span data-stu-id="4ce81-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="4ce81-112">다음 세 명령은 각각 os 디스크와 2개의 데이터 디스크를 각 디스크에 저장된 이미지에 $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="4ce81-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="4ce81-113">각 디스크의 URI는 $osDiskVhdUri, $dataDiskVhdUri 1 및 $dataDiskVhdUri 2에 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="4ce81-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="4ce81-114">마지막 명령은 리소스 그룹 'ResourceGroup01'에 'ImageName01'이라는 이미지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4ce81-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="4ce81-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ce81-115">PARAMETERS</span></span>

### <span data-ttu-id="4ce81-116">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="4ce81-116">-DataDisk</span></span>
<span data-ttu-id="4ce81-117">데이터 디스크 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ce81-117">Specifies the data disk object.</span></span>

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

### <span data-ttu-id="4ce81-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ce81-118">-DefaultProfile</span></span>
<span data-ttu-id="4ce81-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4ce81-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ce81-120">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="4ce81-120">-HyperVGeneration</span></span>
<span data-ttu-id="4ce81-121">이미지에서 만든 가상 머신에 대한 HyperVGeneration 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ce81-121">Specifies the HyperVGeneration Type for the virtual machine created from the image.</span></span>  <span data-ttu-id="4ce81-122">허용되는 값은 V1 및 V2입니다.</span><span class="sxs-lookup"><span data-stu-id="4ce81-122">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="4ce81-123">-Location</span><span class="sxs-lookup"><span data-stu-id="4ce81-123">-Location</span></span>
<span data-ttu-id="4ce81-124">위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ce81-124">Specifies a location.</span></span>

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

### <span data-ttu-id="4ce81-125">-OsDisk</span><span class="sxs-lookup"><span data-stu-id="4ce81-125">-OsDisk</span></span>
<span data-ttu-id="4ce81-126">운영 체제 디스크를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ce81-126">Specifies the operating system Disk.</span></span>

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

### <span data-ttu-id="4ce81-127">-SourceVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="4ce81-127">-SourceVirtualMachineId</span></span>
<span data-ttu-id="4ce81-128">원본 가상 머신 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ce81-128">Specifies the source virtual machine ID.</span></span>

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

### <span data-ttu-id="4ce81-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="4ce81-129">-Tag</span></span>
<span data-ttu-id="4ce81-130">해시 테이블 형식의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="4ce81-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4ce81-131">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="4ce81-131">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="4ce81-132">-ZoneResilient</span><span class="sxs-lookup"><span data-stu-id="4ce81-132">-ZoneResilient</span></span>
<span data-ttu-id="4ce81-133">영역 탄력적 사용</span><span class="sxs-lookup"><span data-stu-id="4ce81-133">Enable zone resilient</span></span>

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

### <span data-ttu-id="4ce81-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4ce81-134">-Confirm</span></span>
<span data-ttu-id="4ce81-135">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4ce81-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ce81-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ce81-136">-WhatIf</span></span>
<span data-ttu-id="4ce81-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="4ce81-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4ce81-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4ce81-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ce81-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ce81-139">CommonParameters</span></span>
<span data-ttu-id="4ce81-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4ce81-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ce81-141">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4ce81-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ce81-142">입력</span><span class="sxs-lookup"><span data-stu-id="4ce81-142">INPUTS</span></span>

### <span data-ttu-id="4ce81-143">System.String</span><span class="sxs-lookup"><span data-stu-id="4ce81-143">System.String</span></span>

### <span data-ttu-id="4ce81-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="4ce81-144">System.Collections.Hashtable</span></span>

### <span data-ttu-id="4ce81-145">Microsoft.Azure.Management.Compute.Models.ImageOSDisk</span><span class="sxs-lookup"><span data-stu-id="4ce81-145">Microsoft.Azure.Management.Compute.Models.ImageOSDisk</span></span>

### <span data-ttu-id="4ce81-146">Microsoft.Azure.Management.Compute.Models.ImageDataDisk[]</span><span class="sxs-lookup"><span data-stu-id="4ce81-146">Microsoft.Azure.Management.Compute.Models.ImageDataDisk[]</span></span>

## <span data-ttu-id="4ce81-147">출력</span><span class="sxs-lookup"><span data-stu-id="4ce81-147">OUTPUTS</span></span>

### <span data-ttu-id="4ce81-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="4ce81-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="4ce81-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4ce81-149">NOTES</span></span>

## <span data-ttu-id="4ce81-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4ce81-150">RELATED LINKS</span></span>
