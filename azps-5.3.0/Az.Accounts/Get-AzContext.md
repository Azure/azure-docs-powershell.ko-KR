---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContext.md
ms.openlocfilehash: dab6388205c00ee457b7f8095f0f529f591b304f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494559"
---
# <span data-ttu-id="d72b7-101">Get-AzContext</span><span class="sxs-lookup"><span data-stu-id="d72b7-101">Get-AzContext</span></span>

## <span data-ttu-id="d72b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d72b7-102">SYNOPSIS</span></span>
<span data-ttu-id="d72b7-103">Azure Resource Manager 요청을 인증하는 데 사용되는 메타데이터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d72b7-103">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

## <span data-ttu-id="d72b7-104">구문</span><span class="sxs-lookup"><span data-stu-id="d72b7-104">SYNTAX</span></span>

### <span data-ttu-id="d72b7-105">GetSingleContext(기본값)</span><span class="sxs-lookup"><span data-stu-id="d72b7-105">GetSingleContext (Default)</span></span>
```
Get-AzContext [-DefaultProfile <IAzureContextContainer>] [[-Name] <String>] [<CommonParameters>]
```

### <span data-ttu-id="d72b7-106">ListAllContexts</span><span class="sxs-lookup"><span data-stu-id="d72b7-106">ListAllContexts</span></span>
```
Get-AzContext [-ListAvailable] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d72b7-107">설명</span><span class="sxs-lookup"><span data-stu-id="d72b7-107">DESCRIPTION</span></span>
<span data-ttu-id="d72b7-108">Get-AzContext cmdlet은 Azure Resource Manager 요청을 인증하는 데 사용되는 현재 메타데이터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d72b7-108">The Get-AzContext cmdlet gets the current metadata used to authenticate Azure Resource Manager requests.</span></span>
<span data-ttu-id="d72b7-109">이 cmdlet은 Active Directory 계정, Active Directory 테넌트, Azure 구독 및 대상 Azure 환경을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d72b7-109">This cmdlet gets the Active Directory account, Active Directory tenant, Azure subscription, and the targeted Azure environment.</span></span>
<span data-ttu-id="d72b7-110">Azure Resource Manager cmdlet은 Azure Resource Manager 요청을 만들 때 기본적으로 이러한 설정을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="d72b7-110">Azure Resource Manager cmdlets use these settings by default when making Azure Resource Manager requests.</span></span>

## <span data-ttu-id="d72b7-111">예제</span><span class="sxs-lookup"><span data-stu-id="d72b7-111">EXAMPLES</span></span>

### <span data-ttu-id="d72b7-112">예제 1: 현재 컨텍스트를</span><span class="sxs-lookup"><span data-stu-id="d72b7-112">Example 1: Getting the current context</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzContext

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="d72b7-113">이 예제에서는 Connect-AzAccount를 사용하여 Azure 구독으로 계정에 로그인한 다음 Get-AzContext를 호출하여 현재 세션의 컨텍스트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d72b7-113">In this example we are logging into our account with an Azure subscription using Connect-AzAccount, and then we are getting the context of the current session by calling Get-AzContext.</span></span>

### <span data-ttu-id="d72b7-114">예제 2: 사용 가능한 모든 컨텍스트 나열</span><span class="sxs-lookup"><span data-stu-id="d72b7-114">Example 2: Listing all available contexts</span></span>
```
PS C:\> Get-AzContext -ListAvailable

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
Subscription2 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription2       AzureCloud          xxxxxxxx-x...
Subscription3 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription3       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="d72b7-115">이 예제에서는 현재 사용 가능한 모든 컨텍스트가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d72b7-115">In this example, all currently available contexts are displayed.</span></span>  <span data-ttu-id="d72b7-116">사용자는 Select-AzContext를 사용하여 이러한 컨텍스트 중 하나를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d72b7-116">The user may select one of these contexts using Select-AzContext.</span></span>

## <span data-ttu-id="d72b7-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d72b7-117">PARAMETERS</span></span>

### <span data-ttu-id="d72b7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d72b7-118">-DefaultProfile</span></span>
<span data-ttu-id="d72b7-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d72b7-119">The credentials, account, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d72b7-120">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="d72b7-120">-ListAvailable</span></span>
<span data-ttu-id="d72b7-121">현재 세션에서 사용 가능한 모든 컨텍스트를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="d72b7-121">List all available contexts in the current session.</span></span>

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

### <span data-ttu-id="d72b7-122">-Name</span><span class="sxs-lookup"><span data-stu-id="d72b7-122">-Name</span></span>
<span data-ttu-id="d72b7-123">컨텍스트의 이름</span><span class="sxs-lookup"><span data-stu-id="d72b7-123">The name of the context</span></span>

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

### <span data-ttu-id="d72b7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d72b7-124">CommonParameters</span></span>
<span data-ttu-id="d72b7-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d72b7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d72b7-126">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d72b7-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d72b7-127">입력</span><span class="sxs-lookup"><span data-stu-id="d72b7-127">INPUTS</span></span>

### <span data-ttu-id="d72b7-128">없음</span><span class="sxs-lookup"><span data-stu-id="d72b7-128">None</span></span>

## <span data-ttu-id="d72b7-129">출력</span><span class="sxs-lookup"><span data-stu-id="d72b7-129">OUTPUTS</span></span>

### <span data-ttu-id="d72b7-130">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="d72b7-130">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="d72b7-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d72b7-131">NOTES</span></span>

## <span data-ttu-id="d72b7-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d72b7-132">RELATED LINKS</span></span>

[<span data-ttu-id="d72b7-133">Set-AzContext</span><span class="sxs-lookup"><span data-stu-id="d72b7-133">Set-AzContext</span></span>](./Set-AzContext.md)

