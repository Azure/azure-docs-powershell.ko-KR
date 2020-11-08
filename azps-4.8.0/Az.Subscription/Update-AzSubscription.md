---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/update-azsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Update-AzSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Update-AzSubscription.md
ms.openlocfilehash: b83d186089558b18cbd511cdc5d0b407a997f635
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204704"
---
# <span data-ttu-id="8dadc-101">Update-AzSubscription</span><span class="sxs-lookup"><span data-stu-id="8dadc-101">Update-AzSubscription</span></span>

## <span data-ttu-id="8dadc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8dadc-102">SYNOPSIS</span></span>
<span data-ttu-id="8dadc-103">Azure 구독 업데이트</span><span class="sxs-lookup"><span data-stu-id="8dadc-103">Updates an Azure Subscription</span></span>

## <span data-ttu-id="8dadc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8dadc-104">SYNTAX</span></span>

```
Update-AzSubscription -SubscriptionId <String> -Action <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8dadc-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8dadc-105">DESCRIPTION</span></span>
<span data-ttu-id="8dadc-106">**업데이트 AzSubscription** Cmdlet은 Azure 구독을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8dadc-106">The **Update-AzSubscription** cmdlet updates an Azure subscription</span></span>

## <span data-ttu-id="8dadc-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8dadc-107">EXAMPLES</span></span>

### <span data-ttu-id="8dadc-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="8dadc-108">Example 1</span></span>
```powershell
PS C:\> Update-AzSubscription -SubscriptionId "86869d42-1782-4337-98b0-c905fb937d46" -Action "Cancel"

Name        : My Subscription
Id          : 86869d42-1782-4337-98b0-c905fb937d46
TenantId    : a5dcb057-fd83-4384-9d49-5198004d33a5
State       : Enabled

```
<span data-ttu-id="8dadc-109">구독 업데이트</span><span class="sxs-lookup"><span data-stu-id="8dadc-109">Updates the subscription</span></span>

## <span data-ttu-id="8dadc-110">변수</span><span class="sxs-lookup"><span data-stu-id="8dadc-110">PARAMETERS</span></span>

### <span data-ttu-id="8dadc-111">-작업</span><span class="sxs-lookup"><span data-stu-id="8dadc-111">-Action</span></span>
<span data-ttu-id="8dadc-112">구독에 수행할 작업</span><span class="sxs-lookup"><span data-stu-id="8dadc-112">Action to perform on subscription</span></span>

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

### <span data-ttu-id="8dadc-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8dadc-113">-AsJob</span></span>
<span data-ttu-id="8dadc-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="8dadc-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8dadc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dadc-115">-DefaultProfile</span></span>
<span data-ttu-id="8dadc-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8dadc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8dadc-117">-이름</span><span class="sxs-lookup"><span data-stu-id="8dadc-117">-Name</span></span>
<span data-ttu-id="8dadc-118">구독 이름</span><span class="sxs-lookup"><span data-stu-id="8dadc-118">Name of the subscription</span></span>

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

### <span data-ttu-id="8dadc-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8dadc-119">-SubscriptionId</span></span>
<span data-ttu-id="8dadc-120">업데이트할 구독 Id</span><span class="sxs-lookup"><span data-stu-id="8dadc-120">Subscription Id to update</span></span>

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

### <span data-ttu-id="8dadc-121">-확인</span><span class="sxs-lookup"><span data-stu-id="8dadc-121">-Confirm</span></span>
<span data-ttu-id="8dadc-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8dadc-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8dadc-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8dadc-123">-WhatIf</span></span>
<span data-ttu-id="8dadc-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8dadc-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8dadc-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8dadc-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8dadc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dadc-126">CommonParameters</span></span>
<span data-ttu-id="8dadc-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8dadc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dadc-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8dadc-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dadc-129">입력</span><span class="sxs-lookup"><span data-stu-id="8dadc-129">INPUTS</span></span>

### <span data-ttu-id="8dadc-130">않아야</span><span class="sxs-lookup"><span data-stu-id="8dadc-130">None</span></span>

## <span data-ttu-id="8dadc-131">출력</span><span class="sxs-lookup"><span data-stu-id="8dadc-131">OUTPUTS</span></span>

### <span data-ttu-id="8dadc-132">PSAzureSubscription에 대 한.</span><span class="sxs-lookup"><span data-stu-id="8dadc-132">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="8dadc-133">상속자</span><span class="sxs-lookup"><span data-stu-id="8dadc-133">NOTES</span></span>

## <span data-ttu-id="8dadc-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8dadc-134">RELATED LINKS</span></span>
