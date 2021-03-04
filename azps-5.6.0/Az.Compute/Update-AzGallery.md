---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/update-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGallery.md
ms.openlocfilehash: 4badbfc9973b20869c6db421bd1299e00337d7fa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990416"
---
# <span data-ttu-id="203cb-101">Update-AzGallery</span><span class="sxs-lookup"><span data-stu-id="203cb-101">Update-AzGallery</span></span>

## <span data-ttu-id="203cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="203cb-102">SYNOPSIS</span></span>
<span data-ttu-id="203cb-103">갤러리를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="203cb-103">Update a gallery.</span></span>

## <span data-ttu-id="203cb-104">구문</span><span class="sxs-lookup"><span data-stu-id="203cb-104">SYNTAX</span></span>

### <span data-ttu-id="203cb-105">DefaultParameter(기본값)</span><span class="sxs-lookup"><span data-stu-id="203cb-105">DefaultParameter (Default)</span></span>
```
Update-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Description <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="203cb-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="203cb-106">ResourceIdParameter</span></span>
```
Update-AzGallery [-ResourceId] <String> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="203cb-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="203cb-107">ObjectParameter</span></span>
```
Update-AzGallery [-InputObject] <PSGallery> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="203cb-108">설명</span><span class="sxs-lookup"><span data-stu-id="203cb-108">DESCRIPTION</span></span>
<span data-ttu-id="203cb-109">갤러리를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="203cb-109">Update a gallery.</span></span>

## <span data-ttu-id="203cb-110">예제</span><span class="sxs-lookup"><span data-stu-id="203cb-110">EXAMPLES</span></span>

### <span data-ttu-id="203cb-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="203cb-111">Example 1</span></span>
```powershell
PS C:\> Update-AzGallery -ResourceGroupName $rgname -Name $galleryName -Description $galleryDescription
```

<span data-ttu-id="203cb-112">갤러리를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="203cb-112">Update a gallery.</span></span>

## <span data-ttu-id="203cb-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="203cb-113">PARAMETERS</span></span>

### <span data-ttu-id="203cb-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="203cb-114">-AsJob</span></span>
<span data-ttu-id="203cb-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="203cb-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="203cb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="203cb-116">-DefaultProfile</span></span>
<span data-ttu-id="203cb-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="203cb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="203cb-118">-Description</span><span class="sxs-lookup"><span data-stu-id="203cb-118">-Description</span></span>
<span data-ttu-id="203cb-119">갤러리 리소스에 대한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="203cb-119">The description of the gallery resource.</span></span>

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

### <span data-ttu-id="203cb-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="203cb-120">-InputObject</span></span>
<span data-ttu-id="203cb-121">PS 갤러리 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="203cb-121">The PS Gallery Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery
Parameter Sets: ObjectParameter
Aliases: Gallery

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="203cb-122">-Name</span><span class="sxs-lookup"><span data-stu-id="203cb-122">-Name</span></span>
<span data-ttu-id="203cb-123">갤러리의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="203cb-123">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="203cb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="203cb-124">-ResourceGroupName</span></span>
<span data-ttu-id="203cb-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="203cb-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="203cb-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="203cb-126">-ResourceId</span></span>
<span data-ttu-id="203cb-127">갤러리에 대한 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="203cb-127">The resource Id for the gallery</span></span>

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

### <span data-ttu-id="203cb-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="203cb-128">-Tag</span></span>
<span data-ttu-id="203cb-129">리소스 태그</span><span class="sxs-lookup"><span data-stu-id="203cb-129">Resource tags</span></span>

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

### <span data-ttu-id="203cb-130">-확인</span><span class="sxs-lookup"><span data-stu-id="203cb-130">-Confirm</span></span>
<span data-ttu-id="203cb-131">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="203cb-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="203cb-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="203cb-132">-WhatIf</span></span>
<span data-ttu-id="203cb-133">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="203cb-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="203cb-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="203cb-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="203cb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="203cb-135">CommonParameters</span></span>
<span data-ttu-id="203cb-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="203cb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="203cb-137">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="203cb-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="203cb-138">입력</span><span class="sxs-lookup"><span data-stu-id="203cb-138">INPUTS</span></span>

### <span data-ttu-id="203cb-139">System.String</span><span class="sxs-lookup"><span data-stu-id="203cb-139">System.String</span></span>

### <span data-ttu-id="203cb-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span><span class="sxs-lookup"><span data-stu-id="203cb-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

### <span data-ttu-id="203cb-141">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="203cb-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="203cb-142">출력</span><span class="sxs-lookup"><span data-stu-id="203cb-142">OUTPUTS</span></span>

### <span data-ttu-id="203cb-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span><span class="sxs-lookup"><span data-stu-id="203cb-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="203cb-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="203cb-144">NOTES</span></span>

## <span data-ttu-id="203cb-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="203cb-145">RELATED LINKS</span></span>
