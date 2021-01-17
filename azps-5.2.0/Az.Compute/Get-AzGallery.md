---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGallery.md
ms.openlocfilehash: baa3730ee03dd8f871e64e7964659c62f60e8032
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332786"
---
# <span data-ttu-id="c34c7-101">Get-AzGallery</span><span class="sxs-lookup"><span data-stu-id="c34c7-101">Get-AzGallery</span></span>

## <span data-ttu-id="c34c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c34c7-102">SYNOPSIS</span></span>
<span data-ttu-id="c34c7-103">갤러리를 얻거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="c34c7-103">Get or list galleries.</span></span>

## <span data-ttu-id="c34c7-104">구문</span><span class="sxs-lookup"><span data-stu-id="c34c7-104">SYNTAX</span></span>

### <span data-ttu-id="c34c7-105">DefaultParameter(기본값)</span><span class="sxs-lookup"><span data-stu-id="c34c7-105">DefaultParameter (Default)</span></span>
```
Get-AzGallery [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c34c7-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="c34c7-106">ResourceIdParameter</span></span>
```
Get-AzGallery [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c34c7-107">설명</span><span class="sxs-lookup"><span data-stu-id="c34c7-107">DESCRIPTION</span></span>
<span data-ttu-id="c34c7-108">갤러리를 얻거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="c34c7-108">Get or list galleries.</span></span>

## <span data-ttu-id="c34c7-109">예제</span><span class="sxs-lookup"><span data-stu-id="c34c7-109">EXAMPLES</span></span>

### <span data-ttu-id="c34c7-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="c34c7-110">Example 1</span></span>
```powershell
PS C:\> Get-AzGallery -ResourceGroupName rg1 -GalleryName gallery1

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery1
Name              : gallery1
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}
```

<span data-ttu-id="c34c7-111">갤러리 "gallery1"</span><span class="sxs-lookup"><span data-stu-id="c34c7-111">Get the gallery "gallery1"</span></span>

### <span data-ttu-id="c34c7-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="c34c7-112">Example 2</span></span>
```powershell
PS C:\> Get-AzGallery -ResourceGroupName rg1

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery1
Name              : gallery1
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery2
Name              : gallery2
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}
```

<span data-ttu-id="c34c7-113">rg1에서 모든 갤러리를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c34c7-113">Get all galleries in rg1.</span></span>

### <span data-ttu-id="c34c7-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="c34c7-114">Example 3</span></span>
```powershell
PS C:\> Get-AzGallery

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery1
Name              : gallery1
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery2
Name              : gallery2
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}

ResourceGroupName : rg2
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg2/providers/Microsoft.Compute/galleries/gallery3
Name              : gallery3
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}
```

<span data-ttu-id="c34c7-115">구독의 모든 갤러리를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c34c7-115">Get all galleries in subscription.</span></span>

### <span data-ttu-id="c34c7-116">예제 4</span><span class="sxs-lookup"><span data-stu-id="c34c7-116">Example 4</span></span>
```powershell
PS C:\> Get-AzGallery -Name gallery*

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery1
Name              : gallery1
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery2
Name              : gallery2
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}

ResourceGroupName : rg2
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg2/providers/Microsoft.Compute/galleries/gallery3
Name              : gallery3
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}
```

<span data-ttu-id="c34c7-117">"gallery"로 시작하는 구독의 모든 갤러리를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c34c7-117">Get all galleries in subscription that start with "gallery".</span></span>

## <span data-ttu-id="c34c7-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c34c7-118">PARAMETERS</span></span>

### <span data-ttu-id="c34c7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c34c7-119">-DefaultProfile</span></span>
<span data-ttu-id="c34c7-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c34c7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c34c7-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c34c7-121">-Name</span></span>
<span data-ttu-id="c34c7-122">갤러리의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c34c7-122">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="c34c7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c34c7-123">-ResourceGroupName</span></span>
<span data-ttu-id="c34c7-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c34c7-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="c34c7-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c34c7-125">-ResourceId</span></span>
<span data-ttu-id="c34c7-126">갤러리의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="c34c7-126">The resource id for Gallery</span></span>

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

### <span data-ttu-id="c34c7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c34c7-127">CommonParameters</span></span>
<span data-ttu-id="c34c7-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c34c7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c34c7-129">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c34c7-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c34c7-130">입력</span><span class="sxs-lookup"><span data-stu-id="c34c7-130">INPUTS</span></span>

### <span data-ttu-id="c34c7-131">System.String</span><span class="sxs-lookup"><span data-stu-id="c34c7-131">System.String</span></span>

## <span data-ttu-id="c34c7-132">출력</span><span class="sxs-lookup"><span data-stu-id="c34c7-132">OUTPUTS</span></span>

### <span data-ttu-id="c34c7-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span><span class="sxs-lookup"><span data-stu-id="c34c7-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="c34c7-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c34c7-134">NOTES</span></span>

## <span data-ttu-id="c34c7-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c34c7-135">RELATED LINKS</span></span>
