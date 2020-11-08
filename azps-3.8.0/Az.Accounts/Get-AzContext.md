---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContext.md
ms.openlocfilehash: dab6388205c00ee457b7f8095f0f529f591b304f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043022"
---
# <span data-ttu-id="8c6d8-101">Get-AzContext</span><span class="sxs-lookup"><span data-stu-id="8c6d8-101">Get-AzContext</span></span>

## <span data-ttu-id="8c6d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c6d8-102">SYNOPSIS</span></span>
<span data-ttu-id="8c6d8-103">Azure Resource Manager 요청을 인증 하는 데 사용 되는 메타 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8c6d8-103">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

## <span data-ttu-id="8c6d8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8c6d8-104">SYNTAX</span></span>

### <span data-ttu-id="8c6d8-105">GetSingleContext (기본값)</span><span class="sxs-lookup"><span data-stu-id="8c6d8-105">GetSingleContext (Default)</span></span>
```
Get-AzContext [-DefaultProfile <IAzureContextContainer>] [[-Name] <String>] [<CommonParameters>]
```

### <span data-ttu-id="8c6d8-106">ListAllContexts</span><span class="sxs-lookup"><span data-stu-id="8c6d8-106">ListAllContexts</span></span>
```
Get-AzContext [-ListAvailable] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c6d8-107">설명은</span><span class="sxs-lookup"><span data-stu-id="8c6d8-107">DESCRIPTION</span></span>
<span data-ttu-id="8c6d8-108">Get-AzContext cmdlet은 Azure Resource Manager 요청을 인증 하는 데 사용 된 현재 메타 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8c6d8-108">The Get-AzContext cmdlet gets the current metadata used to authenticate Azure Resource Manager requests.</span></span>
<span data-ttu-id="8c6d8-109">이 cmdlet은 Active Directory 계정, Active Directory 테 넌 트, Azure 구독, 대상 Azure 환경을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8c6d8-109">This cmdlet gets the Active Directory account, Active Directory tenant, Azure subscription, and the targeted Azure environment.</span></span>
<span data-ttu-id="8c6d8-110">Azure resource manager cmdlet은 Azure Resource Manager 요청을 수행할 때 기본적으로 이러한 설정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c6d8-110">Azure Resource Manager cmdlets use these settings by default when making Azure Resource Manager requests.</span></span>

## <span data-ttu-id="8c6d8-111">예제의</span><span class="sxs-lookup"><span data-stu-id="8c6d8-111">EXAMPLES</span></span>

### <span data-ttu-id="8c6d8-112">예제 1: 현재 컨텍스트 가져오기</span><span class="sxs-lookup"><span data-stu-id="8c6d8-112">Example 1: Getting the current context</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzContext

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="8c6d8-113">이 예제에서는 AzAccount를 사용 하 여 Azure 구독이 있는 계정에 로그인 하 고, 이제 Get-AzContext를 호출 하 여 현재 세션의 컨텍스트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8c6d8-113">In this example we are logging into our account with an Azure subscription using Connect-AzAccount, and then we are getting the context of the current session by calling Get-AzContext.</span></span>

### <span data-ttu-id="8c6d8-114">예제 2: 사용 가능한 모든 컨텍스트 나열</span><span class="sxs-lookup"><span data-stu-id="8c6d8-114">Example 2: Listing all available contexts</span></span>
```
PS C:\> Get-AzContext -ListAvailable

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
Subscription2 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription2       AzureCloud          xxxxxxxx-x...
Subscription3 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription3       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="8c6d8-115">이 예제에서는 현재 사용 가능한 모든 컨텍스트가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8c6d8-115">In this example, all currently available contexts are displayed.</span></span>  <span data-ttu-id="8c6d8-116">사용자는 Select-AzContext를 사용 하 여 이러한 컨텍스트 중 하나를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8c6d8-116">The user may select one of these contexts using Select-AzContext.</span></span>

## <span data-ttu-id="8c6d8-117">변수</span><span class="sxs-lookup"><span data-stu-id="8c6d8-117">PARAMETERS</span></span>

### <span data-ttu-id="8c6d8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c6d8-118">-DefaultProfile</span></span>
<span data-ttu-id="8c6d8-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8c6d8-119">The credentials, account, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8c6d8-120">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="8c6d8-120">-ListAvailable</span></span>
<span data-ttu-id="8c6d8-121">현재 세션에서 사용 가능한 모든 컨텍스트를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c6d8-121">List all available contexts in the current session.</span></span>

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

### <span data-ttu-id="8c6d8-122">-이름</span><span class="sxs-lookup"><span data-stu-id="8c6d8-122">-Name</span></span>
<span data-ttu-id="8c6d8-123">컨텍스트 이름</span><span class="sxs-lookup"><span data-stu-id="8c6d8-123">The name of the context</span></span>

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

### <span data-ttu-id="8c6d8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c6d8-124">CommonParameters</span></span>
<span data-ttu-id="8c6d8-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c6d8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c6d8-126">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c6d8-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c6d8-127">입력</span><span class="sxs-lookup"><span data-stu-id="8c6d8-127">INPUTS</span></span>

### <span data-ttu-id="8c6d8-128">않아야</span><span class="sxs-lookup"><span data-stu-id="8c6d8-128">None</span></span>

## <span data-ttu-id="8c6d8-129">출력</span><span class="sxs-lookup"><span data-stu-id="8c6d8-129">OUTPUTS</span></span>

### <span data-ttu-id="8c6d8-130">Microsoft. Azure. a PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="8c6d8-130">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="8c6d8-131">상속자</span><span class="sxs-lookup"><span data-stu-id="8c6d8-131">NOTES</span></span>

## <span data-ttu-id="8c6d8-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8c6d8-132">RELATED LINKS</span></span>

[<span data-ttu-id="8c6d8-133">Set-AzContext</span><span class="sxs-lookup"><span data-stu-id="8c6d8-133">Set-AzContext</span></span>](./Set-AzContext.md)

