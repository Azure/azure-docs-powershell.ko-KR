---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGallery.md
ms.openlocfilehash: d1a25b3e8466c691272f4c556fe728cbce47a718
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034927"
---
# <span data-ttu-id="2d84c-101">New-AzGallery</span><span class="sxs-lookup"><span data-stu-id="2d84c-101">New-AzGallery</span></span>

## <span data-ttu-id="2d84c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d84c-102">SYNOPSIS</span></span>
<span data-ttu-id="2d84c-103">갤러리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2d84c-103">Create a gallery.</span></span>

## <span data-ttu-id="2d84c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2d84c-104">SYNTAX</span></span>

```
New-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Location] <String>
 [-Description <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2d84c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2d84c-105">DESCRIPTION</span></span>
<span data-ttu-id="2d84c-106">갤러리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2d84c-106">Create a gallery.</span></span>

## <span data-ttu-id="2d84c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2d84c-107">EXAMPLES</span></span>

### <span data-ttu-id="2d84c-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="2d84c-108">Example 1</span></span>
```powershell
PS C:\> New-AzGallery -ResourceGroupName $rgname -Name $galleryName -Location $location -Description $galleryDescription
```

<span data-ttu-id="2d84c-109">갤러리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2d84c-109">Create a gallery.</span></span>

## <span data-ttu-id="2d84c-110">변수</span><span class="sxs-lookup"><span data-stu-id="2d84c-110">PARAMETERS</span></span>

### <span data-ttu-id="2d84c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2d84c-111">-AsJob</span></span>
<span data-ttu-id="2d84c-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="2d84c-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2d84c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d84c-113">-DefaultProfile</span></span>
<span data-ttu-id="2d84c-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2d84c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d84c-115">-설명</span><span class="sxs-lookup"><span data-stu-id="2d84c-115">-Description</span></span>
<span data-ttu-id="2d84c-116">갤러리 리소스에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="2d84c-116">The description of the gallery resource.</span></span>

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

### <span data-ttu-id="2d84c-117">-위치</span><span class="sxs-lookup"><span data-stu-id="2d84c-117">-Location</span></span>
<span data-ttu-id="2d84c-118">리소스 위치</span><span class="sxs-lookup"><span data-stu-id="2d84c-118">Resource location</span></span>

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

### <span data-ttu-id="2d84c-119">-이름</span><span class="sxs-lookup"><span data-stu-id="2d84c-119">-Name</span></span>
<span data-ttu-id="2d84c-120">갤러리의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2d84c-120">The name of the gallery.</span></span>

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

### <span data-ttu-id="2d84c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d84c-121">-ResourceGroupName</span></span>
<span data-ttu-id="2d84c-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2d84c-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="2d84c-123">태그</span><span class="sxs-lookup"><span data-stu-id="2d84c-123">-Tag</span></span>
<span data-ttu-id="2d84c-124">리소스 태그</span><span class="sxs-lookup"><span data-stu-id="2d84c-124">Resource tags</span></span>

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

### <span data-ttu-id="2d84c-125">-확인</span><span class="sxs-lookup"><span data-stu-id="2d84c-125">-Confirm</span></span>
<span data-ttu-id="2d84c-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d84c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d84c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d84c-127">-WhatIf</span></span>
<span data-ttu-id="2d84c-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2d84c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d84c-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2d84c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d84c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d84c-130">CommonParameters</span></span>
<span data-ttu-id="2d84c-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d84c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d84c-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2d84c-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d84c-133">입력</span><span class="sxs-lookup"><span data-stu-id="2d84c-133">INPUTS</span></span>

### <span data-ttu-id="2d84c-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2d84c-134">System.String</span></span>

### <span data-ttu-id="2d84c-135">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="2d84c-135">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2d84c-136">출력</span><span class="sxs-lookup"><span data-stu-id="2d84c-136">OUTPUTS</span></span>

### <span data-ttu-id="2d84c-137">PSGallery의. m a.</span><span class="sxs-lookup"><span data-stu-id="2d84c-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="2d84c-138">상속자</span><span class="sxs-lookup"><span data-stu-id="2d84c-138">NOTES</span></span>

## <span data-ttu-id="2d84c-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2d84c-139">RELATED LINKS</span></span>
