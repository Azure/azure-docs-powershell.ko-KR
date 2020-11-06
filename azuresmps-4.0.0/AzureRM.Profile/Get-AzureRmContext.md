---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 914b75e3952f7841aaf3ff505f51f7b4ebdc6044
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523403"
---
# <span data-ttu-id="0045c-101">Get-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="0045c-101">Get-AzureRmContext</span></span>

## <span data-ttu-id="0045c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0045c-102">SYNOPSIS</span></span>
<span data-ttu-id="0045c-103">Azure Resource Manager 요청을 인증 하는 데 사용 되는 메타 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0045c-103">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

## <span data-ttu-id="0045c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0045c-104">SYNTAX</span></span>

```
Get-AzureRmContext [<CommonParameters>]
```

## <span data-ttu-id="0045c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0045c-105">DESCRIPTION</span></span>
<span data-ttu-id="0045c-106">Get-AzureRmContext cmdlet은 Azure Resource Manager 요청을 인증 하는 데 사용 된 현재 메타 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0045c-106">The Get-AzureRmContext cmdlet gets the current metadata used to authenticate Azure Resource Manager requests.</span></span>

<span data-ttu-id="0045c-107">이 cmdlet은 Active Directory 계정, Active Directory 테 넌 트, Azure 구독, 대상 Azure 환경을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0045c-107">This cmdlet gets the Active Directory account, Active Directory tenant, Azure subscription, and the targeted Azure environment.</span></span>
<span data-ttu-id="0045c-108">Azure resource manager cmdlet은 Azure Resource Manager 요청을 수행할 때 기본적으로 이러한 설정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0045c-108">Azure Resource Manager cmdlets use these settings by default when making Azure Resource Manager requests.</span></span>

## <span data-ttu-id="0045c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="0045c-109">EXAMPLES</span></span>

### <span data-ttu-id="0045c-110">예제 1: 현재 컨텍스트 가져오기</span><span class="sxs-lookup"><span data-stu-id="0045c-110">Example 1: Getting the current context</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmContext

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="0045c-111">이 예제에서는 AzureRmAccount를 사용 하 여 Azure 구독이 있는 계정에 로그인 하 고, 이제 Get-AzureRmContext를 호출 하 여 현재 세션의 컨텍스트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0045c-111">In this example we are logging into our account with an Azure subscription using Add-AzureRmAccount, and then we are getting the context of the current session by calling Get-AzureRmContext.</span></span>

## <span data-ttu-id="0045c-112">변수</span><span class="sxs-lookup"><span data-stu-id="0045c-112">PARAMETERS</span></span>

### <span data-ttu-id="0045c-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0045c-113">CommonParameters</span></span>
<span data-ttu-id="0045c-114">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0045c-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0045c-115">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0045c-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0045c-116">입력</span><span class="sxs-lookup"><span data-stu-id="0045c-116">INPUTS</span></span>

## <span data-ttu-id="0045c-117">출력</span><span class="sxs-lookup"><span data-stu-id="0045c-117">OUTPUTS</span></span>

### <span data-ttu-id="0045c-118">PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="0045c-118">PSAzureContext</span></span>
<span data-ttu-id="0045c-119">이 cmdlet은 Azure Resource Manager cmdlet에 사용 되는 계정, 테 넌 트 및 구독을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0045c-119">This cmdlet returns the account, tenant, and subscription used by Azure Resource Manager cmdlets.</span></span>

## <span data-ttu-id="0045c-120">상속자</span><span class="sxs-lookup"><span data-stu-id="0045c-120">NOTES</span></span>

## <span data-ttu-id="0045c-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0045c-121">RELATED LINKS</span></span>

[<span data-ttu-id="0045c-122">Set-AzureRMContext</span><span class="sxs-lookup"><span data-stu-id="0045c-122">Set-AzureRMContext</span></span>]()

