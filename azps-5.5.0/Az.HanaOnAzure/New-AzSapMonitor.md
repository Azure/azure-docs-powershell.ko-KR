---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/new-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitor.md
ms.openlocfilehash: 95a9e996612827b355b141165231651e17c78f6d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203966"
---
# <span data-ttu-id="18db7-101">New-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="18db7-101">New-AzSapMonitor</span></span>

## <span data-ttu-id="18db7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18db7-102">SYNOPSIS</span></span>
<span data-ttu-id="18db7-103">지정된 구독, 리소스 그룹 및 리소스 이름에 대한 SAP 모니터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="18db7-103">Creates a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="18db7-104">구문</span><span class="sxs-lookup"><span data-stu-id="18db7-104">SYNTAX</span></span>

```
New-AzSapMonitor -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-EnableCustomerAnalytic] [-LogAnalyticsWorkspaceId <String>] [-LogAnalyticsWorkspaceResourceId <String>]
 [-LogAnalyticsWorkspaceSharedKey <String>] [-MonitorSubnetResourceId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="18db7-105">설명</span><span class="sxs-lookup"><span data-stu-id="18db7-105">DESCRIPTION</span></span>
<span data-ttu-id="18db7-106">지정된 구독, 리소스 그룹 및 리소스 이름에 대한 SAP 모니터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="18db7-106">Creates a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="18db7-107">예제</span><span class="sxs-lookup"><span data-stu-id="18db7-107">EXAMPLES</span></span>

### <span data-ttu-id="18db7-108">예제 1: 새 SAP 모니터</span><span class="sxs-lookup"><span data-stu-id="18db7-108">Example 1: New SAP monitor</span></span> 
```powershell
PS C:\> $Workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName nancyc-hn1 -Name sapmonitor-test  -Location westus2 -Sku "Standard"
PS C:\> $WorkspaceKey = Get-AzOperationalInsightsWorkspaceSharedKey -ResourceGroupName nancyc-hn1 -Name sapmonitor-test
PS C:\> New-AzSapMonitor -Name ps-sapmonitor-t01 -ResourceGroupName nancyc-hn1 -Location westus2 -EnableCustomerAnalytic -MonitorSubnet "/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/nancyc-hn1/providers/Microsoft.Network/virtualNetworks/vnet-sap/subnets/subnet-admin" -LogAnalyticsWorkspaceSharedKey $WorkspaceKey.PrimarySharedKey -LogAnalyticsWorkspaceId $Workspace.CustomerId -LogAnalyticsWorkspaceResourceId $Workspace.ResourceId

Location Name              Type
-------- ----              ----
westus2  ps-sapmonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="18db7-109">이 명령은 SAP 모니터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="18db7-109">This command creates a SAP monitor.</span></span>

## <span data-ttu-id="18db7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="18db7-110">PARAMETERS</span></span>

### <span data-ttu-id="18db7-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="18db7-111">-AsJob</span></span>
<span data-ttu-id="18db7-112">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="18db7-112">Run the command as a job</span></span>

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

### <span data-ttu-id="18db7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18db7-113">-DefaultProfile</span></span>
<span data-ttu-id="18db7-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="18db7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18db7-115">-EnableCustomerAnalytic</span><span class="sxs-lookup"><span data-stu-id="18db7-115">-EnableCustomerAnalytic</span></span>
<span data-ttu-id="18db7-116">Microsoft에 분석을 보낼지 여부를 나타내는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="18db7-116">The value indicating whether to send analytics to Microsoft</span></span>

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

### <span data-ttu-id="18db7-117">-Location</span><span class="sxs-lookup"><span data-stu-id="18db7-117">-Location</span></span>
<span data-ttu-id="18db7-118">리소스가 있는 지리적 위치</span><span class="sxs-lookup"><span data-stu-id="18db7-118">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="18db7-119">-LogAnalyticsWorkspaceId</span><span class="sxs-lookup"><span data-stu-id="18db7-119">-LogAnalyticsWorkspaceId</span></span>
<span data-ttu-id="18db7-120">모니터링에 사용할 로그 분석 작업 영역의 작업 영역 ID</span><span class="sxs-lookup"><span data-stu-id="18db7-120">The workspace ID of the log analytics workspace to be used for monitoring</span></span>

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

### <span data-ttu-id="18db7-121">-LogAnalyticsWorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="18db7-121">-LogAnalyticsWorkspaceResourceId</span></span>
<span data-ttu-id="18db7-122">모니터링에 ARM Log Analytics 작업 영역의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="18db7-122">The ARM ID of the Log Analytics Workspace that is used for monitoring</span></span>

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

### <span data-ttu-id="18db7-123">-LogAnalyticsWorkspaceSharedKey</span><span class="sxs-lookup"><span data-stu-id="18db7-123">-LogAnalyticsWorkspaceSharedKey</span></span>
<span data-ttu-id="18db7-124">모니터링에 사용되는 로그 분석 작업 영역의 공유 키</span><span class="sxs-lookup"><span data-stu-id="18db7-124">The shared key of the log analytics workspace that is used for monitoring</span></span>

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

### <span data-ttu-id="18db7-125">-MonitorSubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="18db7-125">-MonitorSubnetResourceId</span></span>
<span data-ttu-id="18db7-126">SAP 모니터를 배포할 서브넷입니다.</span><span class="sxs-lookup"><span data-stu-id="18db7-126">The subnet which the SAP monitor will be deployed in.</span></span>
<span data-ttu-id="18db7-127">HANA 데이터베이스의 동일한 서브넷에 해당해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="18db7-127">It should be the same subnet of HANA database.</span></span>

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

### <span data-ttu-id="18db7-128">-Name</span><span class="sxs-lookup"><span data-stu-id="18db7-128">-Name</span></span>
<span data-ttu-id="18db7-129">SAP 모니터 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="18db7-129">Name of the SAP monitor resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SapMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18db7-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="18db7-130">-NoWait</span></span>
<span data-ttu-id="18db7-131">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="18db7-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="18db7-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18db7-132">-ResourceGroupName</span></span>
<span data-ttu-id="18db7-133">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="18db7-133">Name of the resource group.</span></span>

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

### <span data-ttu-id="18db7-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="18db7-134">-SubscriptionId</span></span>
<span data-ttu-id="18db7-135">Microsoft Azure 구독을 고유하게 식별하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="18db7-135">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="18db7-136">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="18db7-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="18db7-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="18db7-137">-Tag</span></span>
<span data-ttu-id="18db7-138">리소스 태그.</span><span class="sxs-lookup"><span data-stu-id="18db7-138">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18db7-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="18db7-139">-Confirm</span></span>
<span data-ttu-id="18db7-140">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="18db7-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18db7-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18db7-141">-WhatIf</span></span>
<span data-ttu-id="18db7-142">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="18db7-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18db7-143">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="18db7-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18db7-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18db7-144">CommonParameters</span></span>
<span data-ttu-id="18db7-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="18db7-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18db7-146">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="18db7-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18db7-147">입력</span><span class="sxs-lookup"><span data-stu-id="18db7-147">INPUTS</span></span>

## <span data-ttu-id="18db7-148">출력</span><span class="sxs-lookup"><span data-stu-id="18db7-148">OUTPUTS</span></span>

### <span data-ttu-id="18db7-149">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span><span class="sxs-lookup"><span data-stu-id="18db7-149">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span></span>

## <span data-ttu-id="18db7-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="18db7-150">NOTES</span></span>

<span data-ttu-id="18db7-151">별칭</span><span class="sxs-lookup"><span data-stu-id="18db7-151">ALIASES</span></span>

## <span data-ttu-id="18db7-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="18db7-152">RELATED LINKS</span></span>

