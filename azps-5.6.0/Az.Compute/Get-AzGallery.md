---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGallery.md
ms.openlocfilehash: 7764ee4cd151e3de7cca2af84ed0cf670c52a6a9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969291"
---
# <span data-ttu-id="7d33c-101">Get-AzGallery</span><span class="sxs-lookup"><span data-stu-id="7d33c-101">Get-AzGallery</span></span>

## <span data-ttu-id="7d33c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d33c-102">SYNOPSIS</span></span>
<span data-ttu-id="7d33c-103">갤러리를 얻거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="7d33c-103">Get or list galleries.</span></span>

## <span data-ttu-id="7d33c-104">구문</span><span class="sxs-lookup"><span data-stu-id="7d33c-104">SYNTAX</span></span>

### <span data-ttu-id="7d33c-105">DefaultParameter(기본값)</span><span class="sxs-lookup"><span data-stu-id="7d33c-105">DefaultParameter (Default)</span></span>
```
Get-AzGallery [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7d33c-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="7d33c-106">ResourceIdParameter</span></span>
```
Get-AzGallery [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d33c-107">설명</span><span class="sxs-lookup"><span data-stu-id="7d33c-107">DESCRIPTION</span></span>
<span data-ttu-id="7d33c-108">갤러리를 얻거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="7d33c-108">Get or list galleries.</span></span>

## <span data-ttu-id="7d33c-109">예제</span><span class="sxs-lookup"><span data-stu-id="7d33c-109">EXAMPLES</span></span>

### <span data-ttu-id="7d33c-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="7d33c-110">Example 1</span></span>
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

<span data-ttu-id="7d33c-111">갤러리 "gallery1" 얻기</span><span class="sxs-lookup"><span data-stu-id="7d33c-111">Get the gallery "gallery1"</span></span>

### <span data-ttu-id="7d33c-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="7d33c-112">Example 2</span></span>
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

<span data-ttu-id="7d33c-113">rg1에서 모든 갤러리를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7d33c-113">Get all galleries in rg1.</span></span>

### <span data-ttu-id="7d33c-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="7d33c-114">Example 3</span></span>
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

<span data-ttu-id="7d33c-115">구독의 모든 갤러리를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7d33c-115">Get all galleries in subscription.</span></span>

### <span data-ttu-id="7d33c-116">예제 4</span><span class="sxs-lookup"><span data-stu-id="7d33c-116">Example 4</span></span>
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

<span data-ttu-id="7d33c-117">"갤러리"로 시작하는 구독의 모든 갤러리를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7d33c-117">Get all galleries in subscription that start with "gallery".</span></span>

## <span data-ttu-id="7d33c-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7d33c-118">PARAMETERS</span></span>

### <span data-ttu-id="7d33c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d33c-119">-DefaultProfile</span></span>
<span data-ttu-id="7d33c-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7d33c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d33c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="7d33c-121">-Name</span></span>
<span data-ttu-id="7d33c-122">갤러리의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7d33c-122">The name of the gallery.</span></span>

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

### <span data-ttu-id="7d33c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d33c-123">-ResourceGroupName</span></span>
<span data-ttu-id="7d33c-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7d33c-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="7d33c-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d33c-125">-ResourceId</span></span>
<span data-ttu-id="7d33c-126">갤러리에 대한 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="7d33c-126">The resource id for Gallery</span></span>

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

### <span data-ttu-id="7d33c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d33c-127">CommonParameters</span></span>
<span data-ttu-id="7d33c-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7d33c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d33c-129">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7d33c-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d33c-130">입력</span><span class="sxs-lookup"><span data-stu-id="7d33c-130">INPUTS</span></span>

### <span data-ttu-id="7d33c-131">System.String</span><span class="sxs-lookup"><span data-stu-id="7d33c-131">System.String</span></span>

## <span data-ttu-id="7d33c-132">출력</span><span class="sxs-lookup"><span data-stu-id="7d33c-132">OUTPUTS</span></span>

### <span data-ttu-id="7d33c-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span><span class="sxs-lookup"><span data-stu-id="7d33c-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="7d33c-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7d33c-134">NOTES</span></span>

## <span data-ttu-id="7d33c-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7d33c-135">RELATED LINKS</span></span>
