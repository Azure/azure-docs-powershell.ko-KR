---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprint.md
ms.openlocfilehash: 3213d5dbb981d9cc7d7871ce97f9fd78f375a59a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697635"
---
# <span data-ttu-id="fc86f-101">New-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="fc86f-101">New-AzBlueprint</span></span>

## <span data-ttu-id="fc86f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc86f-102">SYNOPSIS</span></span>
<span data-ttu-id="fc86f-103">새 청사진 정의를 만들고 지정 된 구독 또는 관리 그룹 내에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc86f-103">Create a new blueprint definition and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="fc86f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fc86f-104">SYNTAX</span></span>

### <span data-ttu-id="fc86f-105">CreateBlueprintBySubscription (기본값)</span><span class="sxs-lookup"><span data-stu-id="fc86f-105">CreateBlueprintBySubscription (Default)</span></span>
```
New-AzBlueprint -Name <String> [-SubscriptionId <String>] -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc86f-106">CreateBlueprintByManagementGroup</span><span class="sxs-lookup"><span data-stu-id="fc86f-106">CreateBlueprintByManagementGroup</span></span>
```
New-AzBlueprint -Name <String> -ManagementGroupId <String> -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc86f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="fc86f-107">DESCRIPTION</span></span>
<span data-ttu-id="fc86f-108">새 청사진 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fc86f-108">Create a new blueprint definition.</span></span> 

## <span data-ttu-id="fc86f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="fc86f-109">EXAMPLES</span></span>

### <span data-ttu-id="fc86f-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="fc86f-110">Example 1</span></span>
```powershell
PS C:\> New-AzBlueprint -Name MyNewBlueprint -SubscriptionId 00000000-1111-0000-1111-000000000000 -BlueprintFile C:\Blueprint.json

Name              : SimpleBlueprint
Id                : /providers/Microsoft.Management/managementGroups/{mgId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint
ManagementGroupId : myManagementGroupId
Versions          : 
Description       : test
TimeCreated       : 2019-05-12
TargetScope       : Subscription
Parameters        : {enforcetaganditsvalue_tagName, enforcetaganditsvalue_tagValue}
ResourceGroups    : {AppNetworkRG}
```

<span data-ttu-id="fc86f-111">지정 된 구독 내에 새 청사진 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fc86f-111">Create a new blueprint definition within the specified subscription.</span></span>

## <span data-ttu-id="fc86f-112">변수</span><span class="sxs-lookup"><span data-stu-id="fc86f-112">PARAMETERS</span></span>

### <span data-ttu-id="fc86f-113">-BlueprintFile</span><span class="sxs-lookup"><span data-stu-id="fc86f-113">-BlueprintFile</span></span>
<span data-ttu-id="fc86f-114">디스크의 청사진 JSON 파일에 대 한 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="fc86f-114">Path to a Blueprint JSON file on disk.</span></span>

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

### <span data-ttu-id="fc86f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc86f-115">-DefaultProfile</span></span>
<span data-ttu-id="fc86f-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fc86f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc86f-117">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="fc86f-117">-ManagementGroupId</span></span>
<span data-ttu-id="fc86f-118">청사진 정의가 있거나 저장 되는 관리 그룹 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="fc86f-118">Management Group Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: String
Parameter Sets: CreateBlueprintByManagementGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc86f-119">-이름</span><span class="sxs-lookup"><span data-stu-id="fc86f-119">-Name</span></span>
<span data-ttu-id="fc86f-120">청사진 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fc86f-120">Blueprint definition name.</span></span>

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

### <span data-ttu-id="fc86f-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fc86f-121">-SubscriptionId</span></span>
<span data-ttu-id="fc86f-122">청사진 정의가 있는 구독 Id 또는 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fc86f-122">Subscription Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: String
Parameter Sets: CreateBlueprintBySubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc86f-123">-확인</span><span class="sxs-lookup"><span data-stu-id="fc86f-123">-Confirm</span></span>
<span data-ttu-id="fc86f-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc86f-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc86f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc86f-125">-WhatIf</span></span>
<span data-ttu-id="fc86f-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fc86f-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc86f-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fc86f-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc86f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc86f-128">CommonParameters</span></span>
<span data-ttu-id="fc86f-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc86f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="fc86f-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc86f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc86f-131">입력</span><span class="sxs-lookup"><span data-stu-id="fc86f-131">INPUTS</span></span>

### <span data-ttu-id="fc86f-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fc86f-132">System.String</span></span>

## <span data-ttu-id="fc86f-133">출력</span><span class="sxs-lookup"><span data-stu-id="fc86f-133">OUTPUTS</span></span>

### <span data-ttu-id="fc86f-134">Microsoft. m a. 모델. PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="fc86f-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="fc86f-135">상속자</span><span class="sxs-lookup"><span data-stu-id="fc86f-135">NOTES</span></span>

## <span data-ttu-id="fc86f-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fc86f-136">RELATED LINKS</span></span>
