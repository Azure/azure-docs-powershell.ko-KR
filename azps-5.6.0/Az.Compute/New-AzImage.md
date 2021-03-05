---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImage.md
ms.openlocfilehash: 77a4879d403b52a828460bcfec5666b7071dcea9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959664"
---
# <span data-ttu-id="5b34d-101">New-AzImage</span><span class="sxs-lookup"><span data-stu-id="5b34d-101">New-AzImage</span></span>

## <span data-ttu-id="5b34d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b34d-102">SYNOPSIS</span></span>
<span data-ttu-id="5b34d-103">이미지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b34d-103">Creates an image.</span></span>

## <span data-ttu-id="5b34d-104">구문</span><span class="sxs-lookup"><span data-stu-id="5b34d-104">SYNTAX</span></span>

```
New-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <PSImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b34d-105">설명</span><span class="sxs-lookup"><span data-stu-id="5b34d-105">DESCRIPTION</span></span>
<span data-ttu-id="5b34d-106">**New-AzImage** cmdlet은 이미지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b34d-106">The **New-AzImage** cmdlet creates an image.</span></span>

## <span data-ttu-id="5b34d-107">예제</span><span class="sxs-lookup"><span data-stu-id="5b34d-107">EXAMPLES</span></span>

### <span data-ttu-id="5b34d-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="5b34d-108">Example 1</span></span>
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

<span data-ttu-id="5b34d-109">첫 번째 명령은 이미지 개체를 만든 다음, $imageConfig 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="5b34d-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="5b34d-110">다음 세 가지 명령은 os 디스크의 경로와 두 개의 데이터 디스크를 $osDiskVhdUri, $dataDiskVhdUri 1 및 $dataDiskVhdUri 2 변수에 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="5b34d-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="5b34d-111">이 방법은 다음 명령의 가독성을 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="5b34d-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="5b34d-112">다음 세 가지 명령은 각각 os 디스크와 두 개의 데이터 디스크를 저장한 이미지에 $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="5b34d-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="5b34d-113">각 디스크의 URI는 $osDiskVhdUri, $dataDiskVhdUri 1 및 $dataDiskVhdUri 2에 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b34d-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="5b34d-114">마지막 명령은 리소스 그룹 'ResourceGroup01'에서 'ImageName01'이라는 이미지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b34d-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="5b34d-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="5b34d-115">PARAMETERS</span></span>

### <span data-ttu-id="5b34d-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5b34d-116">-AsJob</span></span>
<span data-ttu-id="5b34d-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="5b34d-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5b34d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b34d-118">-DefaultProfile</span></span>
<span data-ttu-id="5b34d-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5b34d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b34d-120">-Image</span><span class="sxs-lookup"><span data-stu-id="5b34d-120">-Image</span></span>
<span data-ttu-id="5b34d-121">로컬 이미지 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5b34d-121">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b34d-122">-ImageName</span><span class="sxs-lookup"><span data-stu-id="5b34d-122">-ImageName</span></span>
<span data-ttu-id="5b34d-123">이미지의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5b34d-123">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b34d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b34d-124">-ResourceGroupName</span></span>
<span data-ttu-id="5b34d-125">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5b34d-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b34d-126">-확인</span><span class="sxs-lookup"><span data-stu-id="5b34d-126">-Confirm</span></span>
<span data-ttu-id="5b34d-127">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b34d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b34d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b34d-128">-WhatIf</span></span>
<span data-ttu-id="5b34d-129">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="5b34d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b34d-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5b34d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b34d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b34d-131">CommonParameters</span></span>
<span data-ttu-id="5b34d-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5b34d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b34d-133">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5b34d-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b34d-134">입력</span><span class="sxs-lookup"><span data-stu-id="5b34d-134">INPUTS</span></span>

### <span data-ttu-id="5b34d-135">System.String</span><span class="sxs-lookup"><span data-stu-id="5b34d-135">System.String</span></span>

### <span data-ttu-id="5b34d-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="5b34d-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="5b34d-137">출력</span><span class="sxs-lookup"><span data-stu-id="5b34d-137">OUTPUTS</span></span>

### <span data-ttu-id="5b34d-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="5b34d-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="5b34d-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5b34d-139">NOTES</span></span>

## <span data-ttu-id="5b34d-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5b34d-140">RELATED LINKS</span></span>
