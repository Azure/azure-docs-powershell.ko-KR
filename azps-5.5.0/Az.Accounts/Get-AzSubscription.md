---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzSubscription.md
ms.openlocfilehash: aecdd4a0b5f0ef4465f08441841fb923a273afdf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190481"
---
# <span data-ttu-id="1f857-101">Get-AzSubscription</span><span class="sxs-lookup"><span data-stu-id="1f857-101">Get-AzSubscription</span></span>

## <span data-ttu-id="1f857-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f857-102">SYNOPSIS</span></span>
<span data-ttu-id="1f857-103">현재 계정이 액세스할 수 있는 구독을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1f857-103">Get subscriptions that the current account can access.</span></span>

## <span data-ttu-id="1f857-104">구문</span><span class="sxs-lookup"><span data-stu-id="1f857-104">SYNTAX</span></span>

### <span data-ttu-id="1f857-105">ListByIdInTenant(기본값)</span><span class="sxs-lookup"><span data-stu-id="1f857-105">ListByIdInTenant (Default)</span></span>
```
Get-AzSubscription [-SubscriptionId <String>] [-TenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f857-106">ListByNameInTenant</span><span class="sxs-lookup"><span data-stu-id="1f857-106">ListByNameInTenant</span></span>
```
Get-AzSubscription [-SubscriptionName <String>] [-TenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f857-107">설명</span><span class="sxs-lookup"><span data-stu-id="1f857-107">DESCRIPTION</span></span>
<span data-ttu-id="1f857-108">Get-AzSubscription cmdlet은 현재 계정이 액세스할 수 있는 구독에 대한 구독 ID, 구독 이름 및 홈 테넌트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1f857-108">The Get-AzSubscription cmdlet gets the subscription ID, subscription name, and home tenant for subscriptions that the current account can access.</span></span>

## <span data-ttu-id="1f857-109">예제</span><span class="sxs-lookup"><span data-stu-id="1f857-109">EXAMPLES</span></span>

### <span data-ttu-id="1f857-110">예제 1: 모든 테넌트의 모든 구독을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1f857-110">Example 1: Get all subscriptions in all tenants</span></span>
```
PS C:\>Get-AzSubscription

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription3                      zzzz-zzzz-zzzz-zzzz     bbbb-bbbb-bbbb-bbbb             Enabled
```

<span data-ttu-id="1f857-111">이 명령은 현재 계정에 대해 권한이 부여된 모든 테넌트의 모든 구독을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1f857-111">This command gets all subscriptions in all tenants that are authorized for the current account.</span></span>

### <span data-ttu-id="1f857-112">예제 2: 특정 테넌트에 대한 모든 구독을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1f857-112">Example 2: Get all subscriptions for a specific tenant</span></span>
```
PS C:\>Get-AzSubscription -TenantId "aaaa-aaaa-aaaa-aaaa"

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
```

<span data-ttu-id="1f857-113">현재 계정에 대해 권한이 부여된 주어진 테넌트의 모든 구독을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="1f857-113">List all subscriptions in the given tenant that are authorized for the current account.</span></span>

### <span data-ttu-id="1f857-114">예제 3: 현재 테넌트의 모든 구독을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1f857-114">Example 3: Get all subscriptions in the current tenant</span></span>
```
PS C:\>Get-AzSubscription

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
```

<span data-ttu-id="1f857-115">이 명령은 현재 사용자에 대해 권한이 부여된 현재 테넌트의 모든 구독을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1f857-115">This command gets all subscriptions in the current tenant that are authorized for the current user.</span></span>

### <span data-ttu-id="1f857-116">예제 4: 특정 구독을 사용하여 현재 컨텍스트 변경</span><span class="sxs-lookup"><span data-stu-id="1f857-116">Example 4: Change the current context to use a specific subscription</span></span>
```
PS C:\>Get-AzSubscription -SubscriptionId "xxxx-xxxx-xxxx-xxxx" -TenantId "yyyy-yyyy-yyyy-yyyy" | Set-AzContext

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxx-xxxx-xxxx-xxxx)      azureuser@micros... Subscription1       AzureCloud          yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="1f857-117">이 명령은 지정된 구독을 얻은 다음, 사용할 현재 컨텍스트를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="1f857-117">This command gets the specified subscription, and then sets the current context to use it.</span></span> <span data-ttu-id="1f857-118">이 세션의 모든 후속 cmdlet은 기본적으로 새 구독(Contoso 구독 1)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f857-118">All subsequent cmdlets in this session use the new subscription (Contoso Subscription 1) by default.</span></span>

## <span data-ttu-id="1f857-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1f857-119">PARAMETERS</span></span>

### <span data-ttu-id="1f857-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1f857-120">-AsJob</span></span>
<span data-ttu-id="1f857-121">백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="1f857-121">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="1f857-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f857-122">-DefaultProfile</span></span>
<span data-ttu-id="1f857-123">Azure와의 통신에 사용되는 자격 증명, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="1f857-123">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1f857-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1f857-124">-SubscriptionId</span></span>
<span data-ttu-id="1f857-125">얻을 구독의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1f857-125">Specifies the ID of the subscription to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByIdInTenant
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f857-126">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="1f857-126">-SubscriptionName</span></span>
<span data-ttu-id="1f857-127">얻을 구독의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1f857-127">Specifies the name of the subscription to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByNameInTenant
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f857-128">-TenantId</span><span class="sxs-lookup"><span data-stu-id="1f857-128">-TenantId</span></span>
<span data-ttu-id="1f857-129">얻을 구독이 포함된 테넌트의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1f857-129">Specifies the ID of the tenant that contains subscriptions to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f857-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f857-130">CommonParameters</span></span>
<span data-ttu-id="1f857-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1f857-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f857-132">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1f857-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f857-133">입력</span><span class="sxs-lookup"><span data-stu-id="1f857-133">INPUTS</span></span>

### <span data-ttu-id="1f857-134">System.String</span><span class="sxs-lookup"><span data-stu-id="1f857-134">System.String</span></span>

## <span data-ttu-id="1f857-135">출력</span><span class="sxs-lookup"><span data-stu-id="1f857-135">OUTPUTS</span></span>

### <span data-ttu-id="1f857-136">Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="1f857-136">Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="1f857-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1f857-137">NOTES</span></span>

## <span data-ttu-id="1f857-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1f857-138">RELATED LINKS</span></span>
