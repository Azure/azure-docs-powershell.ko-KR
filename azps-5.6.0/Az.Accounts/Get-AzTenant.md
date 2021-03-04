---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/get-aztenant
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzTenant.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzTenant.md
ms.openlocfilehash: 4ef371f26eeca71edda42a6aca5e7d5ad28fe753
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955035"
---
# <span data-ttu-id="e1ce2-101">Get-AzTenant</span><span class="sxs-lookup"><span data-stu-id="e1ce2-101">Get-AzTenant</span></span>

## <span data-ttu-id="e1ce2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1ce2-102">SYNOPSIS</span></span>
<span data-ttu-id="e1ce2-103">현재 사용자에 대한 권한이 부여된 테넌트가 도착합니다.</span><span class="sxs-lookup"><span data-stu-id="e1ce2-103">Gets tenants that are authorized for the current user.</span></span>

## <span data-ttu-id="e1ce2-104">구문</span><span class="sxs-lookup"><span data-stu-id="e1ce2-104">SYNTAX</span></span>

```
Get-AzTenant [[-TenantId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1ce2-105">설명</span><span class="sxs-lookup"><span data-stu-id="e1ce2-105">DESCRIPTION</span></span>
<span data-ttu-id="e1ce2-106">Get-AzTenant cmdlet은 현재 사용자에 대한 권한이 부여된 테넌트가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e1ce2-106">The Get-AzTenant cmdlet gets tenants authorized for the current user.</span></span>

## <span data-ttu-id="e1ce2-107">예제</span><span class="sxs-lookup"><span data-stu-id="e1ce2-107">EXAMPLES</span></span>

### <span data-ttu-id="e1ce2-108">예제 1: 모든 테넌트 사용</span><span class="sxs-lookup"><span data-stu-id="e1ce2-108">Example 1: Getting all tenants</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzTenant

Id                                   Name        Category Domains
--                                   ----------- -------- -------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft   Home     {test0.com, test1.com, test2.microsoft.com, test3.microsoft.com...}
yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy Testhost    Home     testhost.onmicrosoft.com
```

<span data-ttu-id="e1ce2-109">이 예제에서는 Azure 계정의 권한이 부여된 모든 테넌트를 얻을 수 있는 방법을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e1ce2-109">This example shows how to get all of the authorized tenants of an Azure account.</span></span>

### <span data-ttu-id="e1ce2-110">예제 2: 특정 테넌트 점점</span><span class="sxs-lookup"><span data-stu-id="e1ce2-110">Example 2: Getting a specific tenant</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzTenant -TenantId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

Id                                   Name        Category Domains
--                                   ----------- -------- -------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft   Home     {test0.com, test1.com, test2.microsoft.com, test3.microsoft.com...}
```

<span data-ttu-id="e1ce2-111">이 예제에서는 Azure 계정의 특정 권한이 부여된 테넌트를 구하는 방법을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e1ce2-111">This example shows how to get a specific authorized tenant of an Azure account.</span></span>

## <span data-ttu-id="e1ce2-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e1ce2-112">PARAMETERS</span></span>

### <span data-ttu-id="e1ce2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1ce2-113">-DefaultProfile</span></span>
<span data-ttu-id="e1ce2-114">Azure와의 통신에 사용되는 자격 증명, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e1ce2-114">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e1ce2-115">-TenantId</span><span class="sxs-lookup"><span data-stu-id="e1ce2-115">-TenantId</span></span>
<span data-ttu-id="e1ce2-116">이 cmdlet이 얻을 테넌트의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e1ce2-116">Specifies the ID of the tenant that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e1ce2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1ce2-117">CommonParameters</span></span>
<span data-ttu-id="e1ce2-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e1ce2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1ce2-119">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e1ce2-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1ce2-120">입력</span><span class="sxs-lookup"><span data-stu-id="e1ce2-120">INPUTS</span></span>

### <span data-ttu-id="e1ce2-121">System.String</span><span class="sxs-lookup"><span data-stu-id="e1ce2-121">System.String</span></span>

## <span data-ttu-id="e1ce2-122">출력</span><span class="sxs-lookup"><span data-stu-id="e1ce2-122">OUTPUTS</span></span>

### <span data-ttu-id="e1ce2-123">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="e1ce2-123">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span></span>

## <span data-ttu-id="e1ce2-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e1ce2-124">NOTES</span></span>

## <span data-ttu-id="e1ce2-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e1ce2-125">RELATED LINKS</span></span>
