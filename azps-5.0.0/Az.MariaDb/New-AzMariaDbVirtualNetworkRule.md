---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/new-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: 77a89dec96e0e9b7ca7bd003f8368274edf6acdf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218644"
---
# <span data-ttu-id="9adcc-101">New-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="9adcc-101">New-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="9adcc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9adcc-102">SYNOPSIS</span></span>
<span data-ttu-id="9adcc-103">기존 가상 네트워크 규칙을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9adcc-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="9adcc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9adcc-104">SYNTAX</span></span>

```
New-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint] [-SubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9adcc-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9adcc-105">DESCRIPTION</span></span>
<span data-ttu-id="9adcc-106">기존 가상 네트워크 규칙을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9adcc-106">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="9adcc-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9adcc-107">EXAMPLES</span></span>

### <span data-ttu-id="9adcc-108">예제 1:2에 대 한 가상 네트워크 규칙 만들기 (Adb)</span><span class="sxs-lookup"><span data-stu-id="9adcc-108">Example 1: Create a virtual network rule for a MariaDB</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name vnet -ResourceGroupName mariadb-test-qu5ov0
PS C:\> New-AzMariaDbVirtualNetworkRule -ServerName mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 -Name vnet-001 -SubnetId $vnet.Subnets[0].Id -IgnoreMissingVnetServiceEndpoint

Name     Type
----     ----
vnet-001 Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="9adcc-109">이 명령은 a 2에 대 한 가상 네트워크 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9adcc-109">This command creates a virtual network rule for a MariaDB.</span></span>

## <span data-ttu-id="9adcc-110">변수</span><span class="sxs-lookup"><span data-stu-id="9adcc-110">PARAMETERS</span></span>

### <span data-ttu-id="9adcc-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9adcc-111">-AsJob</span></span>
<span data-ttu-id="9adcc-112">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="9adcc-112">Run the command as a job</span></span>

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

### <span data-ttu-id="9adcc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9adcc-113">-DefaultProfile</span></span>
<span data-ttu-id="9adcc-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9adcc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9adcc-115">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="9adcc-115">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="9adcc-116">가상 네트워크에 vnet 서비스 끝점을 사용 하도록 설정 하기 전에 방화벽 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9adcc-116">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="9adcc-117">-이름</span><span class="sxs-lookup"><span data-stu-id="9adcc-117">-Name</span></span>
<span data-ttu-id="9adcc-118">가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9adcc-118">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9adcc-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9adcc-119">-NoWait</span></span>
<span data-ttu-id="9adcc-120">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="9adcc-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9adcc-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9adcc-121">-PassThru</span></span>
<span data-ttu-id="9adcc-122">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9adcc-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="9adcc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9adcc-123">-ResourceGroupName</span></span>
<span data-ttu-id="9adcc-124">리소스가 포함 된 자원 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9adcc-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="9adcc-125">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9adcc-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="9adcc-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9adcc-126">-ServerName</span></span>
<span data-ttu-id="9adcc-127">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9adcc-127">The name of the server.</span></span>

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

### <span data-ttu-id="9adcc-128">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="9adcc-128">-SubnetId</span></span>
<span data-ttu-id="9adcc-129">가상 네트워크 서브넷의 ARM 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="9adcc-129">The ARM resource id of the virtual network subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9adcc-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9adcc-130">-SubscriptionId</span></span>
<span data-ttu-id="9adcc-131">Azure 구독을 식별 하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="9adcc-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="9adcc-132">-확인</span><span class="sxs-lookup"><span data-stu-id="9adcc-132">-Confirm</span></span>
<span data-ttu-id="9adcc-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9adcc-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9adcc-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9adcc-134">-WhatIf</span></span>
<span data-ttu-id="9adcc-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9adcc-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9adcc-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9adcc-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9adcc-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9adcc-137">CommonParameters</span></span>
<span data-ttu-id="9adcc-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9adcc-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9adcc-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9adcc-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9adcc-140">입력</span><span class="sxs-lookup"><span data-stu-id="9adcc-140">INPUTS</span></span>

## <span data-ttu-id="9adcc-141">출력</span><span class="sxs-lookup"><span data-stu-id="9adcc-141">OUTPUTS</span></span>

### <span data-ttu-id="9adcc-142">Microsoft. Api20180601Preview. IVirtualNetworkRule에 대 한. b a r i.</span><span class="sxs-lookup"><span data-stu-id="9adcc-142">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span></span>

## <span data-ttu-id="9adcc-143">상속자</span><span class="sxs-lookup"><span data-stu-id="9adcc-143">NOTES</span></span>

<span data-ttu-id="9adcc-144">별칭과</span><span class="sxs-lookup"><span data-stu-id="9adcc-144">ALIASES</span></span>

## <span data-ttu-id="9adcc-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9adcc-145">RELATED LINKS</span></span>

