---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/new-azvmwareauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWareAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWareAuthorization.md
ms.openlocfilehash: b1e8ca1e5140470524ec83656ef0042bafa494b7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213443"
---
# <span data-ttu-id="69277-101">New-AzVMWareAuthorization</span><span class="sxs-lookup"><span data-stu-id="69277-101">New-AzVMWareAuthorization</span></span>

## <span data-ttu-id="69277-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69277-102">SYNOPSIS</span></span>
<span data-ttu-id="69277-103">사설 클라우드에서 Express 경로에 대 한 회로 권한 부여 만들기 또는 업데이트</span><span class="sxs-lookup"><span data-stu-id="69277-103">Create or update an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="69277-104">구문과</span><span class="sxs-lookup"><span data-stu-id="69277-104">SYNTAX</span></span>

```
New-AzVMWareAuthorization -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="69277-105">설명은</span><span class="sxs-lookup"><span data-stu-id="69277-105">DESCRIPTION</span></span>
<span data-ttu-id="69277-106">사설 클라우드에서 Express 경로에 대 한 회로 권한 부여 만들기 또는 업데이트</span><span class="sxs-lookup"><span data-stu-id="69277-106">Create or update an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="69277-107">예제의</span><span class="sxs-lookup"><span data-stu-id="69277-107">EXAMPLES</span></span>

### <span data-ttu-id="69277-108">예제 1: autorization 만들기</span><span class="sxs-lookup"><span data-stu-id="69277-108">Example 1: Create autorization</span></span>
```powershell
PS C:\> New-AzVMWareAuthorization -Name azps-test-auth -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="69277-109">이 cmdlet은 사설 클라우드에서 권한 부여를 만듭니다. `azps-test-auth``azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="69277-109">This cmdlet creates authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

## <span data-ttu-id="69277-110">변수</span><span class="sxs-lookup"><span data-stu-id="69277-110">PARAMETERS</span></span>

### <span data-ttu-id="69277-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="69277-111">-AsJob</span></span>
<span data-ttu-id="69277-112">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="69277-112">Run the command as a job</span></span>

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

### <span data-ttu-id="69277-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69277-113">-DefaultProfile</span></span>
<span data-ttu-id="69277-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="69277-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69277-115">-이름</span><span class="sxs-lookup"><span data-stu-id="69277-115">-Name</span></span>
<span data-ttu-id="69277-116">사설 클라우드의 Express 경로 인증의 이름</span><span class="sxs-lookup"><span data-stu-id="69277-116">Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>

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

### <span data-ttu-id="69277-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="69277-117">-NoWait</span></span>
<span data-ttu-id="69277-118">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="69277-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="69277-119">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="69277-119">-PrivateCloudName</span></span>
<span data-ttu-id="69277-120">사설 클라우드의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="69277-120">The name of the private cloud.</span></span>

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

### <span data-ttu-id="69277-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69277-121">-ResourceGroupName</span></span>
<span data-ttu-id="69277-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="69277-122">The name of the resource group.</span></span>
<span data-ttu-id="69277-123">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="69277-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="69277-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="69277-124">-SubscriptionId</span></span>
<span data-ttu-id="69277-125">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="69277-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="69277-126">-확인</span><span class="sxs-lookup"><span data-stu-id="69277-126">-Confirm</span></span>
<span data-ttu-id="69277-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="69277-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69277-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69277-128">-WhatIf</span></span>
<span data-ttu-id="69277-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="69277-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69277-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="69277-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69277-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69277-131">CommonParameters</span></span>
<span data-ttu-id="69277-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="69277-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69277-133">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="69277-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69277-134">입력</span><span class="sxs-lookup"><span data-stu-id="69277-134">INPUTS</span></span>

## <span data-ttu-id="69277-135">출력</span><span class="sxs-lookup"><span data-stu-id="69277-135">OUTPUTS</span></span>

### <span data-ttu-id="69277-136">Api20200320. IExpressRouteAuthorization에 대 한 Microsoft.</span><span class="sxs-lookup"><span data-stu-id="69277-136">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IExpressRouteAuthorization</span></span>

## <span data-ttu-id="69277-137">상속자</span><span class="sxs-lookup"><span data-stu-id="69277-137">NOTES</span></span>

<span data-ttu-id="69277-138">별칭과</span><span class="sxs-lookup"><span data-stu-id="69277-138">ALIASES</span></span>

## <span data-ttu-id="69277-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="69277-139">RELATED LINKS</span></span>

