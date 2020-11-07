---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintAssignment.md
ms.openlocfilehash: 0e3d08384383f858ed65c30637e7321663344959
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93877386"
---
# <span data-ttu-id="a087c-101">Get-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="a087c-101">Get-AzBlueprintAssignment</span></span>

## <span data-ttu-id="a087c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a087c-102">SYNOPSIS</span></span>
<span data-ttu-id="a087c-103">하나 이상의 청사진 과제를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a087c-103">Get one or more blueprint assignments.</span></span>

## <span data-ttu-id="a087c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a087c-104">SYNTAX</span></span>

### <span data-ttu-id="a087c-105">BlueprintAssignmentsBySubscription (기본값)</span><span class="sxs-lookup"><span data-stu-id="a087c-105">BlueprintAssignmentsBySubscription (Default)</span></span>
```
Get-AzBlueprintAssignment [[-SubscriptionId] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a087c-106">BlueprintAssignmentByName</span><span class="sxs-lookup"><span data-stu-id="a087c-106">BlueprintAssignmentByName</span></span>
```
Get-AzBlueprintAssignment [[-SubscriptionId] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a087c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a087c-107">DESCRIPTION</span></span>
<span data-ttu-id="a087c-108">하나 이상의 청사진 과제를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a087c-108">Get one or more blueprint assignments.</span></span> <span data-ttu-id="a087c-109">구독 범위에는 청사진 배정이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a087c-109">Blueprint assignments exist at the subscription scope.</span></span>

## <span data-ttu-id="a087c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="a087c-110">EXAMPLES</span></span>

### <span data-ttu-id="a087c-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="a087c-111">Example 1</span></span>
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

<span data-ttu-id="a087c-112">지정 된 구독 내에서 청사진 과제를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a087c-112">Get the blueprint assignments within the specified subscription.</span></span>

### <span data-ttu-id="a087c-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="a087c-113">Example 2</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myAssignmentName"
```

<span data-ttu-id="a087c-114">지정 된 구독 내에서 주어진 이름으로 청사진 과제를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a087c-114">Get the blueprint assignment with the given name within the specified subscription.</span></span>

## <span data-ttu-id="a087c-115">변수</span><span class="sxs-lookup"><span data-stu-id="a087c-115">PARAMETERS</span></span>

### <span data-ttu-id="a087c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a087c-116">-DefaultProfile</span></span>
<span data-ttu-id="a087c-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a087c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a087c-118">-이름</span><span class="sxs-lookup"><span data-stu-id="a087c-118">-Name</span></span>
<span data-ttu-id="a087c-119">청사진 과제 이름.</span><span class="sxs-lookup"><span data-stu-id="a087c-119">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: BlueprintAssignmentByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a087c-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a087c-120">-SubscriptionId</span></span>
<span data-ttu-id="a087c-121">청사진 배정이 배포 되는 구독 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="a087c-121">Subscription Id the blueprint assignment is deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a087c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a087c-122">CommonParameters</span></span>
<span data-ttu-id="a087c-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a087c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a087c-124">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a087c-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a087c-125">입력</span><span class="sxs-lookup"><span data-stu-id="a087c-125">INPUTS</span></span>

### <span data-ttu-id="a087c-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a087c-126">System.String</span></span>

## <span data-ttu-id="a087c-127">출력</span><span class="sxs-lookup"><span data-stu-id="a087c-127">OUTPUTS</span></span>

### <span data-ttu-id="a087c-128">System. 개체</span><span class="sxs-lookup"><span data-stu-id="a087c-128">System.Object</span></span>
## <span data-ttu-id="a087c-129">상속자</span><span class="sxs-lookup"><span data-stu-id="a087c-129">NOTES</span></span>

## <span data-ttu-id="a087c-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a087c-130">RELATED LINKS</span></span>
