---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/publish-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
ms.openlocfilehash: e61beaa43f881aa148401ef91cd4cb37c1f18d88
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034453"
---
# <span data-ttu-id="d313a-101">Publish-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="d313a-101">Publish-AzBlueprint</span></span>

## <span data-ttu-id="d313a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d313a-102">SYNOPSIS</span></span>
<span data-ttu-id="d313a-103">새 버전의 청사진을 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d313a-103">Publish a new version of a blueprint.</span></span>

## <span data-ttu-id="d313a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d313a-104">SYNTAX</span></span>

```
Publish-AzBlueprint -Version <String> -ChangeNote <String> -Blueprint <PSBlueprint> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d313a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d313a-105">DESCRIPTION</span></span>
<span data-ttu-id="d313a-106">새 버전의 청사진 정의를 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d313a-106">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="d313a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d313a-107">EXAMPLES</span></span>

### <span data-ttu-id="d313a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="d313a-108">Example 1</span></span>
```powershell
PS C:\> Publish-AzBlueprint -Blueprint $bp -Version 1.0 

Name           : SimpleBlueprint
Id             : /subscriptions/{subscriptionId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint/versions/1.0
SubscriptionId : 00000000-1111-0000-1111-000000000000
Version        : 1.0
Description    : My simple blueprint
TimeCreated    : 2019-05-30
TargetScope    : Subscription
Parameters     : {[tagName, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue], [tagValue, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroups : {storageRG}
```
<span data-ttu-id="d313a-109">새 버전의 청사진 정의를 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d313a-109">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="d313a-110">변수</span><span class="sxs-lookup"><span data-stu-id="d313a-110">PARAMETERS</span></span>

### <span data-ttu-id="d313a-111">-청사진</span><span class="sxs-lookup"><span data-stu-id="d313a-111">-Blueprint</span></span>
<span data-ttu-id="d313a-112">청사진 개체</span><span class="sxs-lookup"><span data-stu-id="d313a-112">Blueprint object.</span></span>

```yaml
Type: PSBlueprint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d313a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d313a-113">-DefaultProfile</span></span>
<span data-ttu-id="d313a-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d313a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d313a-115">-버전</span><span class="sxs-lookup"><span data-stu-id="d313a-115">-Version</span></span>
<span data-ttu-id="d313a-116">청사진 정의 버전.</span><span class="sxs-lookup"><span data-stu-id="d313a-116">Version for the blueprint definition.</span></span>

### <span data-ttu-id="d313a-117">-ChangeNote</span><span class="sxs-lookup"><span data-stu-id="d313a-117">-ChangeNote</span></span>
<span data-ttu-id="d313a-118">이 청사진 버전의 내용에 대 한 설명을 참고 하세요.</span><span class="sxs-lookup"><span data-stu-id="d313a-118">Notes to describe the contents of this blueprint version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d313a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d313a-119">CommonParameters</span></span>
<span data-ttu-id="d313a-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d313a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d313a-121">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d313a-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d313a-122">입력</span><span class="sxs-lookup"><span data-stu-id="d313a-122">INPUTS</span></span>

### <span data-ttu-id="d313a-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d313a-123">System.String</span></span>

### <span data-ttu-id="d313a-124">Microsoft. m a. 모델. PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="d313a-124">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="d313a-125">출력</span><span class="sxs-lookup"><span data-stu-id="d313a-125">OUTPUTS</span></span>

### <span data-ttu-id="d313a-126">PSPublishedBlueprint (.).</span><span class="sxs-lookup"><span data-stu-id="d313a-126">Microsoft.Azure.Commands.Blueprint.Models.PSPublishedBlueprint</span></span>

## <span data-ttu-id="d313a-127">상속자</span><span class="sxs-lookup"><span data-stu-id="d313a-127">NOTES</span></span>

## <span data-ttu-id="d313a-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d313a-128">RELATED LINKS</span></span>
