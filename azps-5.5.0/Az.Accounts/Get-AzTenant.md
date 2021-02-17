---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-aztenant
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzTenant.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzTenant.md
ms.openlocfilehash: 936eb5bb7f49c2530a325b3bfa8c369b8f097711
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190476"
---
# <span data-ttu-id="431a7-101">Get-AzTenant</span><span class="sxs-lookup"><span data-stu-id="431a7-101">Get-AzTenant</span></span>

## <span data-ttu-id="431a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="431a7-102">SYNOPSIS</span></span>
<span data-ttu-id="431a7-103">현재 사용자에 대해 권한이 부여된 테넌트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="431a7-103">Gets tenants that are authorized for the current user.</span></span>

## <span data-ttu-id="431a7-104">구문</span><span class="sxs-lookup"><span data-stu-id="431a7-104">SYNTAX</span></span>

```
Get-AzTenant [[-TenantId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="431a7-105">설명</span><span class="sxs-lookup"><span data-stu-id="431a7-105">DESCRIPTION</span></span>
<span data-ttu-id="431a7-106">Get-AzTenant cmdlet은 현재 사용자에 대한 권한이 부여된 테넌트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="431a7-106">The Get-AzTenant cmdlet gets tenants authorized for the current user.</span></span>

## <span data-ttu-id="431a7-107">예제</span><span class="sxs-lookup"><span data-stu-id="431a7-107">EXAMPLES</span></span>

### <span data-ttu-id="431a7-108">예제 1: 모든 테넌트 사용</span><span class="sxs-lookup"><span data-stu-id="431a7-108">Example 1: Getting all tenants</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzTenant

Id                                   Name        Category Domains
--                                   ----------- -------- -------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft   Home     {test0.com, test1.com, test2.microsoft.com, test3.microsoft.com...}
yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy Testhost    Home     testhost.onmicrosoft.com
```

<span data-ttu-id="431a7-109">이 예제에서는 Azure 계정의 권한이 부여된 모든 테넌트에 액세스하는 방법을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="431a7-109">This example shows how to get all of the authorized tenants of an Azure account.</span></span>

### <span data-ttu-id="431a7-110">예제 2: 특정 테넌트 사용</span><span class="sxs-lookup"><span data-stu-id="431a7-110">Example 2: Getting a specific tenant</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzTenant -TenantId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

Id                                   Name        Category Domains
--                                   ----------- -------- -------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft   Home     {test0.com, test1.com, test2.microsoft.com, test3.microsoft.com...}
```

<span data-ttu-id="431a7-111">이 예제에서는 Azure 계정의 권한이 부여된 특정 테넌트에 액세스하는 방법을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="431a7-111">This example shows how to get a specific authorized tenant of an Azure account.</span></span>

## <span data-ttu-id="431a7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="431a7-112">PARAMETERS</span></span>

### <span data-ttu-id="431a7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="431a7-113">-DefaultProfile</span></span>
<span data-ttu-id="431a7-114">Azure와의 통신에 사용되는 자격 증명, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="431a7-114">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="431a7-115">-TenantId</span><span class="sxs-lookup"><span data-stu-id="431a7-115">-TenantId</span></span>
<span data-ttu-id="431a7-116">이 cmdlet이 얻을 테넌트의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="431a7-116">Specifies the ID of the tenant that this cmdlet gets.</span></span>

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

### <span data-ttu-id="431a7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="431a7-117">CommonParameters</span></span>
<span data-ttu-id="431a7-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="431a7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="431a7-119">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="431a7-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="431a7-120">입력</span><span class="sxs-lookup"><span data-stu-id="431a7-120">INPUTS</span></span>

### <span data-ttu-id="431a7-121">System.String</span><span class="sxs-lookup"><span data-stu-id="431a7-121">System.String</span></span>

## <span data-ttu-id="431a7-122">출력</span><span class="sxs-lookup"><span data-stu-id="431a7-122">OUTPUTS</span></span>

### <span data-ttu-id="431a7-123">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="431a7-123">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span></span>

## <span data-ttu-id="431a7-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="431a7-124">NOTES</span></span>

## <span data-ttu-id="431a7-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="431a7-125">RELATED LINKS</span></span>
