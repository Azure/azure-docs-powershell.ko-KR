---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermtenant
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmTenant.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmTenant.md
ms.openlocfilehash: 7d9687877e3a27d175719a7a7b9ec6c78a529e52
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532708"
---
# <span data-ttu-id="ce278-101">Get-AzureRmTenant</span><span class="sxs-lookup"><span data-stu-id="ce278-101">Get-AzureRmTenant</span></span>

## <span data-ttu-id="ce278-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce278-102">SYNOPSIS</span></span>
<span data-ttu-id="ce278-103">현재 사용자에 대해 권한이 있는 테 넌 트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ce278-103">Gets tenants that are authorized for the current user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce278-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ce278-104">SYNTAX</span></span>

```
Get-AzureRmTenant [[-TenantId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce278-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ce278-105">DESCRIPTION</span></span>
<span data-ttu-id="ce278-106">Get-AzureRmTenant cmdlet은 현재 사용자에 대해 승인 된 테 넌 트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ce278-106">The Get-AzureRmTenant cmdlet gets tenants authorized for the current user.</span></span>

## <span data-ttu-id="ce278-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ce278-107">EXAMPLES</span></span>

### <span data-ttu-id="ce278-108">예제 1: 모든 테 넌 트 가져오기</span><span class="sxs-lookup"><span data-stu-id="ce278-108">Example 1: Getting all tenants</span></span>
```
PS C:\> Connect-AzureRmAccount
PS C:\> Get-AzureRmTenant

TenantId : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Domain   : microsoft.com

TenantId : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Domain   : microsoft.com
```

<span data-ttu-id="ce278-109">이 예제에서는 Azure 계정의 모든 권한이 부여 된 테 넌 트를 가져오는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ce278-109">This example shows how to get all of the authorized tenants of an Azure account.</span></span>

### <span data-ttu-id="ce278-110">예제 2: 특정 테 넌 트 가져오기</span><span class="sxs-lookup"><span data-stu-id="ce278-110">Example 2: Getting a specific tenant</span></span>
```
PS C:\> Connect-AzureRmAccount
PS C:\> Get-AzureRmTenant -TenantId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

TenantId : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Domain   : microsoft.com
```

<span data-ttu-id="ce278-111">이 예제에서는 Azure 계정에 대해 권한이 부여 된 특정 테 넌 트를 가져오는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ce278-111">This example shows how to get a specific authorized tenant of an Azure account.</span></span>

## <span data-ttu-id="ce278-112">변수</span><span class="sxs-lookup"><span data-stu-id="ce278-112">PARAMETERS</span></span>

### <span data-ttu-id="ce278-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce278-113">-DefaultProfile</span></span>
<span data-ttu-id="ce278-114">Azure와 통신 하는 데 사용 되는 자격 증명, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ce278-114">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ce278-115">-TenantId</span><span class="sxs-lookup"><span data-stu-id="ce278-115">-TenantId</span></span>
<span data-ttu-id="ce278-116">이 cmdlet이 가져오는 테 넌 트의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce278-116">Specifies the ID of the tenant that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ce278-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce278-117">CommonParameters</span></span>
<span data-ttu-id="ce278-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce278-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce278-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce278-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce278-120">입력</span><span class="sxs-lookup"><span data-stu-id="ce278-120">INPUTS</span></span>

### <span data-ttu-id="ce278-121">않아야</span><span class="sxs-lookup"><span data-stu-id="ce278-121">None</span></span>
<span data-ttu-id="ce278-122">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ce278-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ce278-123">출력</span><span class="sxs-lookup"><span data-stu-id="ce278-123">OUTPUTS</span></span>

### <span data-ttu-id="ce278-124">PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="ce278-124">PSAzureTenant</span></span>
<span data-ttu-id="ce278-125">이 cmdlet은 현재 계정에 대해 승인 된 테 넌 트 ID 및 연결 된 도메인 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce278-125">This cmdlet returns the tenant ID and associated domain information for tenants authorized for the current account.</span></span>

## <span data-ttu-id="ce278-126">상속자</span><span class="sxs-lookup"><span data-stu-id="ce278-126">NOTES</span></span>

## <span data-ttu-id="ce278-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ce278-127">RELATED LINKS</span></span>

