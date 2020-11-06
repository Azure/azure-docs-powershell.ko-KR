---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmContext.md
ms.openlocfilehash: dbe93ca98fe8cf7a0a22f2b52a17a17e7222c261
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527803"
---
# <span data-ttu-id="7165d-101">Get-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="7165d-101">Get-AzureRmContext</span></span>

## <span data-ttu-id="7165d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7165d-102">SYNOPSIS</span></span>
<span data-ttu-id="7165d-103">Azure Resource Manager 요청을 인증 하는 데 사용 되는 메타 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7165d-103">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7165d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7165d-104">SYNTAX</span></span>

### <span data-ttu-id="7165d-105">GetSingleContext (기본값)</span><span class="sxs-lookup"><span data-stu-id="7165d-105">GetSingleContext (Default)</span></span>
```
Get-AzureRmContext [-DefaultProfile <IAzureContextContainer>] [[-Name] <String>] [<CommonParameters>]
```

### <span data-ttu-id="7165d-106">ListAllContexts</span><span class="sxs-lookup"><span data-stu-id="7165d-106">ListAllContexts</span></span>
```
Get-AzureRmContext [-ListAvailable] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7165d-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7165d-107">DESCRIPTION</span></span>
<span data-ttu-id="7165d-108">Get-AzureRmContext cmdlet은 Azure Resource Manager 요청을 인증 하는 데 사용 된 현재 메타 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7165d-108">The Get-AzureRmContext cmdlet gets the current metadata used to authenticate Azure Resource Manager requests.</span></span>
<span data-ttu-id="7165d-109">이 cmdlet은 Active Directory 계정, Active Directory 테 넌 트, Azure 구독, 대상 Azure 환경을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7165d-109">This cmdlet gets the Active Directory account, Active Directory tenant, Azure subscription, and the targeted Azure environment.</span></span>
<span data-ttu-id="7165d-110">Azure resource manager cmdlet은 Azure Resource Manager 요청을 수행할 때 기본적으로 이러한 설정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7165d-110">Azure Resource Manager cmdlets use these settings by default when making Azure Resource Manager requests.</span></span>

## <span data-ttu-id="7165d-111">예제의</span><span class="sxs-lookup"><span data-stu-id="7165d-111">EXAMPLES</span></span>

### <span data-ttu-id="7165d-112">예제 1: 현재 컨텍스트 가져오기</span><span class="sxs-lookup"><span data-stu-id="7165d-112">Example 1: Getting the current context</span></span>
```
PS C:\> Connect-AzureRmAccount
PS C:\> Get-AzureRmContext

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="7165d-113">이 예제에서는 AzureRmAccount를 사용 하 여 Azure 구독이 있는 계정에 로그인 하 고, 이제 Get-AzureRmContext를 호출 하 여 현재 세션의 컨텍스트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7165d-113">In this example we are logging into our account with an Azure subscription using Connect-AzureRmAccount, and then we are getting the context of the current session by calling Get-AzureRmContext.</span></span>

### <span data-ttu-id="7165d-114">예제 2: 사용 가능한 모든 컨텍스트 나열</span><span class="sxs-lookup"><span data-stu-id="7165d-114">Example 2: Listing all available contexts</span></span>
```
PS C:\> Get-AzureRmContext -ListAvailable

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
Subscription2 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription2       AzureCloud          xxxxxxxx-x...
Subscription3 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription3       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="7165d-115">이 예제에서는 현재 사용 가능한 모든 컨텍스트가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7165d-115">In this example, all currently available contexts are displayed.</span></span>  <span data-ttu-id="7165d-116">사용자는 Select-AzureRmContext를 사용 하 여 이러한 컨텍스트 중 하나를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7165d-116">The user may select one of these contexts using Select-AzureRmContext.</span></span>

## <span data-ttu-id="7165d-117">변수</span><span class="sxs-lookup"><span data-stu-id="7165d-117">PARAMETERS</span></span>

### <span data-ttu-id="7165d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7165d-118">-DefaultProfile</span></span>
<span data-ttu-id="7165d-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="7165d-119">The credentials, account, tenant and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7165d-120">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="7165d-120">-ListAvailable</span></span>
<span data-ttu-id="7165d-121">현재 세션에서 사용 가능한 모든 컨텍스트를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="7165d-121">List all available contexts in the current session.</span></span>

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

### <span data-ttu-id="7165d-122">-이름</span><span class="sxs-lookup"><span data-stu-id="7165d-122">-Name</span></span>
<span data-ttu-id="7165d-123">컨텍스트 이름</span><span class="sxs-lookup"><span data-stu-id="7165d-123">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: GetSingleContext
Aliases:
Accepted values: Default

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7165d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7165d-124">CommonParameters</span></span>
<span data-ttu-id="7165d-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7165d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7165d-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7165d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7165d-127">입력</span><span class="sxs-lookup"><span data-stu-id="7165d-127">INPUTS</span></span>

### <span data-ttu-id="7165d-128">않아야</span><span class="sxs-lookup"><span data-stu-id="7165d-128">None</span></span>

## <span data-ttu-id="7165d-129">출력</span><span class="sxs-lookup"><span data-stu-id="7165d-129">OUTPUTS</span></span>

### <span data-ttu-id="7165d-130">Microsoft. Azure. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="7165d-130">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="7165d-131">상속자</span><span class="sxs-lookup"><span data-stu-id="7165d-131">NOTES</span></span>

## <span data-ttu-id="7165d-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7165d-132">RELATED LINKS</span></span>

[<span data-ttu-id="7165d-133">Set-AzureRMContext</span><span class="sxs-lookup"><span data-stu-id="7165d-133">Set-AzureRMContext</span></span>](./Set-AzureRMContext.md)

