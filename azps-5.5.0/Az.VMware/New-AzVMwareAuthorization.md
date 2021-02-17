---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/new-azvmwareauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwareAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwareAuthorization.md
ms.openlocfilehash: 394975e341d52fb0067b420397189b0a8858cfcd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190521"
---
# <span data-ttu-id="2d0bf-101">New-AzVMwareAuthorization</span><span class="sxs-lookup"><span data-stu-id="2d0bf-101">New-AzVMwareAuthorization</span></span>

## <span data-ttu-id="2d0bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d0bf-102">SYNOPSIS</span></span>
<span data-ttu-id="2d0bf-103">사설 클라우드에서 ExpressRoute 회로 권한 부여 만들기 또는 업데이트</span><span class="sxs-lookup"><span data-stu-id="2d0bf-103">Create or update an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="2d0bf-104">구문</span><span class="sxs-lookup"><span data-stu-id="2d0bf-104">SYNTAX</span></span>

```
New-AzVMwareAuthorization -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="2d0bf-105">설명</span><span class="sxs-lookup"><span data-stu-id="2d0bf-105">DESCRIPTION</span></span>
<span data-ttu-id="2d0bf-106">사설 클라우드에서 ExpressRoute 회로 권한 부여 만들기 또는 업데이트</span><span class="sxs-lookup"><span data-stu-id="2d0bf-106">Create or update an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="2d0bf-107">예제</span><span class="sxs-lookup"><span data-stu-id="2d0bf-107">EXAMPLES</span></span>

### <span data-ttu-id="2d0bf-108">예제 1: 자동화 만들기</span><span class="sxs-lookup"><span data-stu-id="2d0bf-108">Example 1: Create autorization</span></span>
```powershell
PS C:\> New-AzVMwareAuthorization -Name azps-test-auth -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="2d0bf-109">이 cmdlet은 사설 `azps-test-auth` 클라우드에서 권한 부여를 만듭니다. `azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="2d0bf-109">This cmdlet creates authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

## <span data-ttu-id="2d0bf-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2d0bf-110">PARAMETERS</span></span>

### <span data-ttu-id="2d0bf-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2d0bf-111">-AsJob</span></span>
<span data-ttu-id="2d0bf-112">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="2d0bf-112">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d0bf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d0bf-113">-DefaultProfile</span></span>
<span data-ttu-id="2d0bf-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2d0bf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d0bf-115">-Name</span><span class="sxs-lookup"><span data-stu-id="2d0bf-115">-Name</span></span>
<span data-ttu-id="2d0bf-116">사설 클라우드의 ExpressRoute 회로 권한 부여 이름</span><span class="sxs-lookup"><span data-stu-id="2d0bf-116">Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d0bf-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2d0bf-117">-NoWait</span></span>
<span data-ttu-id="2d0bf-118">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="2d0bf-118">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d0bf-119">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="2d0bf-119">-PrivateCloudName</span></span>
<span data-ttu-id="2d0bf-120">사설 클라우드의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2d0bf-120">The name of the private cloud.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d0bf-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d0bf-121">-ResourceGroupName</span></span>
<span data-ttu-id="2d0bf-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2d0bf-122">The name of the resource group.</span></span>
<span data-ttu-id="2d0bf-123">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="2d0bf-123">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d0bf-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2d0bf-124">-SubscriptionId</span></span>
<span data-ttu-id="2d0bf-125">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2d0bf-125">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d0bf-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2d0bf-126">-Confirm</span></span>
<span data-ttu-id="2d0bf-127">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2d0bf-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d0bf-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d0bf-128">-WhatIf</span></span>
<span data-ttu-id="2d0bf-129">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="2d0bf-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d0bf-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2d0bf-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d0bf-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d0bf-131">CommonParameters</span></span>
<span data-ttu-id="2d0bf-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2d0bf-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d0bf-133">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2d0bf-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d0bf-134">입력</span><span class="sxs-lookup"><span data-stu-id="2d0bf-134">INPUTS</span></span>

## <span data-ttu-id="2d0bf-135">출력</span><span class="sxs-lookup"><span data-stu-id="2d0bf-135">OUTPUTS</span></span>

### <span data-ttu-id="2d0bf-136">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IExpressRouteAuthorization</span><span class="sxs-lookup"><span data-stu-id="2d0bf-136">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IExpressRouteAuthorization</span></span>

## <span data-ttu-id="2d0bf-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2d0bf-137">NOTES</span></span>

<span data-ttu-id="2d0bf-138">별칭</span><span class="sxs-lookup"><span data-stu-id="2d0bf-138">ALIASES</span></span>

## <span data-ttu-id="2d0bf-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2d0bf-139">RELATED LINKS</span></span>

