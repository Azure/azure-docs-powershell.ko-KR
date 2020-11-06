---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2cabb88c490c7fdea56fd5ffde280cfd55bc8f3d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523396"
---
# <span data-ttu-id="cc94a-101">Get-AzureRmTenant</span><span class="sxs-lookup"><span data-stu-id="cc94a-101">Get-AzureRmTenant</span></span>

## <span data-ttu-id="cc94a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc94a-102">SYNOPSIS</span></span>
<span data-ttu-id="cc94a-103">현재 사용자에 대해 권한이 있는 테 넌 트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cc94a-103">Gets tenants that are authorized for the current user.</span></span>

## <span data-ttu-id="cc94a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cc94a-104">SYNTAX</span></span>

```
Get-AzureRmTenant [[-TenantId] <String>] [<CommonParameters>]
```

## <span data-ttu-id="cc94a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cc94a-105">DESCRIPTION</span></span>
<span data-ttu-id="cc94a-106">Get-AzureRmTenant cmdlet은 현재 사용자에 대해 승인 된 테 넌 트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cc94a-106">The Get-AzureRmTenant cmdlet gets tenants authorized for the current user.</span></span>

## <span data-ttu-id="cc94a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="cc94a-107">EXAMPLES</span></span>

### <span data-ttu-id="cc94a-108">예제 1: 모든 테 넌 트 가져오기</span><span class="sxs-lookup"><span data-stu-id="cc94a-108">Example 1: Getting all tenants</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmTenant

TenantId : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Domain   : microsoft.com

TenantId : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Domain   : microsoft.com
```

<span data-ttu-id="cc94a-109">이 예제에서는 Azure 계정의 모든 권한이 부여 된 테 넌 트를 가져오는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cc94a-109">This example shows how to get all of the authorized tenants of an Azure account.</span></span>

### <span data-ttu-id="cc94a-110">예제 2: 특정 테 넌 트 가져오기</span><span class="sxs-lookup"><span data-stu-id="cc94a-110">Example 2: Getting a specific tenant</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmTenant -TenantId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

TenantId : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Domain   : microsoft.com
```

<span data-ttu-id="cc94a-111">이 예제에서는 Azure 계정에 대해 권한이 부여 된 특정 테 넌 트를 가져오는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cc94a-111">This example shows how to get a specific authorized tenant of an Azure account.</span></span>

## <span data-ttu-id="cc94a-112">변수</span><span class="sxs-lookup"><span data-stu-id="cc94a-112">PARAMETERS</span></span>

### <span data-ttu-id="cc94a-113">-TenantId</span><span class="sxs-lookup"><span data-stu-id="cc94a-113">-TenantId</span></span>
<span data-ttu-id="cc94a-114">이 cmdlet이 가져오는 테 넌 트의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc94a-114">Specifies the ID of the tenant that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Domain, Tenant

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc94a-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc94a-115">CommonParameters</span></span>
<span data-ttu-id="cc94a-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc94a-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc94a-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc94a-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc94a-118">입력</span><span class="sxs-lookup"><span data-stu-id="cc94a-118">INPUTS</span></span>

## <span data-ttu-id="cc94a-119">출력</span><span class="sxs-lookup"><span data-stu-id="cc94a-119">OUTPUTS</span></span>

### <span data-ttu-id="cc94a-120">PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="cc94a-120">PSAzureTenant</span></span>
<span data-ttu-id="cc94a-121">이 cmdlet은 현재 계정에 대해 승인 된 테 넌 트 ID 및 연결 된 도메인 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc94a-121">This cmdlet returns the tenant ID and associated domain information for tenants authorized for the current account.</span></span>

## <span data-ttu-id="cc94a-122">상속자</span><span class="sxs-lookup"><span data-stu-id="cc94a-122">NOTES</span></span>

## <span data-ttu-id="cc94a-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cc94a-123">RELATED LINKS</span></span>

