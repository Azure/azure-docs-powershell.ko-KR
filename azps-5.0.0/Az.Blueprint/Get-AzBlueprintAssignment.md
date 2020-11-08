---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintAssignment.md
ms.openlocfilehash: 06398b9c5e880577606e0367722fc22c242d58f4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216112"
---
# <span data-ttu-id="0b708-101">Get-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="0b708-101">Get-AzBlueprintAssignment</span></span>

## <span data-ttu-id="0b708-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b708-102">SYNOPSIS</span></span>
<span data-ttu-id="0b708-103">하나 이상의 청사진 과제를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0b708-103">Get one or more blueprint assignments.</span></span>

## <span data-ttu-id="0b708-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0b708-104">SYNTAX</span></span>

### <span data-ttu-id="0b708-105">구독 범위 (기본값)</span><span class="sxs-lookup"><span data-stu-id="0b708-105">SubscriptionScope (Default)</span></span>
```
Get-AzBlueprintAssignment [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0b708-106">BySubscriptionAndName</span><span class="sxs-lookup"><span data-stu-id="0b708-106">BySubscriptionAndName</span></span>
```
Get-AzBlueprintAssignment -Name <String> [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0b708-107">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="0b708-107">ByManagementGroupAndName</span></span>
```
Get-AzBlueprintAssignment -Name <String> -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0b708-108">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="0b708-108">ManagementGroupScope</span></span>
```
Get-AzBlueprintAssignment -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0b708-109">설명은</span><span class="sxs-lookup"><span data-stu-id="0b708-109">DESCRIPTION</span></span>
<span data-ttu-id="0b708-110">하나 이상의 청사진 과제를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0b708-110">Get one or more blueprint assignments.</span></span> <span data-ttu-id="0b708-111">구독 범위에는 청사진 배정이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0b708-111">Blueprint assignments exist at the subscription scope.</span></span>

## <span data-ttu-id="0b708-112">예제의</span><span class="sxs-lookup"><span data-stu-id="0b708-112">EXAMPLES</span></span>

### <span data-ttu-id="0b708-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="0b708-113">Example 1</span></span>
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

<span data-ttu-id="0b708-114">지정 된 구독 내에서 청사진 과제를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0b708-114">Get the blueprint assignments within the specified subscription.</span></span>

### <span data-ttu-id="0b708-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="0b708-115">Example 2</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myAssignmentName"
```

<span data-ttu-id="0b708-116">지정 된 구독 내에서 주어진 이름으로 청사진 과제를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0b708-116">Get the blueprint assignment with the given name within the specified subscription.</span></span>

### <span data-ttu-id="0b708-117">예제 3</span><span class="sxs-lookup"><span data-stu-id="0b708-117">Example 3</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -ManagementGroupId "myManagementGroup"
```

<span data-ttu-id="0b708-118">지정 된 관리 그룹 내에서 청사진 과제를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0b708-118">Get the blueprint assignments within the specified management group.</span></span>

### <span data-ttu-id="0b708-119">예제 4</span><span class="sxs-lookup"><span data-stu-id="0b708-119">Example 4</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -ManagementGroupId "myManagementGroup" -Name "myAssignmentName"
```

<span data-ttu-id="0b708-120">지정 된 관리 그룹 내에서 주어진 이름으로 청사진 과제를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0b708-120">Get the blueprint assignment with the given name within the specified management group.</span></span>

## <span data-ttu-id="0b708-121">변수</span><span class="sxs-lookup"><span data-stu-id="0b708-121">PARAMETERS</span></span>

### <span data-ttu-id="0b708-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b708-122">-DefaultProfile</span></span>
<span data-ttu-id="0b708-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0b708-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b708-124">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="0b708-124">-ManagementGroupId</span></span>
<span data-ttu-id="0b708-125">청사진 배정이 저장 된 관리 그룹의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0b708-125">The ID of the management group where the Blueprint assignment is saved.</span></span>

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

### <span data-ttu-id="0b708-126">-이름</span><span class="sxs-lookup"><span data-stu-id="0b708-126">-Name</span></span>
<span data-ttu-id="0b708-127">청사진 과제 이름.</span><span class="sxs-lookup"><span data-stu-id="0b708-127">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="0b708-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0b708-128">-SubscriptionId</span></span>
<span data-ttu-id="0b708-129">청사진 배정이 배포 되는 구독 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="0b708-129">Subscription Id the blueprint assignment is deployed to.</span></span>

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

### <span data-ttu-id="0b708-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b708-130">CommonParameters</span></span>
<span data-ttu-id="0b708-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b708-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b708-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0b708-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b708-133">입력</span><span class="sxs-lookup"><span data-stu-id="0b708-133">INPUTS</span></span>

### <span data-ttu-id="0b708-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0b708-134">System.String</span></span>

## <span data-ttu-id="0b708-135">출력</span><span class="sxs-lookup"><span data-stu-id="0b708-135">OUTPUTS</span></span>

### <span data-ttu-id="0b708-136">System. 개체</span><span class="sxs-lookup"><span data-stu-id="0b708-136">System.Object</span></span>
## <span data-ttu-id="0b708-137">상속자</span><span class="sxs-lookup"><span data-stu-id="0b708-137">NOTES</span></span>

## <span data-ttu-id="0b708-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0b708-138">RELATED LINKS</span></span>
