---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/import-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
ms.openlocfilehash: 3853cc1785ca0e9f087b1e30870d17d304666df4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697640"
---
# <span data-ttu-id="00604-101">Import-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="00604-101">Import-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="00604-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00604-102">SYNOPSIS</span></span>
<span data-ttu-id="00604-103">JSON 형식의 청사진 파일을 청사진 개체로 가져와 지정 된 구독 또는 관리 그룹 내에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="00604-103">Import a blueprint file in JSON format to a blueprint object and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="00604-104">구문과</span><span class="sxs-lookup"><span data-stu-id="00604-104">SYNTAX</span></span>

```
Import-AzBlueprintWithArtifact -Name <String> [-SubscriptionId <String>] [-ManagementGroupId <String>]
 -InputPath <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00604-105">설명은</span><span class="sxs-lookup"><span data-stu-id="00604-105">DESCRIPTION</span></span>
<span data-ttu-id="00604-106">해당 가공물을 사용 하 여 청사진 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="00604-106">Import a blueprint definition with its artifacts.</span></span> 

## <span data-ttu-id="00604-107">예제의</span><span class="sxs-lookup"><span data-stu-id="00604-107">EXAMPLES</span></span>

### <span data-ttu-id="00604-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="00604-108">Example 1</span></span>
```powershell
PS C:\> Import-AzBlueprintWithArtifact -Name MySimpleBlueprint -SubscriptionId 00000000-1111-0000-1111-000000000000 -InputPath  C:\Blueprints\SimpleBlueprint
```

<span data-ttu-id="00604-109">해당 가공물을 사용 하 여 청사진 정의를 가져오고 구독 내에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="00604-109">Import a blueprint definition with its artifacts and save within a subscription.</span></span>

## <span data-ttu-id="00604-110">변수</span><span class="sxs-lookup"><span data-stu-id="00604-110">PARAMETERS</span></span>

### <span data-ttu-id="00604-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00604-111">-DefaultProfile</span></span>
<span data-ttu-id="00604-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="00604-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00604-113">-Force</span><span class="sxs-lookup"><span data-stu-id="00604-113">-Force</span></span>
<span data-ttu-id="00604-114">True로 설정 하면 실행 시 확인 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="00604-114">When set to true, execution will not ask for a confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00604-115">-InputPath</span><span class="sxs-lookup"><span data-stu-id="00604-115">-InputPath</span></span>
<span data-ttu-id="00604-116">디스크의 청사진 JSON 파일에 대 한 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="00604-116">Path to a Blueprint JSON file on disk.</span></span>

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

### <span data-ttu-id="00604-117">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="00604-117">-ManagementGroupId</span></span>
<span data-ttu-id="00604-118">청사진 정의가 있거나 저장 되는 관리 그룹 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="00604-118">Management Group Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00604-119">-이름</span><span class="sxs-lookup"><span data-stu-id="00604-119">-Name</span></span>
<span data-ttu-id="00604-120">청사진 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="00604-120">Blueprint definition name.</span></span>

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

### <span data-ttu-id="00604-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="00604-121">-SubscriptionId</span></span>
<span data-ttu-id="00604-122">청사진 정의가 있는 구독 Id 또는 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="00604-122">Subscription Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00604-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00604-123">CommonParameters</span></span>
<span data-ttu-id="00604-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="00604-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="00604-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00604-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00604-126">입력</span><span class="sxs-lookup"><span data-stu-id="00604-126">INPUTS</span></span>

### <span data-ttu-id="00604-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="00604-127">System.String</span></span>

## <span data-ttu-id="00604-128">출력</span><span class="sxs-lookup"><span data-stu-id="00604-128">OUTPUTS</span></span>

### <span data-ttu-id="00604-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="00604-129">System.String</span></span>

## <span data-ttu-id="00604-130">상속자</span><span class="sxs-lookup"><span data-stu-id="00604-130">NOTES</span></span>

## <span data-ttu-id="00604-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="00604-131">RELATED LINKS</span></span>
