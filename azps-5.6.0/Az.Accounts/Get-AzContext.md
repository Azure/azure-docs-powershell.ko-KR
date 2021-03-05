---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/get-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContext.md
ms.openlocfilehash: 2060a1cbe9f002a20b94e82ac9547c5fc96c0e07
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010128"
---
# <span data-ttu-id="12dc8-101">Get-AzContext</span><span class="sxs-lookup"><span data-stu-id="12dc8-101">Get-AzContext</span></span>

## <span data-ttu-id="12dc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12dc8-102">SYNOPSIS</span></span>
<span data-ttu-id="12dc8-103">Azure Resource Manager 요청을 인증하는 데 사용되는 메타데이터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="12dc8-103">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

## <span data-ttu-id="12dc8-104">구문</span><span class="sxs-lookup"><span data-stu-id="12dc8-104">SYNTAX</span></span>

### <span data-ttu-id="12dc8-105">GetSingleContext(기본값)</span><span class="sxs-lookup"><span data-stu-id="12dc8-105">GetSingleContext (Default)</span></span>
```
Get-AzContext [-DefaultProfile <IAzureContextContainer>] [[-Name] <String>] [<CommonParameters>]
```

### <span data-ttu-id="12dc8-106">ListAllContexts</span><span class="sxs-lookup"><span data-stu-id="12dc8-106">ListAllContexts</span></span>
```
Get-AzContext [-ListAvailable] [-RefreshContextFromTokenCache] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="12dc8-107">설명</span><span class="sxs-lookup"><span data-stu-id="12dc8-107">DESCRIPTION</span></span>
<span data-ttu-id="12dc8-108">Get-AzContext cmdlet은 Azure Resource Manager 요청을 인증하는 데 사용되는 현재 메타데이터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="12dc8-108">The Get-AzContext cmdlet gets the current metadata used to authenticate Azure Resource Manager requests.</span></span>
<span data-ttu-id="12dc8-109">이 cmdlet은 Active Directory 계정, Active Directory 테넌트, Azure 구독 및 대상 Azure 환경을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="12dc8-109">This cmdlet gets the Active Directory account, Active Directory tenant, Azure subscription, and the targeted Azure environment.</span></span>
<span data-ttu-id="12dc8-110">Azure Resource Manager cmdlet은 Azure Resource Manager 요청을 만들 때 기본적으로 이러한 설정을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="12dc8-110">Azure Resource Manager cmdlets use these settings by default when making Azure Resource Manager requests.</span></span>

## <span data-ttu-id="12dc8-111">예제</span><span class="sxs-lookup"><span data-stu-id="12dc8-111">EXAMPLES</span></span>

### <span data-ttu-id="12dc8-112">예제 1: 현재 컨텍스트를</span><span class="sxs-lookup"><span data-stu-id="12dc8-112">Example 1: Getting the current context</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzContext

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="12dc8-113">이 예제에서는 Connect-AzAccount를 사용하여 Azure 구독으로 계정에 로그인한 다음 Get-AzContext를 호출하여 현재 세션의 컨텍스트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="12dc8-113">In this example we are logging into our account with an Azure subscription using Connect-AzAccount, and then we are getting the context of the current session by calling Get-AzContext.</span></span>

### <span data-ttu-id="12dc8-114">예제 2: 사용 가능한 모든 컨텍스트 나열</span><span class="sxs-lookup"><span data-stu-id="12dc8-114">Example 2: Listing all available contexts</span></span>
```
PS C:\> Get-AzContext -ListAvailable

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
Subscription2 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription2       AzureCloud          xxxxxxxx-x...
Subscription3 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription3       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="12dc8-115">이 예제에서는 현재 사용 가능한 모든 컨텍스트가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="12dc8-115">In this example, all currently available contexts are displayed.</span></span>  <span data-ttu-id="12dc8-116">사용자는 Select-AzContext를 사용하여 이러한 컨텍스트 중 하나를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="12dc8-116">The user may select one of these contexts using Select-AzContext.</span></span>

## <span data-ttu-id="12dc8-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="12dc8-117">PARAMETERS</span></span>

### <span data-ttu-id="12dc8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12dc8-118">-DefaultProfile</span></span>
<span data-ttu-id="12dc8-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="12dc8-119">The credentials, account, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="12dc8-120">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="12dc8-120">-ListAvailable</span></span>
<span data-ttu-id="12dc8-121">현재 세션에서 사용 가능한 모든 컨텍스트를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="12dc8-121">List all available contexts in the current session.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListAllContexts
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12dc8-122">-Name</span><span class="sxs-lookup"><span data-stu-id="12dc8-122">-Name</span></span>
<span data-ttu-id="12dc8-123">컨텍스트의 이름</span><span class="sxs-lookup"><span data-stu-id="12dc8-123">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: GetSingleContext
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12dc8-124">-RefreshContextFromTokenCache</span><span class="sxs-lookup"><span data-stu-id="12dc8-124">-RefreshContextFromTokenCache</span></span>
<span data-ttu-id="12dc8-125">토큰 캐시에서 컨텍스트 새로 고침</span><span class="sxs-lookup"><span data-stu-id="12dc8-125">Refresh contexts from token cache</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListAllContexts
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12dc8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12dc8-126">CommonParameters</span></span>
<span data-ttu-id="12dc8-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="12dc8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12dc8-128">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="12dc8-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12dc8-129">입력</span><span class="sxs-lookup"><span data-stu-id="12dc8-129">INPUTS</span></span>

### <span data-ttu-id="12dc8-130">없음</span><span class="sxs-lookup"><span data-stu-id="12dc8-130">None</span></span>

## <span data-ttu-id="12dc8-131">출력</span><span class="sxs-lookup"><span data-stu-id="12dc8-131">OUTPUTS</span></span>

### <span data-ttu-id="12dc8-132">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="12dc8-132">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="12dc8-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="12dc8-133">NOTES</span></span>

## <span data-ttu-id="12dc8-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="12dc8-134">RELATED LINKS</span></span>

[<span data-ttu-id="12dc8-135">Set-AzContext</span><span class="sxs-lookup"><span data-stu-id="12dc8-135">Set-AzContext</span></span>](./Set-AzContext.md)

