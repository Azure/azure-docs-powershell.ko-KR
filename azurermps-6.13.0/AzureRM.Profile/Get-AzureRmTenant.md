---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermtenant
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmTenant.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmTenant.md
ms.openlocfilehash: 1d5312cfaf7afb96149ae00b0e7900905206fb3d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530133"
---
# <span data-ttu-id="e18fa-101">Get-AzureRmTenant</span><span class="sxs-lookup"><span data-stu-id="e18fa-101">Get-AzureRmTenant</span></span>

## <span data-ttu-id="e18fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e18fa-102">SYNOPSIS</span></span>
<span data-ttu-id="e18fa-103">현재 사용자에 대해 권한이 있는 테 넌 트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e18fa-103">Gets tenants that are authorized for the current user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e18fa-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e18fa-104">SYNTAX</span></span>

```
Get-AzureRmTenant [[-TenantId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e18fa-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e18fa-105">DESCRIPTION</span></span>
<span data-ttu-id="e18fa-106">Get-AzureRmTenant cmdlet은 현재 사용자에 대해 승인 된 테 넌 트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e18fa-106">The Get-AzureRmTenant cmdlet gets tenants authorized for the current user.</span></span>

## <span data-ttu-id="e18fa-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e18fa-107">EXAMPLES</span></span>

### <span data-ttu-id="e18fa-108">예제 1: 모든 테 넌 트 가져오기</span><span class="sxs-lookup"><span data-stu-id="e18fa-108">Example 1: Getting all tenants</span></span>
```
PS C:\> Connect-AzureRmAccount
PS C:\> Get-AzureRmTenant

Id                                   Directory
--                                   ---------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx microsoft.com
yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy microsoft.com
```

<span data-ttu-id="e18fa-109">이 예제에서는 Azure 계정의 모든 권한이 부여 된 테 넌 트를 가져오는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e18fa-109">This example shows how to get all of the authorized tenants of an Azure account.</span></span>

### <span data-ttu-id="e18fa-110">예제 2: 특정 테 넌 트 가져오기</span><span class="sxs-lookup"><span data-stu-id="e18fa-110">Example 2: Getting a specific tenant</span></span>
```
PS C:\> Connect-AzureRmAccount
PS C:\> Get-AzureRmTenant -TenantId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

Id                                   Directory
--                                   ---------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx microsoft.com
```

<span data-ttu-id="e18fa-111">이 예제에서는 Azure 계정에 대해 권한이 부여 된 특정 테 넌 트를 가져오는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e18fa-111">This example shows how to get a specific authorized tenant of an Azure account.</span></span>

## <span data-ttu-id="e18fa-112">변수</span><span class="sxs-lookup"><span data-stu-id="e18fa-112">PARAMETERS</span></span>

### <span data-ttu-id="e18fa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e18fa-113">-DefaultProfile</span></span>
<span data-ttu-id="e18fa-114">Azure와 통신 하는 데 사용 되는 자격 증명, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e18fa-114">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e18fa-115">-TenantId</span><span class="sxs-lookup"><span data-stu-id="e18fa-115">-TenantId</span></span>
<span data-ttu-id="e18fa-116">이 cmdlet이 가져오는 테 넌 트의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e18fa-116">Specifies the ID of the tenant that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Domain, Tenant

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e18fa-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e18fa-117">CommonParameters</span></span>
<span data-ttu-id="e18fa-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e18fa-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e18fa-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e18fa-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e18fa-120">입력</span><span class="sxs-lookup"><span data-stu-id="e18fa-120">INPUTS</span></span>

### <span data-ttu-id="e18fa-121">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e18fa-121">System.String</span></span>

## <span data-ttu-id="e18fa-122">출력</span><span class="sxs-lookup"><span data-stu-id="e18fa-122">OUTPUTS</span></span>

### <span data-ttu-id="e18fa-123">PSAzureTenant (. \*)</span><span class="sxs-lookup"><span data-stu-id="e18fa-123">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span></span>

## <span data-ttu-id="e18fa-124">상속자</span><span class="sxs-lookup"><span data-stu-id="e18fa-124">NOTES</span></span>

## <span data-ttu-id="e18fa-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e18fa-125">RELATED LINKS</span></span>
