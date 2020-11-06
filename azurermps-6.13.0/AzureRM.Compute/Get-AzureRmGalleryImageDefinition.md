---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmGalleryImageDefinition.md
ms.openlocfilehash: 75d30165c5dc5d69eabd08e89ad2577df82f7ebd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528601"
---
# <span data-ttu-id="dc355-101">Get-AzureRmGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="dc355-101">Get-AzureRmGalleryImageDefinition</span></span>

## <span data-ttu-id="dc355-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc355-102">SYNOPSIS</span></span>
<span data-ttu-id="dc355-103">갤러리 이미지 정의를 가져오거나 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc355-103">Get or list gallery image definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc355-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dc355-104">SYNTAX</span></span>

### <span data-ttu-id="dc355-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="dc355-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc355-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="dc355-106">ResourceIdParameter</span></span>
```
Get-AzureRmGalleryImageDefinition [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dc355-107">설명은</span><span class="sxs-lookup"><span data-stu-id="dc355-107">DESCRIPTION</span></span>
<span data-ttu-id="dc355-108">갤러리 이미지 정의를 가져오거나 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc355-108">Get or list gallery image definitions.</span></span>

## <span data-ttu-id="dc355-109">예제의</span><span class="sxs-lookup"><span data-stu-id="dc355-109">EXAMPLES</span></span>

### <span data-ttu-id="dc355-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="dc355-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmGalleryImageDefinition -ResourceGroupName $rgname -GalleryName $gallery -GalleryImageDefinitionName $image
```

<span data-ttu-id="dc355-111">갤러리 이미지 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dc355-111">Get the gallery image definition.</span></span>

## <span data-ttu-id="dc355-112">변수</span><span class="sxs-lookup"><span data-stu-id="dc355-112">PARAMETERS</span></span>

### <span data-ttu-id="dc355-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc355-113">-DefaultProfile</span></span>
<span data-ttu-id="dc355-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dc355-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc355-115">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="dc355-115">-GalleryName</span></span>
<span data-ttu-id="dc355-116">갤러리의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dc355-116">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc355-117">-이름</span><span class="sxs-lookup"><span data-stu-id="dc355-117">-Name</span></span>
<span data-ttu-id="dc355-118">갤러리 이미지 정의의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dc355-118">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageDefinitionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc355-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc355-119">-ResourceGroupName</span></span>
<span data-ttu-id="dc355-120">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dc355-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="dc355-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dc355-121">-ResourceId</span></span>
<span data-ttu-id="dc355-122">갤러리 이미지 정의의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="dc355-122">The resource ID for the gallery image definition</span></span>

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

### <span data-ttu-id="dc355-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc355-123">CommonParameters</span></span>
<span data-ttu-id="dc355-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc355-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc355-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc355-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc355-126">입력</span><span class="sxs-lookup"><span data-stu-id="dc355-126">INPUTS</span></span>

### <span data-ttu-id="dc355-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="dc355-127">System.String</span></span>

## <span data-ttu-id="dc355-128">출력</span><span class="sxs-lookup"><span data-stu-id="dc355-128">OUTPUTS</span></span>

### <span data-ttu-id="dc355-129">PSGalleryImage의. m a.</span><span class="sxs-lookup"><span data-stu-id="dc355-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="dc355-130">상속자</span><span class="sxs-lookup"><span data-stu-id="dc355-130">NOTES</span></span>

## <span data-ttu-id="dc355-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dc355-131">RELATED LINKS</span></span>
