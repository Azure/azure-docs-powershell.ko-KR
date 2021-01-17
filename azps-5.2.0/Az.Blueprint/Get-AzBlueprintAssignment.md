---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintAssignment.md
ms.openlocfilehash: 06398b9c5e880577606e0367722fc22c242d58f4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327781"
---
# <span data-ttu-id="c956a-101">Get-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="c956a-101">Get-AzBlueprintAssignment</span></span>

## <span data-ttu-id="c956a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c956a-102">SYNOPSIS</span></span>
<span data-ttu-id="c956a-103">하나 이상의 청사진 할당을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c956a-103">Get one or more blueprint assignments.</span></span>

## <span data-ttu-id="c956a-104">구문</span><span class="sxs-lookup"><span data-stu-id="c956a-104">SYNTAX</span></span>

### <span data-ttu-id="c956a-105">SubscriptionScope(기본값)</span><span class="sxs-lookup"><span data-stu-id="c956a-105">SubscriptionScope (Default)</span></span>
```
Get-AzBlueprintAssignment [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c956a-106">BySubscriptionAndName</span><span class="sxs-lookup"><span data-stu-id="c956a-106">BySubscriptionAndName</span></span>
```
Get-AzBlueprintAssignment -Name <String> [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c956a-107">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="c956a-107">ByManagementGroupAndName</span></span>
```
Get-AzBlueprintAssignment -Name <String> -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c956a-108">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="c956a-108">ManagementGroupScope</span></span>
```
Get-AzBlueprintAssignment -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c956a-109">설명</span><span class="sxs-lookup"><span data-stu-id="c956a-109">DESCRIPTION</span></span>
<span data-ttu-id="c956a-110">하나 이상의 청사진 할당을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c956a-110">Get one or more blueprint assignments.</span></span> <span data-ttu-id="c956a-111">청사진 할당은 구독 범위에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c956a-111">Blueprint assignments exist at the subscription scope.</span></span>

## <span data-ttu-id="c956a-112">예제</span><span class="sxs-lookup"><span data-stu-id="c956a-112">EXAMPLES</span></span>

### <span data-ttu-id="c956a-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="c956a-113">Example 1</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -SubscriptionId "00000000-1111-0000-1111-000000000000"

Name              : Assignment-PS-BlueprintDefinition
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/Assignment-PS-BlueprintDefinition
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : AllResourcesReadOnly
ProvisioningState : Succeeded
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="c956a-114">지정된 구독 내에서 청사진 할당을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c956a-114">Get the blueprint assignments within the specified subscription.</span></span>

### <span data-ttu-id="c956a-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="c956a-115">Example 2</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myAssignmentName"
```

<span data-ttu-id="c956a-116">지정된 구독 내에서 지정된 이름으로 청사진 할당을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c956a-116">Get the blueprint assignment with the given name within the specified subscription.</span></span>

### <span data-ttu-id="c956a-117">예제 3</span><span class="sxs-lookup"><span data-stu-id="c956a-117">Example 3</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -ManagementGroupId "myManagementGroup"
```

<span data-ttu-id="c956a-118">지정된 관리 그룹 내에서 청사진 할당을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c956a-118">Get the blueprint assignments within the specified management group.</span></span>

### <span data-ttu-id="c956a-119">예제 4</span><span class="sxs-lookup"><span data-stu-id="c956a-119">Example 4</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -ManagementGroupId "myManagementGroup" -Name "myAssignmentName"
```

<span data-ttu-id="c956a-120">지정된 관리 그룹 내에서 지정된 이름으로 청사진 할당을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c956a-120">Get the blueprint assignment with the given name within the specified management group.</span></span>

## <span data-ttu-id="c956a-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c956a-121">PARAMETERS</span></span>

### <span data-ttu-id="c956a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c956a-122">-DefaultProfile</span></span>
<span data-ttu-id="c956a-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c956a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c956a-124">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="c956a-124">-ManagementGroupId</span></span>
<span data-ttu-id="c956a-125">청사진 할당이 저장되는 관리 그룹의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c956a-125">The ID of the management group where the Blueprint assignment is saved.</span></span>

```yaml
Type: System.String
Parameter Sets: ByManagementGroupAndName, ManagementGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c956a-126">-Name</span><span class="sxs-lookup"><span data-stu-id="c956a-126">-Name</span></span>
<span data-ttu-id="c956a-127">청사진 할당 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c956a-127">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionAndName, ByManagementGroupAndName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c956a-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c956a-128">-SubscriptionId</span></span>
<span data-ttu-id="c956a-129">청사진 할당이 배포된 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c956a-129">Subscription Id the blueprint assignment is deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionScope, BySubscriptionAndName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c956a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c956a-130">CommonParameters</span></span>
<span data-ttu-id="c956a-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c956a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c956a-132">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c956a-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c956a-133">입력</span><span class="sxs-lookup"><span data-stu-id="c956a-133">INPUTS</span></span>

### <span data-ttu-id="c956a-134">System.String</span><span class="sxs-lookup"><span data-stu-id="c956a-134">System.String</span></span>

## <span data-ttu-id="c956a-135">출력</span><span class="sxs-lookup"><span data-stu-id="c956a-135">OUTPUTS</span></span>

### <span data-ttu-id="c956a-136">System.Object</span><span class="sxs-lookup"><span data-stu-id="c956a-136">System.Object</span></span>
## <span data-ttu-id="c956a-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c956a-137">NOTES</span></span>

## <span data-ttu-id="c956a-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c956a-138">RELATED LINKS</span></span>
