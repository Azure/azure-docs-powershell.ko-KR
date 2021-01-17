---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzImage.md
ms.openlocfilehash: b829321dc3d091549ff0b8a89a5ad564867db478
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489240"
---
# <span data-ttu-id="91c13-101">Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="91c13-101">Update-AzImage</span></span>

## <span data-ttu-id="91c13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91c13-102">SYNOPSIS</span></span>
<span data-ttu-id="91c13-103">이미지를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="91c13-103">Updates an image.</span></span>

## <span data-ttu-id="91c13-104">구문</span><span class="sxs-lookup"><span data-stu-id="91c13-104">SYNTAX</span></span>

### <span data-ttu-id="91c13-105">DefaultParameter(기본값)</span><span class="sxs-lookup"><span data-stu-id="91c13-105">DefaultParameter (Default)</span></span>
```
Update-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91c13-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="91c13-106">ResourceIdParameter</span></span>
```
Update-AzImage [-Tag <Hashtable>] [-AsJob] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91c13-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="91c13-107">ObjectParameter</span></span>
```
Update-AzImage [-Tag <Hashtable>] [-AsJob] [-Image] <PSImage> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91c13-108">설명</span><span class="sxs-lookup"><span data-stu-id="91c13-108">DESCRIPTION</span></span>
<span data-ttu-id="91c13-109">**Update-AzImage** cmdlet은 이미지를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="91c13-109">The **Update-AzImage** cmdlet updates an image.</span></span>
<span data-ttu-id="91c13-110">현재는 태그만 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91c13-110">Currently, only the Tags can be updated.</span></span>

## <span data-ttu-id="91c13-111">예제</span><span class="sxs-lookup"><span data-stu-id="91c13-111">EXAMPLES</span></span>

### <span data-ttu-id="91c13-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="91c13-112">Example 1</span></span>
```
PS C:\> $image = Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' 
PS C:\> $image.Tags = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\> $image.Tags.Add("key1", "val1")
PS C:\> Update-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Image $image
```

<span data-ttu-id="91c13-113">이 명령은 리소스 그룹 'ResourceGroup01'에서 기존 이미지 'Image01'의 태그 값을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="91c13-113">This command updates the Tag value of the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="91c13-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91c13-114">PARAMETERS</span></span>

### <span data-ttu-id="91c13-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="91c13-115">-AsJob</span></span>
<span data-ttu-id="91c13-116">백그라운드에서 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="91c13-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="91c13-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91c13-117">-DefaultProfile</span></span>
<span data-ttu-id="91c13-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="91c13-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91c13-119">-Image</span><span class="sxs-lookup"><span data-stu-id="91c13-119">-Image</span></span>
<span data-ttu-id="91c13-120">로컬 이미지 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="91c13-120">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: ObjectParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="91c13-121">-ImageName</span><span class="sxs-lookup"><span data-stu-id="91c13-121">-ImageName</span></span>
<span data-ttu-id="91c13-122">이미지의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="91c13-122">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91c13-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91c13-123">-ResourceGroupName</span></span>
<span data-ttu-id="91c13-124">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="91c13-124">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91c13-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="91c13-125">-ResourceId</span></span>
<span data-ttu-id="91c13-126">이미지의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="91c13-126">The resource Id for the image</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91c13-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="91c13-127">-Tag</span></span>
<span data-ttu-id="91c13-128">리소스 태그</span><span class="sxs-lookup"><span data-stu-id="91c13-128">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91c13-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="91c13-129">-Confirm</span></span>
<span data-ttu-id="91c13-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="91c13-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91c13-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91c13-131">-WhatIf</span></span>
<span data-ttu-id="91c13-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="91c13-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91c13-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="91c13-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91c13-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91c13-134">CommonParameters</span></span>
<span data-ttu-id="91c13-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="91c13-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91c13-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="91c13-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91c13-137">입력</span><span class="sxs-lookup"><span data-stu-id="91c13-137">INPUTS</span></span>

### <span data-ttu-id="91c13-138">System.String</span><span class="sxs-lookup"><span data-stu-id="91c13-138">System.String</span></span>

### <span data-ttu-id="91c13-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="91c13-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="91c13-140">출력</span><span class="sxs-lookup"><span data-stu-id="91c13-140">OUTPUTS</span></span>

### <span data-ttu-id="91c13-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="91c13-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="91c13-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="91c13-142">NOTES</span></span>

## <span data-ttu-id="91c13-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="91c13-143">RELATED LINKS</span></span>
