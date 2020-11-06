---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmGalleryImageVersion.md
ms.openlocfilehash: bff748b8c867b272208469d34229cc2724bc8610
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528600"
---
# <span data-ttu-id="db36c-101">Get-AzureRmGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="db36c-101">Get-AzureRmGalleryImageVersion</span></span>

## <span data-ttu-id="db36c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db36c-102">SYNOPSIS</span></span>
<span data-ttu-id="db36c-103">갤러리 이미지 버전을 가져오거나 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="db36c-103">Get or list gallery image versions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db36c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="db36c-104">SYNTAX</span></span>

### <span data-ttu-id="db36c-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="db36c-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [[-Name] <String>] [-ExpandReplicationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="db36c-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="db36c-106">ResourceIdParameter</span></span>
```
Get-AzureRmGalleryImageVersion [-ResourceId] <String> [-ExpandReplicationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db36c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="db36c-107">DESCRIPTION</span></span>
<span data-ttu-id="db36c-108">갤러리 이미지 버전을 가져오거나 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="db36c-108">Get or list gallery image versions.</span></span>

## <span data-ttu-id="db36c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="db36c-109">EXAMPLES</span></span>

### <span data-ttu-id="db36c-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="db36c-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmGalleryImageVersion -ResourceGroupName $rgname -GalleryName $gallery -ImageDefinitionName $image -GalleryImageVersionName $version
```

<span data-ttu-id="db36c-111">갤러리 이미지 버전을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="db36c-111">Get the gallery image version.</span></span>

## <span data-ttu-id="db36c-112">변수</span><span class="sxs-lookup"><span data-stu-id="db36c-112">PARAMETERS</span></span>

### <span data-ttu-id="db36c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db36c-113">-DefaultProfile</span></span>
<span data-ttu-id="db36c-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="db36c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db36c-115">-ExpandReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="db36c-115">-ExpandReplicationStatus</span></span>
<span data-ttu-id="db36c-116">복제 상태를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="db36c-116">Show replication status.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db36c-117">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="db36c-117">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="db36c-118">갤러리 이미지 정의의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="db36c-118">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db36c-119">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="db36c-119">-GalleryName</span></span>
<span data-ttu-id="db36c-120">갤러리의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="db36c-120">The name of the gallery.</span></span>

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

### <span data-ttu-id="db36c-121">-이름</span><span class="sxs-lookup"><span data-stu-id="db36c-121">-Name</span></span>
<span data-ttu-id="db36c-122">갤러리 이미지 버전의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="db36c-122">The name of the gallery image version.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageVersionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db36c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db36c-123">-ResourceGroupName</span></span>
<span data-ttu-id="db36c-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="db36c-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="db36c-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="db36c-125">-ResourceId</span></span>
<span data-ttu-id="db36c-126">갤러리 이미지 버전의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="db36c-126">The resource ID for the gallery image version</span></span>

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

### <span data-ttu-id="db36c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db36c-127">CommonParameters</span></span>
<span data-ttu-id="db36c-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="db36c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db36c-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db36c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db36c-130">입력</span><span class="sxs-lookup"><span data-stu-id="db36c-130">INPUTS</span></span>

### <span data-ttu-id="db36c-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="db36c-131">System.String</span></span>

### <span data-ttu-id="db36c-132">PSGalleryImageVersion의. m a.</span><span class="sxs-lookup"><span data-stu-id="db36c-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="db36c-133">출력</span><span class="sxs-lookup"><span data-stu-id="db36c-133">OUTPUTS</span></span>

### <span data-ttu-id="db36c-134">PSGalleryImageVersion의. m a.</span><span class="sxs-lookup"><span data-stu-id="db36c-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="db36c-135">상속자</span><span class="sxs-lookup"><span data-stu-id="db36c-135">NOTES</span></span>

## <span data-ttu-id="db36c-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="db36c-136">RELATED LINKS</span></span>
