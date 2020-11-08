---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azimageconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImageConfig.md
ms.openlocfilehash: 56834ad267b4ac60613afc4dbd08499eae212512
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217062"
---
# <span data-ttu-id="93e16-101">New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="93e16-101">New-AzImageConfig</span></span>

## <span data-ttu-id="93e16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93e16-102">SYNOPSIS</span></span>
<span data-ttu-id="93e16-103">구성 가능한 image 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="93e16-103">Creates a configurable image object.</span></span>

## <span data-ttu-id="93e16-104">구문과</span><span class="sxs-lookup"><span data-stu-id="93e16-104">SYNTAX</span></span>

```
New-AzImageConfig [[-Location] <String>] [[-Tag] <Hashtable>] [[-SourceVirtualMachineId] <String>]
 [[-OsDisk] <ImageOSDisk>] [-HyperVGeneration <String>] [-DataDisk <ImageDataDisk[]>] [-ZoneResilient]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93e16-105">설명은</span><span class="sxs-lookup"><span data-stu-id="93e16-105">DESCRIPTION</span></span>
<span data-ttu-id="93e16-106">**AzImageConfig** cmdlet은 구성 가능한 image 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="93e16-106">The **New-AzImageConfig** cmdlet creates a configurable image object.</span></span>

## <span data-ttu-id="93e16-107">예제의</span><span class="sxs-lookup"><span data-stu-id="93e16-107">EXAMPLES</span></span>

### <span data-ttu-id="93e16-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="93e16-108">Example 1</span></span>
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

<span data-ttu-id="93e16-109">첫 번째 명령은 image 개체를 만든 다음 $imageConfig 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="93e16-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="93e16-110">다음 세 개의 명령은 os 디스크의 경로와 두 개의 데이터 디스크를 $osDiskVhdUri, $dataDiskVhdUri 1 및 $dataDiskVhdUri 2 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="93e16-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span> <span data-ttu-id="93e16-111">이 방법은 다음 명령에 대 한 읽기 전용입니다.</span><span class="sxs-lookup"><span data-stu-id="93e16-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="93e16-112">다음 세 개의 명령은 각각 os 디스크와 두 개의 데이터 디스크를 $imageConfig에 저장 된 이미지에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="93e16-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="93e16-113">각 디스크의 URI는 $osDiskVhdUri, $dataDiskVhdUri 1 및 $dataDiskVhdUri 2에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="93e16-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="93e16-114">마지막 명령은 리소스 그룹 ' ResourceGroup01 '에 ' ImageName01 ' 이미지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="93e16-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="93e16-115">변수</span><span class="sxs-lookup"><span data-stu-id="93e16-115">PARAMETERS</span></span>

### <span data-ttu-id="93e16-116">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="93e16-116">-DataDisk</span></span>
<span data-ttu-id="93e16-117">데이터 디스크 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="93e16-117">Specifies the data disk object.</span></span>

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

### <span data-ttu-id="93e16-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93e16-118">-DefaultProfile</span></span>
<span data-ttu-id="93e16-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="93e16-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93e16-120">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="93e16-120">-HyperVGeneration</span></span>
<span data-ttu-id="93e16-121">이미지에서 만든 가상 컴퓨터에 대 한 HyperVGeneration 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="93e16-121">Specifies the HyperVGeneration Type for the virtual machine created from the image.</span></span>  <span data-ttu-id="93e16-122">허용 되는 값은 V1 및 V2입니다.</span><span class="sxs-lookup"><span data-stu-id="93e16-122">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="93e16-123">-위치</span><span class="sxs-lookup"><span data-stu-id="93e16-123">-Location</span></span>
<span data-ttu-id="93e16-124">위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="93e16-124">Specifies a location.</span></span>

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

### <span data-ttu-id="93e16-125">-OsDisk</span><span class="sxs-lookup"><span data-stu-id="93e16-125">-OsDisk</span></span>
<span data-ttu-id="93e16-126">운영 체제 디스크를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="93e16-126">Specifies the operating system Disk.</span></span>

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

### <span data-ttu-id="93e16-127">-SourceVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="93e16-127">-SourceVirtualMachineId</span></span>
<span data-ttu-id="93e16-128">원본 가상 컴퓨터 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="93e16-128">Specifies the source virtual machine ID.</span></span>

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

### <span data-ttu-id="93e16-129">태그</span><span class="sxs-lookup"><span data-stu-id="93e16-129">-Tag</span></span>
<span data-ttu-id="93e16-130">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="93e16-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="93e16-131">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="93e16-131">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="93e16-132">-ZoneResilient</span><span class="sxs-lookup"><span data-stu-id="93e16-132">-ZoneResilient</span></span>
<span data-ttu-id="93e16-133">영역 탄성 사용</span><span class="sxs-lookup"><span data-stu-id="93e16-133">Enable zone resilient</span></span>

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

### <span data-ttu-id="93e16-134">-확인</span><span class="sxs-lookup"><span data-stu-id="93e16-134">-Confirm</span></span>
<span data-ttu-id="93e16-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="93e16-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93e16-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93e16-136">-WhatIf</span></span>
<span data-ttu-id="93e16-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="93e16-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="93e16-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="93e16-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93e16-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93e16-139">CommonParameters</span></span>
<span data-ttu-id="93e16-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="93e16-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93e16-141">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="93e16-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93e16-142">입력</span><span class="sxs-lookup"><span data-stu-id="93e16-142">INPUTS</span></span>

### <span data-ttu-id="93e16-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="93e16-143">System.String</span></span>

### <span data-ttu-id="93e16-144">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="93e16-144">System.Collections.Hashtable</span></span>

### <span data-ttu-id="93e16-145">ImageOSDisk를 통해 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="93e16-145">Microsoft.Azure.Management.Compute.Models.ImageOSDisk</span></span>

### <span data-ttu-id="93e16-146">Microsoft. g. ImageDataDisk []</span><span class="sxs-lookup"><span data-stu-id="93e16-146">Microsoft.Azure.Management.Compute.Models.ImageDataDisk[]</span></span>

## <span data-ttu-id="93e16-147">출력</span><span class="sxs-lookup"><span data-stu-id="93e16-147">OUTPUTS</span></span>

### <span data-ttu-id="93e16-148">PSImage의. m a.</span><span class="sxs-lookup"><span data-stu-id="93e16-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="93e16-149">상속자</span><span class="sxs-lookup"><span data-stu-id="93e16-149">NOTES</span></span>

## <span data-ttu-id="93e16-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="93e16-150">RELATED LINKS</span></span>
