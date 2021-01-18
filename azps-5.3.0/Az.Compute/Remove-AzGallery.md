---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGallery.md
ms.openlocfilehash: 13964bf668533aa5c1bc09b9c4eaaab83c6c421e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98496010"
---
# <span data-ttu-id="ad356-101">Remove-AzGallery</span><span class="sxs-lookup"><span data-stu-id="ad356-101">Remove-AzGallery</span></span>

## <span data-ttu-id="ad356-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad356-102">SYNOPSIS</span></span>
<span data-ttu-id="ad356-103">갤러리를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="ad356-103">Delete a gallery.</span></span>

## <span data-ttu-id="ad356-104">구문</span><span class="sxs-lookup"><span data-stu-id="ad356-104">SYNTAX</span></span>

### <span data-ttu-id="ad356-105">DefaultParameter(기본값)</span><span class="sxs-lookup"><span data-stu-id="ad356-105">DefaultParameter (Default)</span></span>
```
Remove-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad356-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="ad356-106">ResourceIdParameter</span></span>
```
Remove-AzGallery [-Force] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad356-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="ad356-107">ObjectParameter</span></span>
```
Remove-AzGallery [-Force] [-InputObject] <PSGallery> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad356-108">설명</span><span class="sxs-lookup"><span data-stu-id="ad356-108">DESCRIPTION</span></span>
<span data-ttu-id="ad356-109">갤러리를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="ad356-109">Delete a gallery.</span></span>

## <span data-ttu-id="ad356-110">예제</span><span class="sxs-lookup"><span data-stu-id="ad356-110">EXAMPLES</span></span>

### <span data-ttu-id="ad356-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="ad356-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGallery -ResourceGroupName $rgname -GalleryName $galleryName
```

<span data-ttu-id="ad356-112">주어진 갤러리를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="ad356-112">Delete the given gallery.</span></span>

## <span data-ttu-id="ad356-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad356-113">PARAMETERS</span></span>

### <span data-ttu-id="ad356-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ad356-114">-AsJob</span></span>
<span data-ttu-id="ad356-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="ad356-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ad356-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad356-116">-DefaultProfile</span></span>
<span data-ttu-id="ad356-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ad356-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad356-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ad356-118">-Force</span></span>
<span data-ttu-id="ad356-119">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="ad356-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ad356-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad356-120">-InputObject</span></span>
<span data-ttu-id="ad356-121">PS 갤러리 개체</span><span class="sxs-lookup"><span data-stu-id="ad356-121">The PS Gallery Object</span></span>

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

### <span data-ttu-id="ad356-122">-Name</span><span class="sxs-lookup"><span data-stu-id="ad356-122">-Name</span></span>
<span data-ttu-id="ad356-123">갤러리의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ad356-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="ad356-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad356-124">-ResourceGroupName</span></span>
<span data-ttu-id="ad356-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ad356-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="ad356-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad356-126">-ResourceId</span></span>
<span data-ttu-id="ad356-127">갤러리의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="ad356-127">The resource Id for the gallery</span></span>

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

### <span data-ttu-id="ad356-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ad356-128">-Confirm</span></span>
<span data-ttu-id="ad356-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ad356-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad356-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad356-130">-WhatIf</span></span>
<span data-ttu-id="ad356-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ad356-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad356-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ad356-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad356-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad356-133">CommonParameters</span></span>
<span data-ttu-id="ad356-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ad356-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad356-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ad356-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad356-136">입력</span><span class="sxs-lookup"><span data-stu-id="ad356-136">INPUTS</span></span>

### <span data-ttu-id="ad356-137">System.String</span><span class="sxs-lookup"><span data-stu-id="ad356-137">System.String</span></span>

### <span data-ttu-id="ad356-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span><span class="sxs-lookup"><span data-stu-id="ad356-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="ad356-139">출력</span><span class="sxs-lookup"><span data-stu-id="ad356-139">OUTPUTS</span></span>

### <span data-ttu-id="ad356-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="ad356-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="ad356-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ad356-141">NOTES</span></span>

## <span data-ttu-id="ad356-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ad356-142">RELATED LINKS</span></span>
