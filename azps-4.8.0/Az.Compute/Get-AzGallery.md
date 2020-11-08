---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGallery.md
ms.openlocfilehash: baa3730ee03dd8f871e64e7964659c62f60e8032
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048146"
---
# <span data-ttu-id="e4520-101">Get-AzGallery</span><span class="sxs-lookup"><span data-stu-id="e4520-101">Get-AzGallery</span></span>

## <span data-ttu-id="e4520-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4520-102">SYNOPSIS</span></span>
<span data-ttu-id="e4520-103">갤러리 가져오기 또는 나열</span><span class="sxs-lookup"><span data-stu-id="e4520-103">Get or list galleries.</span></span>

## <span data-ttu-id="e4520-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e4520-104">SYNTAX</span></span>

### <span data-ttu-id="e4520-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="e4520-105">DefaultParameter (Default)</span></span>
```
Get-AzGallery [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e4520-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="e4520-106">ResourceIdParameter</span></span>
```
Get-AzGallery [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4520-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e4520-107">DESCRIPTION</span></span>
<span data-ttu-id="e4520-108">갤러리 가져오기 또는 나열</span><span class="sxs-lookup"><span data-stu-id="e4520-108">Get or list galleries.</span></span>

## <span data-ttu-id="e4520-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e4520-109">EXAMPLES</span></span>

### <span data-ttu-id="e4520-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="e4520-110">Example 1</span></span>
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

<span data-ttu-id="e4520-111">"Gallery1" 갤러리 가져오기</span><span class="sxs-lookup"><span data-stu-id="e4520-111">Get the gallery "gallery1"</span></span>

### <span data-ttu-id="e4520-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="e4520-112">Example 2</span></span>
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

<span data-ttu-id="e4520-113">Rg1의 모든 갤러리를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e4520-113">Get all galleries in rg1.</span></span>

### <span data-ttu-id="e4520-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="e4520-114">Example 3</span></span>
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

<span data-ttu-id="e4520-115">구독에 있는 모든 갤러리를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e4520-115">Get all galleries in subscription.</span></span>

### <span data-ttu-id="e4520-116">예제 4</span><span class="sxs-lookup"><span data-stu-id="e4520-116">Example 4</span></span>
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

<span data-ttu-id="e4520-117">"갤러리"로 시작 하는 구독의 모든 갤러리를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e4520-117">Get all galleries in subscription that start with "gallery".</span></span>

## <span data-ttu-id="e4520-118">변수</span><span class="sxs-lookup"><span data-stu-id="e4520-118">PARAMETERS</span></span>

### <span data-ttu-id="e4520-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4520-119">-DefaultProfile</span></span>
<span data-ttu-id="e4520-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e4520-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4520-121">-이름</span><span class="sxs-lookup"><span data-stu-id="e4520-121">-Name</span></span>
<span data-ttu-id="e4520-122">갤러리의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e4520-122">The name of the gallery.</span></span>

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

### <span data-ttu-id="e4520-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4520-123">-ResourceGroupName</span></span>
<span data-ttu-id="e4520-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e4520-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="e4520-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e4520-125">-ResourceId</span></span>
<span data-ttu-id="e4520-126">갤러리의 자원 id</span><span class="sxs-lookup"><span data-stu-id="e4520-126">The resource id for Gallery</span></span>

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

### <span data-ttu-id="e4520-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4520-127">CommonParameters</span></span>
<span data-ttu-id="e4520-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4520-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4520-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e4520-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4520-130">입력</span><span class="sxs-lookup"><span data-stu-id="e4520-130">INPUTS</span></span>

### <span data-ttu-id="e4520-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e4520-131">System.String</span></span>

## <span data-ttu-id="e4520-132">출력</span><span class="sxs-lookup"><span data-stu-id="e4520-132">OUTPUTS</span></span>

### <span data-ttu-id="e4520-133">PSGallery의. m a.</span><span class="sxs-lookup"><span data-stu-id="e4520-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="e4520-134">상속자</span><span class="sxs-lookup"><span data-stu-id="e4520-134">NOTES</span></span>

## <span data-ttu-id="e4520-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e4520-135">RELATED LINKS</span></span>
