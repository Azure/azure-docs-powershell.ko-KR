---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmContext.md
ms.openlocfilehash: 96b9b5a6bec10082d7b004dcede73b743a7e538b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534768"
---
# <span data-ttu-id="46371-101">Get-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="46371-101">Get-AzureRmContext</span></span>

## <span data-ttu-id="46371-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46371-102">SYNOPSIS</span></span>
<span data-ttu-id="46371-103">Azure Resource Manager 요청을 인증 하는 데 사용 되는 메타 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="46371-103">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46371-104">구문과</span><span class="sxs-lookup"><span data-stu-id="46371-104">SYNTAX</span></span>

### <span data-ttu-id="46371-105">GetSingleContext (기본값)</span><span class="sxs-lookup"><span data-stu-id="46371-105">GetSingleContext (Default)</span></span>
```
Get-AzureRmContext [-DefaultProfile <IAzureContextContainer>] [[-Name] <String>] [<CommonParameters>]
```

### <span data-ttu-id="46371-106">ListAllContexts</span><span class="sxs-lookup"><span data-stu-id="46371-106">ListAllContexts</span></span>
```
Get-AzureRmContext [-ListAvailable] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46371-107">설명은</span><span class="sxs-lookup"><span data-stu-id="46371-107">DESCRIPTION</span></span>
<span data-ttu-id="46371-108">Get-AzureRmContext cmdlet은 Azure Resource Manager 요청을 인증 하는 데 사용 된 현재 메타 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="46371-108">The Get-AzureRmContext cmdlet gets the current metadata used to authenticate Azure Resource Manager requests.</span></span>

<span data-ttu-id="46371-109">이 cmdlet은 Active Directory 계정, Active Directory 테 넌 트, Azure 구독, 대상 Azure 환경을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="46371-109">This cmdlet gets the Active Directory account, Active Directory tenant, Azure subscription, and the targeted Azure environment.</span></span>
<span data-ttu-id="46371-110">Azure resource manager cmdlet은 Azure Resource Manager 요청을 수행할 때 기본적으로 이러한 설정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="46371-110">Azure Resource Manager cmdlets use these settings by default when making Azure Resource Manager requests.</span></span>

## <span data-ttu-id="46371-111">예제의</span><span class="sxs-lookup"><span data-stu-id="46371-111">EXAMPLES</span></span>

### <span data-ttu-id="46371-112">예제 1: 현재 컨텍스트 가져오기</span><span class="sxs-lookup"><span data-stu-id="46371-112">Example 1: Getting the current context</span></span>
```
PS C:\> Connect-AzureRmAccount
PS C:\> Get-AzureRmContext

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="46371-113">이 예제에서는 AzureRmAccount를 사용 하 여 Azure 구독이 있는 계정에 로그인 하 고, 이제 Get-AzureRmContext를 호출 하 여 현재 세션의 컨텍스트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="46371-113">In this example we are logging into our account with an Azure subscription using Connect-AzureRmAccount, and then we are getting the context of the current session by calling Get-AzureRmContext.</span></span>

### <span data-ttu-id="46371-114">예제 2: 사용 가능한 모든 컨텍스트 나열</span><span class="sxs-lookup"><span data-stu-id="46371-114">Example 2: Listing all available contexts</span></span>
```
PS C:\> Get-AzureRmContext -ListAvailable

Name                  : Test
Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :

Name                  : Production
Environment           : AzureCloud
Account               : prod@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Production Subscription
CurrentStorageAccount :
```

<span data-ttu-id="46371-115">이 예제에서는 현재 사용 가능한 모든 컨텍스트가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="46371-115">In this example, all currently available contexts are displayed.</span></span>  <span data-ttu-id="46371-116">사용자는 Select-AzureRmContext를 사용 하 여 이러한 컨텍스트 중 하나를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46371-116">The user may select one of these contexts using Select-AzureRmContext.</span></span>

## <span data-ttu-id="46371-117">변수</span><span class="sxs-lookup"><span data-stu-id="46371-117">PARAMETERS</span></span>

### <span data-ttu-id="46371-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46371-118">-DefaultProfile</span></span>
<span data-ttu-id="46371-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="46371-119">The credentials, account, tenant and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46371-120">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="46371-120">-ListAvailable</span></span>
<span data-ttu-id="46371-121">현재 세션에서 사용 가능한 모든 컨텍스트를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="46371-121">List all available contexts in the current session.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ListAllContexts
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46371-122">-이름</span><span class="sxs-lookup"><span data-stu-id="46371-122">-Name</span></span>
<span data-ttu-id="46371-123">컨텍스트 이름</span><span class="sxs-lookup"><span data-stu-id="46371-123">The name of the context</span></span>

```yaml
Type: String
Parameter Sets: GetSingleContext
Aliases: 
Accepted values: Default

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46371-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46371-124">CommonParameters</span></span>
<span data-ttu-id="46371-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="46371-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46371-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46371-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46371-127">입력</span><span class="sxs-lookup"><span data-stu-id="46371-127">INPUTS</span></span>

### <span data-ttu-id="46371-128">않아야</span><span class="sxs-lookup"><span data-stu-id="46371-128">None</span></span>
<span data-ttu-id="46371-129">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="46371-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="46371-130">출력</span><span class="sxs-lookup"><span data-stu-id="46371-130">OUTPUTS</span></span>

### <span data-ttu-id="46371-131">PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="46371-131">PSAzureContext</span></span>
<span data-ttu-id="46371-132">이 cmdlet은 Azure Resource Manager cmdlet에 사용 되는 계정, 테 넌 트 및 구독을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="46371-132">This cmdlet returns the account, tenant, and subscription used by Azure Resource Manager cmdlets.</span></span>

## <span data-ttu-id="46371-133">상속자</span><span class="sxs-lookup"><span data-stu-id="46371-133">NOTES</span></span>

## <span data-ttu-id="46371-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="46371-134">RELATED LINKS</span></span>

[<span data-ttu-id="46371-135">Set-AzureRMContext</span><span class="sxs-lookup"><span data-stu-id="46371-135">Set-AzureRMContext</span></span>](./Set-AzureRMContext.md)

