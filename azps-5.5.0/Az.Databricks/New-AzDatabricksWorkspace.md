---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/new-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksWorkspace.md
ms.openlocfilehash: 0626559fd80a9ebd212c8f6ebb032755d25ba59c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204304"
---
# <span data-ttu-id="70c7d-101">New-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="70c7d-101">New-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="70c7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70c7d-102">SYNOPSIS</span></span>
<span data-ttu-id="70c7d-103">새 작업 영역이 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="70c7d-103">Creates a new workspace.</span></span>

## <span data-ttu-id="70c7d-104">구문</span><span class="sxs-lookup"><span data-stu-id="70c7d-104">SYNTAX</span></span>

```
New-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> -Location <String>
 [-SubscriptionId <String>] [-EnableNoPublicIP] [-ManagedResourceGroupName <String>] [-PrepareEncryption]
 [-PrivateSubnetName <String>] [-PublicSubnetName <String>] [-RequireInfrastructureEncryption] [-Sku <String>]
 [-Tag <Hashtable>] [-VirtualNetworkId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="70c7d-105">설명</span><span class="sxs-lookup"><span data-stu-id="70c7d-105">DESCRIPTION</span></span>
<span data-ttu-id="70c7d-106">새 작업 영역이 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="70c7d-106">Creates a new workspace.</span></span>

## <span data-ttu-id="70c7d-107">예제</span><span class="sxs-lookup"><span data-stu-id="70c7d-107">EXAMPLES</span></span>

### <span data-ttu-id="70c7d-108">예제 1: Databricks 작업 영역 만들기</span><span class="sxs-lookup"><span data-stu-id="70c7d-108">Example 1: Create a Databricks workspace</span></span>
```powershell
PS C:\> New-AzDatabricksWorkspace -Name databricks-test -ResourceGroupName testgroup -Location eastus -ManagedResourceGroupName databricks-group -Sku standard

Location Name            Type
-------- ----            ----
eastus   databricks-test Microsoft.Databricks/workspaces
```

<span data-ttu-id="70c7d-109">이 명령은 Databricks 작업 영역이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="70c7d-109">This command creates a Databricks workspace.</span></span>

### <span data-ttu-id="70c7d-110">예제 2: 사용자 지정된 가상 네트워크를 사용하여 Databricks 작업 영역 만들기</span><span class="sxs-lookup"><span data-stu-id="70c7d-110">Example 2: Create a Databricks workspace with a customized virtual network</span></span>
```powershell
PS C:\> $dlg = New-AzDelegation -Name dbrdl -ServiceName "Microsoft.Databricks/workspaces"
PS C:\> $rdpRule = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
PS C:\> $networkSecurityGroup = New-AzNetworkSecurityGroup -ResourceGroupName testgroup -Location eastus -Name nsg-test -SecurityRules $rdpRule
PS C:\> $privSubnet = New-AzVirtualNetworkSubnetConfig -Name priv-sub -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup -Delegation $dlg
PS C:\> $pubSubnet = New-AzVirtualNetworkSubnetConfig -Name pub-sub  -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup -Delegation $dlg
PS C:\> $testVN = New-AzVirtualNetwork -Name testvn -ResourceGroupName testgroup -Location eastus -AddressPrefix "10.0.0.0/16" -Subnet $privSubnet,$pubSubnet
PS C:\> New-AzDatabricksWorkspace -Name databricks-test-with-custom-vn -ResourceGroupName testgroup -Location eastus -VirtualNetworkId $testVN.Id -PrivateSubnetName $privSubnet.Name -PublicSubnetName $privSubnet.Name -Sku standard

Location Name                           Type
-------- ----                           ----
eastus   databricks-test-with-custom-vn Microsoft.Databricks/workspaces
```

<span data-ttu-id="70c7d-111">이 명령은 리소스 그룹에 사용자 지정된 가상 네트워크를 사용하여 Databricks 작업 영역이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="70c7d-111">This command creates a Databricks workspace with customized virtual network in a resource group.</span></span>

### <span data-ttu-id="70c7d-112">예제 3: 암호화를 사용하도록 설정하여 Databricks 작업 영역 만들기</span><span class="sxs-lookup"><span data-stu-id="70c7d-112">Example 3: Create a Databricks workspace with enable encryption</span></span>
```powershell
PS C:\> New-AzDatabricksWorkspace -Name databricks-test02 -ResourceGroupName testgroup -PrepareEncryption -Location "East US 2 EUAP" -Sku premium

Location Name            Type
-------- ----            ----
eastus   databricks-test02 Microsoft.Databricks/workspaces
```

<span data-ttu-id="70c7d-113">이 명령은 Databricks 작업 영역이 만들어지며 암호화 준비를 위해 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="70c7d-113">This command creates a Databricks workspace and sets it to prepare for encryption.</span></span>
<span data-ttu-id="70c7d-114">암호화에 대한 자세한 설정은 Update-AzDatabricksWorkspace 예제를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="70c7d-114">Please refer to the examples of Update-AzDatabricksWorkspace for more settings to encryption.</span></span>

## <span data-ttu-id="70c7d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="70c7d-115">PARAMETERS</span></span>

### <span data-ttu-id="70c7d-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="70c7d-116">-AsJob</span></span>
<span data-ttu-id="70c7d-117">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="70c7d-117">Run the command as a job</span></span>

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

### <span data-ttu-id="70c7d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70c7d-118">-DefaultProfile</span></span>
<span data-ttu-id="70c7d-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="70c7d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70c7d-120">-EnableNoPublicIP</span><span class="sxs-lookup"><span data-stu-id="70c7d-120">-EnableNoPublicIP</span></span>
<span data-ttu-id="70c7d-121">이 필드에 사용할 값입니다.</span><span class="sxs-lookup"><span data-stu-id="70c7d-121">The value which should be used for this field.</span></span>

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

### <span data-ttu-id="70c7d-122">-Location</span><span class="sxs-lookup"><span data-stu-id="70c7d-122">-Location</span></span>
<span data-ttu-id="70c7d-123">리소스가 있는 지리적 위치</span><span class="sxs-lookup"><span data-stu-id="70c7d-123">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="70c7d-124">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70c7d-124">-ManagedResourceGroupName</span></span>
<span data-ttu-id="70c7d-125">관리되는 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="70c7d-125">The managed resource group name.</span></span>

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

### <span data-ttu-id="70c7d-126">-Name</span><span class="sxs-lookup"><span data-stu-id="70c7d-126">-Name</span></span>
<span data-ttu-id="70c7d-127">작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="70c7d-127">The name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70c7d-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="70c7d-128">-NoWait</span></span>
<span data-ttu-id="70c7d-129">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="70c7d-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="70c7d-130">-PrepareEncryption</span><span class="sxs-lookup"><span data-stu-id="70c7d-130">-PrepareEncryption</span></span>
<span data-ttu-id="70c7d-131">암호화를 위해 작업 영역 준비</span><span class="sxs-lookup"><span data-stu-id="70c7d-131">Prepare the workspace for encryption.</span></span>
<span data-ttu-id="70c7d-132">관리되는 저장소 계정에 대한 관리 ID를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="70c7d-132">Enables the Managed Identity for managed storage account.</span></span>

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

### <span data-ttu-id="70c7d-133">-PrivateSubnetName</span><span class="sxs-lookup"><span data-stu-id="70c7d-133">-PrivateSubnetName</span></span>
<span data-ttu-id="70c7d-134">Virtual Network 내의 개인 서브넷의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="70c7d-134">The name of the Private Subnet within the Virtual Network.</span></span>

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

### <span data-ttu-id="70c7d-135">-PublicSubnetName</span><span class="sxs-lookup"><span data-stu-id="70c7d-135">-PublicSubnetName</span></span>
<span data-ttu-id="70c7d-136">Virtual Network 내의 공용 서브넷의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="70c7d-136">The name of a Public Subnet within the Virtual Network.</span></span>

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

### <span data-ttu-id="70c7d-137">-RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="70c7d-137">-RequireInfrastructureEncryption</span></span>
<span data-ttu-id="70c7d-138">DBFS 루트 파일 시스템을 미사용 데이터에 대한 플랫폼 관리 키를 사용하여 보조 암호화 계층으로 사용할지 여부를 나타내는 부울입니다.</span><span class="sxs-lookup"><span data-stu-id="70c7d-138">A boolean indicating whether or not the DBFS root file system will be enabled with secondary layer of encryption with platform managed keys for data at rest.</span></span>

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

### <span data-ttu-id="70c7d-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70c7d-139">-ResourceGroupName</span></span>
<span data-ttu-id="70c7d-140">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="70c7d-140">The name of the resource group.</span></span>
<span data-ttu-id="70c7d-141">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="70c7d-141">The name is case insensitive.</span></span>

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

### <span data-ttu-id="70c7d-142">-Sku</span><span class="sxs-lookup"><span data-stu-id="70c7d-142">-Sku</span></span>
<span data-ttu-id="70c7d-143">SKU 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="70c7d-143">The SKU name.</span></span>

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

### <span data-ttu-id="70c7d-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="70c7d-144">-SubscriptionId</span></span>
<span data-ttu-id="70c7d-145">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="70c7d-145">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="70c7d-146">-Tag</span><span class="sxs-lookup"><span data-stu-id="70c7d-146">-Tag</span></span>
<span data-ttu-id="70c7d-147">리소스 태그.</span><span class="sxs-lookup"><span data-stu-id="70c7d-147">Resource tags.</span></span>

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

### <span data-ttu-id="70c7d-148">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="70c7d-148">-VirtualNetworkId</span></span>
<span data-ttu-id="70c7d-149">이 Databricks 클러스터를 만들어야 하는 Virtual Network의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="70c7d-149">The ID of a Virtual Network where this Databricks Cluster should be created.</span></span>

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

### <span data-ttu-id="70c7d-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="70c7d-150">-Confirm</span></span>
<span data-ttu-id="70c7d-151">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="70c7d-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70c7d-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70c7d-152">-WhatIf</span></span>
<span data-ttu-id="70c7d-153">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="70c7d-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70c7d-154">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="70c7d-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70c7d-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70c7d-155">CommonParameters</span></span>
<span data-ttu-id="70c7d-156">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="70c7d-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70c7d-157">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="70c7d-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70c7d-158">입력</span><span class="sxs-lookup"><span data-stu-id="70c7d-158">INPUTS</span></span>

## <span data-ttu-id="70c7d-159">출력</span><span class="sxs-lookup"><span data-stu-id="70c7d-159">OUTPUTS</span></span>

### <span data-ttu-id="70c7d-160">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="70c7d-160">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span></span>

## <span data-ttu-id="70c7d-161">참고 사항</span><span class="sxs-lookup"><span data-stu-id="70c7d-161">NOTES</span></span>

<span data-ttu-id="70c7d-162">별칭</span><span class="sxs-lookup"><span data-stu-id="70c7d-162">ALIASES</span></span>

## <span data-ttu-id="70c7d-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="70c7d-163">RELATED LINKS</span></span>

