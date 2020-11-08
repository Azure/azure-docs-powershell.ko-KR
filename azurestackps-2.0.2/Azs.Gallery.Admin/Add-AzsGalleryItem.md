---
external help file: ''
Module Name: Azs.Gallery.Admin
online version: https://docs.microsoft.com/powershell/module/azs.gallery.admin/add-azsgalleryitem
schema: 2.0.0
ms.openlocfilehash: d9ba42966efd4445fa561dff78b69d7e789badb5
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94046807"
---
# <span data-ttu-id="68245-101">Add-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="68245-101">Add-AzsGalleryItem</span></span>

## <span data-ttu-id="68245-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68245-102">SYNOPSIS</span></span>
<span data-ttu-id="68245-103">저장소에 공급자 갤러리 항목을 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="68245-103">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="68245-104">구문과</span><span class="sxs-lookup"><span data-stu-id="68245-104">SYNTAX</span></span>

### <span data-ttu-id="68245-105">CreateExpanded (기본값)</span><span class="sxs-lookup"><span data-stu-id="68245-105">CreateExpanded (Default)</span></span>
```
Add-AzsGalleryItem [-SubscriptionId <String>] [-GalleryItemUri <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="68245-106">만드는</span><span class="sxs-lookup"><span data-stu-id="68245-106">Create</span></span>
```
Add-AzsGalleryItem -GalleryItemUriPayload <IGalleryItemUriPayload> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="68245-107">설명은</span><span class="sxs-lookup"><span data-stu-id="68245-107">DESCRIPTION</span></span>
<span data-ttu-id="68245-108">저장소에 공급자 갤러리 항목을 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="68245-108">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="68245-109">예제의</span><span class="sxs-lookup"><span data-stu-id="68245-109">EXAMPLES</span></span>

### <span data-ttu-id="68245-110">예제 1: Add-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="68245-110">Example 1: Add-AzsGalleryItem</span></span>
```powershell
PS C:\> Add-AzsGalleryItem -GalleryItemUri https://testsa.blob.redmond.ext-n35r1010.masd.stbtest.microsoft.com/testsc/TestUbuntu.Test.1.0.0.azpkg

Name                  Publisher  PublisherDisplayName ItemName ItemDisplayName       Version Summary
----                  ---------  -------------------- -------- ---------------       ------- -------
TestUbuntu.Test.1.0.0 TestUbuntu TestUbuntu           Test     Test.TestUbuntu.1.0.0 1.0.0   Create a simple VM

```

<span data-ttu-id="68245-111">테스트를 갤러리에 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="68245-111">Uploads TestUbuntu.Test.1.0.0 to the gallery.</span></span>

## <span data-ttu-id="68245-112">변수</span><span class="sxs-lookup"><span data-stu-id="68245-112">PARAMETERS</span></span>

### <span data-ttu-id="68245-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68245-113">-DefaultProfile</span></span>
<span data-ttu-id="68245-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="68245-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="68245-115">-GalleryItemUri</span><span class="sxs-lookup"><span data-stu-id="68245-115">-GalleryItemUri</span></span>
<span data-ttu-id="68245-116">이미 온라인으로 업로드 한 갤러리 패키지의 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="68245-116">URI for your gallery package that has already been uploaded online.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="68245-117">-GalleryItemUriPayload</span><span class="sxs-lookup"><span data-stu-id="68245-117">-GalleryItemUriPayload</span></span>
<span data-ttu-id="68245-118">갤러리 항목 페이로드의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="68245-118">Location of gallery item payload.</span></span>
<span data-ttu-id="68245-119">생성 하려면 GALLERYITEMURIPAYLOAD 속성에 대 한 메모 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="68245-119">To construct, see NOTES section for GALLERYITEMURIPAYLOAD properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.Api20150401.IGalleryItemUriPayload
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="68245-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="68245-120">-SubscriptionId</span></span>
<span data-ttu-id="68245-121">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="68245-121">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="68245-122">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="68245-122">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="68245-123">-확인</span><span class="sxs-lookup"><span data-stu-id="68245-123">-Confirm</span></span>
<span data-ttu-id="68245-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="68245-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68245-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68245-125">-WhatIf</span></span>
<span data-ttu-id="68245-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="68245-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68245-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="68245-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68245-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68245-128">CommonParameters</span></span>
<span data-ttu-id="68245-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="68245-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68245-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="68245-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68245-131">입력</span><span class="sxs-lookup"><span data-stu-id="68245-131">INPUTS</span></span>

### <span data-ttu-id="68245-132">Api20150401. IGalleryItemUriPayload에 대 한 Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="68245-132">Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.Api20150401.IGalleryItemUriPayload</span></span>

## <span data-ttu-id="68245-133">출력</span><span class="sxs-lookup"><span data-stu-id="68245-133">OUTPUTS</span></span>

### <span data-ttu-id="68245-134">Api20150401. IGalleryItem에 대 한 Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="68245-134">Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.Api20150401.IGalleryItem</span></span>



## <span data-ttu-id="68245-135">상속자</span><span class="sxs-lookup"><span data-stu-id="68245-135">NOTES</span></span>

<span data-ttu-id="68245-136">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="68245-136">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="68245-137">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="68245-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="68245-138">GALLERYITEMURIPAYLOAD <IGalleryItemUriPayload> : 갤러리 항목 페이로드의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="68245-138">GALLERYITEMURIPAYLOAD <IGalleryItemUriPayload>: Location of gallery item payload.</span></span>
  - <span data-ttu-id="68245-139">`[GalleryItemUri <String>]`: 이미 온라인으로 업로드 된 갤러리 패키지의 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="68245-139">`[GalleryItemUri <String>]`: URI for your gallery package that has already been uploaded online.</span></span>

## <span data-ttu-id="68245-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="68245-140">RELATED LINKS</span></span>

