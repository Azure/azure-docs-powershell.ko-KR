---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmGallery.md
ms.openlocfilehash: cdb703144daa6f9abd62aee41eaad94b2cfa50e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528608"
---
# <span data-ttu-id="d7088-101">Get-AzureRmGallery</span><span class="sxs-lookup"><span data-stu-id="d7088-101">Get-AzureRmGallery</span></span>

## <span data-ttu-id="d7088-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7088-102">SYNOPSIS</span></span>
<span data-ttu-id="d7088-103">갤러리 가져오기 또는 나열</span><span class="sxs-lookup"><span data-stu-id="d7088-103">Get or list galleries.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7088-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d7088-104">SYNTAX</span></span>

### <span data-ttu-id="d7088-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="d7088-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmGallery [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7088-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="d7088-106">ResourceIdParameter</span></span>
```
Get-AzureRmGallery [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7088-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d7088-107">DESCRIPTION</span></span>
<span data-ttu-id="d7088-108">갤러리 가져오기 또는 나열</span><span class="sxs-lookup"><span data-stu-id="d7088-108">Get or list galleries.</span></span>

## <span data-ttu-id="d7088-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d7088-109">EXAMPLES</span></span>

### <span data-ttu-id="d7088-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="d7088-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmGallery -ResourceGroupName $rgname -GalleryName $galleryName

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

<span data-ttu-id="d7088-111">갤러리를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d7088-111">Get the gallery.</span></span>

## <span data-ttu-id="d7088-112">변수</span><span class="sxs-lookup"><span data-stu-id="d7088-112">PARAMETERS</span></span>

### <span data-ttu-id="d7088-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7088-113">-DefaultProfile</span></span>
<span data-ttu-id="d7088-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d7088-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7088-115">-이름</span><span class="sxs-lookup"><span data-stu-id="d7088-115">-Name</span></span>
<span data-ttu-id="d7088-116">갤러리의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d7088-116">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7088-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7088-117">-ResourceGroupName</span></span>
<span data-ttu-id="d7088-118">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d7088-118">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7088-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d7088-119">-ResourceId</span></span>
<span data-ttu-id="d7088-120">갤러리의 자원 id</span><span class="sxs-lookup"><span data-stu-id="d7088-120">The resource id for Gallery</span></span>

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

### <span data-ttu-id="d7088-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7088-121">CommonParameters</span></span>
<span data-ttu-id="d7088-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7088-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7088-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7088-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7088-124">입력</span><span class="sxs-lookup"><span data-stu-id="d7088-124">INPUTS</span></span>

### <span data-ttu-id="d7088-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d7088-125">System.String</span></span>

### <span data-ttu-id="d7088-126">PSGallery의. m a.</span><span class="sxs-lookup"><span data-stu-id="d7088-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="d7088-127">출력</span><span class="sxs-lookup"><span data-stu-id="d7088-127">OUTPUTS</span></span>

### <span data-ttu-id="d7088-128">PSGallery의. m a.</span><span class="sxs-lookup"><span data-stu-id="d7088-128">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="d7088-129">상속자</span><span class="sxs-lookup"><span data-stu-id="d7088-129">NOTES</span></span>

## <span data-ttu-id="d7088-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d7088-130">RELATED LINKS</span></span>
