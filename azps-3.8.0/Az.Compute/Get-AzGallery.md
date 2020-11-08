---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGallery.md
ms.openlocfilehash: baa3730ee03dd8f871e64e7964659c62f60e8032
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043440"
---
# <span data-ttu-id="5aa81-101">Get-AzGallery</span><span class="sxs-lookup"><span data-stu-id="5aa81-101">Get-AzGallery</span></span>

## <span data-ttu-id="5aa81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5aa81-102">SYNOPSIS</span></span>
<span data-ttu-id="5aa81-103">갤러리 가져오기 또는 나열</span><span class="sxs-lookup"><span data-stu-id="5aa81-103">Get or list galleries.</span></span>

## <span data-ttu-id="5aa81-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5aa81-104">SYNTAX</span></span>

### <span data-ttu-id="5aa81-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="5aa81-105">DefaultParameter (Default)</span></span>
```
Get-AzGallery [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5aa81-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="5aa81-106">ResourceIdParameter</span></span>
```
Get-AzGallery [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5aa81-107">설명은</span><span class="sxs-lookup"><span data-stu-id="5aa81-107">DESCRIPTION</span></span>
<span data-ttu-id="5aa81-108">갤러리 가져오기 또는 나열</span><span class="sxs-lookup"><span data-stu-id="5aa81-108">Get or list galleries.</span></span>

## <span data-ttu-id="5aa81-109">예제의</span><span class="sxs-lookup"><span data-stu-id="5aa81-109">EXAMPLES</span></span>

### <span data-ttu-id="5aa81-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="5aa81-110">Example 1</span></span>
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

<span data-ttu-id="5aa81-111">"Gallery1" 갤러리 가져오기</span><span class="sxs-lookup"><span data-stu-id="5aa81-111">Get the gallery "gallery1"</span></span>

### <span data-ttu-id="5aa81-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="5aa81-112">Example 2</span></span>
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

<span data-ttu-id="5aa81-113">Rg1의 모든 갤러리를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5aa81-113">Get all galleries in rg1.</span></span>

### <span data-ttu-id="5aa81-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="5aa81-114">Example 3</span></span>
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

<span data-ttu-id="5aa81-115">구독에 있는 모든 갤러리를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5aa81-115">Get all galleries in subscription.</span></span>

### <span data-ttu-id="5aa81-116">예제 4</span><span class="sxs-lookup"><span data-stu-id="5aa81-116">Example 4</span></span>
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

<span data-ttu-id="5aa81-117">"갤러리"로 시작 하는 구독의 모든 갤러리를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5aa81-117">Get all galleries in subscription that start with "gallery".</span></span>

## <span data-ttu-id="5aa81-118">변수</span><span class="sxs-lookup"><span data-stu-id="5aa81-118">PARAMETERS</span></span>

### <span data-ttu-id="5aa81-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5aa81-119">-DefaultProfile</span></span>
<span data-ttu-id="5aa81-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5aa81-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5aa81-121">-이름</span><span class="sxs-lookup"><span data-stu-id="5aa81-121">-Name</span></span>
<span data-ttu-id="5aa81-122">갤러리의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5aa81-122">The name of the gallery.</span></span>

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

### <span data-ttu-id="5aa81-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5aa81-123">-ResourceGroupName</span></span>
<span data-ttu-id="5aa81-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5aa81-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="5aa81-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5aa81-125">-ResourceId</span></span>
<span data-ttu-id="5aa81-126">갤러리의 자원 id</span><span class="sxs-lookup"><span data-stu-id="5aa81-126">The resource id for Gallery</span></span>

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

### <span data-ttu-id="5aa81-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5aa81-127">CommonParameters</span></span>
<span data-ttu-id="5aa81-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5aa81-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5aa81-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5aa81-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5aa81-130">입력</span><span class="sxs-lookup"><span data-stu-id="5aa81-130">INPUTS</span></span>

### <span data-ttu-id="5aa81-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5aa81-131">System.String</span></span>

## <span data-ttu-id="5aa81-132">출력</span><span class="sxs-lookup"><span data-stu-id="5aa81-132">OUTPUTS</span></span>

### <span data-ttu-id="5aa81-133">PSGallery의. m a.</span><span class="sxs-lookup"><span data-stu-id="5aa81-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="5aa81-134">상속자</span><span class="sxs-lookup"><span data-stu-id="5aa81-134">NOTES</span></span>

## <span data-ttu-id="5aa81-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5aa81-135">RELATED LINKS</span></span>
