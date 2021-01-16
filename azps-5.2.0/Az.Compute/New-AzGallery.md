---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGallery.md
ms.openlocfilehash: d1a25b3e8466c691272f4c556fe728cbce47a718
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356006"
---
# <span data-ttu-id="42763-101">New-AzGallery</span><span class="sxs-lookup"><span data-stu-id="42763-101">New-AzGallery</span></span>

## <span data-ttu-id="42763-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42763-102">SYNOPSIS</span></span>
<span data-ttu-id="42763-103">갤러리를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42763-103">Create a gallery.</span></span>

## <span data-ttu-id="42763-104">구문</span><span class="sxs-lookup"><span data-stu-id="42763-104">SYNTAX</span></span>

```
New-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Location] <String>
 [-Description <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="42763-105">설명</span><span class="sxs-lookup"><span data-stu-id="42763-105">DESCRIPTION</span></span>
<span data-ttu-id="42763-106">갤러리를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42763-106">Create a gallery.</span></span>

## <span data-ttu-id="42763-107">예제</span><span class="sxs-lookup"><span data-stu-id="42763-107">EXAMPLES</span></span>

### <span data-ttu-id="42763-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="42763-108">Example 1</span></span>
```powershell
PS C:\> New-AzGallery -ResourceGroupName $rgname -Name $galleryName -Location $location -Description $galleryDescription
```

<span data-ttu-id="42763-109">갤러리를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42763-109">Create a gallery.</span></span>

## <span data-ttu-id="42763-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="42763-110">PARAMETERS</span></span>

### <span data-ttu-id="42763-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="42763-111">-AsJob</span></span>
<span data-ttu-id="42763-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="42763-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="42763-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42763-113">-DefaultProfile</span></span>
<span data-ttu-id="42763-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="42763-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42763-115">-Description</span><span class="sxs-lookup"><span data-stu-id="42763-115">-Description</span></span>
<span data-ttu-id="42763-116">갤러리 리소스에 대한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="42763-116">The description of the gallery resource.</span></span>

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

### <span data-ttu-id="42763-117">-Location</span><span class="sxs-lookup"><span data-stu-id="42763-117">-Location</span></span>
<span data-ttu-id="42763-118">리소스 위치</span><span class="sxs-lookup"><span data-stu-id="42763-118">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42763-119">-Name</span><span class="sxs-lookup"><span data-stu-id="42763-119">-Name</span></span>
<span data-ttu-id="42763-120">갤러리의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="42763-120">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: GalleryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42763-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42763-121">-ResourceGroupName</span></span>
<span data-ttu-id="42763-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="42763-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="42763-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="42763-123">-Tag</span></span>
<span data-ttu-id="42763-124">리소스 태그</span><span class="sxs-lookup"><span data-stu-id="42763-124">Resource tags</span></span>

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

### <span data-ttu-id="42763-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="42763-125">-Confirm</span></span>
<span data-ttu-id="42763-126">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="42763-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42763-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42763-127">-WhatIf</span></span>
<span data-ttu-id="42763-128">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="42763-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42763-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="42763-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42763-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42763-130">CommonParameters</span></span>
<span data-ttu-id="42763-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="42763-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42763-132">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="42763-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42763-133">입력</span><span class="sxs-lookup"><span data-stu-id="42763-133">INPUTS</span></span>

### <span data-ttu-id="42763-134">System.String</span><span class="sxs-lookup"><span data-stu-id="42763-134">System.String</span></span>

### <span data-ttu-id="42763-135">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="42763-135">System.Collections.Hashtable</span></span>

## <span data-ttu-id="42763-136">출력</span><span class="sxs-lookup"><span data-stu-id="42763-136">OUTPUTS</span></span>

### <span data-ttu-id="42763-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span><span class="sxs-lookup"><span data-stu-id="42763-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="42763-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="42763-138">NOTES</span></span>

## <span data-ttu-id="42763-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="42763-139">RELATED LINKS</span></span>
