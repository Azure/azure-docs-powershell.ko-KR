---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/powershell/module/az.subscription/update-azsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Update-AzSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Update-AzSubscription.md
ms.openlocfilehash: 0fe030e3ef4dfcb8e43ba436d37d582871e55a5b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976139"
---
# <span data-ttu-id="b6a9d-101">Update-AzSubscription</span><span class="sxs-lookup"><span data-stu-id="b6a9d-101">Update-AzSubscription</span></span>

## <span data-ttu-id="b6a9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6a9d-102">SYNOPSIS</span></span>
<span data-ttu-id="b6a9d-103">Azure 구독 업데이트</span><span class="sxs-lookup"><span data-stu-id="b6a9d-103">Updates an Azure Subscription</span></span>

## <span data-ttu-id="b6a9d-104">구문</span><span class="sxs-lookup"><span data-stu-id="b6a9d-104">SYNTAX</span></span>

```
Update-AzSubscription -SubscriptionId <String> -Action <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6a9d-105">설명</span><span class="sxs-lookup"><span data-stu-id="b6a9d-105">DESCRIPTION</span></span>
<span data-ttu-id="b6a9d-106">**Update-AzSubscription** cmdlet은 Azure 구독을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="b6a9d-106">The **Update-AzSubscription** cmdlet updates an Azure subscription</span></span>

## <span data-ttu-id="b6a9d-107">예제</span><span class="sxs-lookup"><span data-stu-id="b6a9d-107">EXAMPLES</span></span>

### <span data-ttu-id="b6a9d-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b6a9d-108">Example 1</span></span>
```powershell
PS C:\> Update-AzSubscription -SubscriptionId "86869d42-1782-4337-98b0-c905fb937d46" -Action "Cancel"

Name        : My Subscription
Id          : 86869d42-1782-4337-98b0-c905fb937d46
TenantId    : a5dcb057-fd83-4384-9d49-5198004d33a5
State       : Enabled
```

<span data-ttu-id="b6a9d-109">구독 업데이트</span><span class="sxs-lookup"><span data-stu-id="b6a9d-109">Updates the subscription</span></span>

## <span data-ttu-id="b6a9d-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b6a9d-110">PARAMETERS</span></span>

### <span data-ttu-id="b6a9d-111">-Action</span><span class="sxs-lookup"><span data-stu-id="b6a9d-111">-Action</span></span>
<span data-ttu-id="b6a9d-112">구독에서 수행할 작업</span><span class="sxs-lookup"><span data-stu-id="b6a9d-112">Action to perform on subscription</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6a9d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b6a9d-113">-AsJob</span></span>
<span data-ttu-id="b6a9d-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="b6a9d-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6a9d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6a9d-115">-DefaultProfile</span></span>
<span data-ttu-id="b6a9d-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b6a9d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6a9d-117">-Name</span><span class="sxs-lookup"><span data-stu-id="b6a9d-117">-Name</span></span>
<span data-ttu-id="b6a9d-118">구독 이름</span><span class="sxs-lookup"><span data-stu-id="b6a9d-118">Name of the subscription</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6a9d-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b6a9d-119">-SubscriptionId</span></span>
<span data-ttu-id="b6a9d-120">업데이트할 구독 ID</span><span class="sxs-lookup"><span data-stu-id="b6a9d-120">Subscription Id to update</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6a9d-121">-확인</span><span class="sxs-lookup"><span data-stu-id="b6a9d-121">-Confirm</span></span>
<span data-ttu-id="b6a9d-122">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b6a9d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6a9d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6a9d-123">-WhatIf</span></span>
<span data-ttu-id="b6a9d-124">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="b6a9d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6a9d-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b6a9d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6a9d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6a9d-126">CommonParameters</span></span>
<span data-ttu-id="b6a9d-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b6a9d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6a9d-128">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b6a9d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6a9d-129">입력</span><span class="sxs-lookup"><span data-stu-id="b6a9d-129">INPUTS</span></span>

### <span data-ttu-id="b6a9d-130">없음</span><span class="sxs-lookup"><span data-stu-id="b6a9d-130">None</span></span>

## <span data-ttu-id="b6a9d-131">출력</span><span class="sxs-lookup"><span data-stu-id="b6a9d-131">OUTPUTS</span></span>

### <span data-ttu-id="b6a9d-132">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="b6a9d-132">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="b6a9d-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b6a9d-133">NOTES</span></span>

## <span data-ttu-id="b6a9d-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b6a9d-134">RELATED LINKS</span></span>
