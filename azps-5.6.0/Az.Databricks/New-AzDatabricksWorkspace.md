---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/powershell/module/az.databricks/new-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksWorkspace.md
ms.openlocfilehash: c49056da040e7259c1cbc0964335f157e00cbecd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962240"
---
# <span data-ttu-id="c7aa4-101">New-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="c7aa4-101">New-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="c7aa4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7aa4-102">SYNOPSIS</span></span>
<span data-ttu-id="c7aa4-103">새 작업 영역 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c7aa4-103">Creates a new workspace.</span></span>

## <span data-ttu-id="c7aa4-104">구문</span><span class="sxs-lookup"><span data-stu-id="c7aa4-104">SYNTAX</span></span>

```
New-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> -Location <String>
 [-SubscriptionId <String>] [-EnableNoPublicIP] [-ManagedResourceGroupName <String>] [-PrepareEncryption]
 [-PrivateSubnetName <String>] [-PublicSubnetName <String>] [-RequireInfrastructureEncryption] [-Sku <String>]
 [-Tag <Hashtable>] [-VirtualNetworkId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c7aa4-105">설명</span><span class="sxs-lookup"><span data-stu-id="c7aa4-105">DESCRIPTION</span></span>
<span data-ttu-id="c7aa4-106">새 작업 영역 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c7aa4-106">Creates a new workspace.</span></span>

## <span data-ttu-id="c7aa4-107">예제</span><span class="sxs-lookup"><span data-stu-id="c7aa4-107">EXAMPLES</span></span>

### <span data-ttu-id="c7aa4-108">예제 1: Databricks 작업 영역 만들기</span><span class="sxs-lookup"><span data-stu-id="c7aa4-108">Example 1: Create a Databricks workspace</span></span>
```powershell
PS C:\> New-AzDatabricksWorkspace -Name databricks-test -ResourceGroupName testgroup -Location eastus -ManagedResourceGroupName databricks-group -Sku standard

Location Name            Type
-------- ----            ----
eastus   databricks-test Microsoft.Databricks/workspaces
```

<span data-ttu-id="c7aa4-109">이 명령은 Databricks 작업 영역이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="c7aa4-109">This command creates a Databricks workspace.</span></span>

### <span data-ttu-id="c7aa4-110">예제 2: 사용자 지정된 가상 네트워크를 사용하여 Databricks 작업 영역 만들기</span><span class="sxs-lookup"><span data-stu-id="c7aa4-110">Example 2: Create a Databricks workspace with a customized virtual network</span></span>
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

<span data-ttu-id="c7aa4-111">이 명령은 리소스 그룹에 사용자 지정된 가상 네트워크를 사용하여 Databricks 작업 영역이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="c7aa4-111">This command creates a Databricks workspace with customized virtual network in a resource group.</span></span>

### <span data-ttu-id="c7aa4-112">예제 3: 암호화를 사용하도록 설정하여 Databricks 작업 영역 만들기</span><span class="sxs-lookup"><span data-stu-id="c7aa4-112">Example 3: Create a Databricks workspace with enable encryption</span></span>
```powershell
PS C:\> New-AzDatabricksWorkspace -Name databricks-test02 -ResourceGroupName testgroup -PrepareEncryption -Location "East US 2 EUAP" -Sku premium

Location Name            Type
-------- ----            ----
eastus   databricks-test02 Microsoft.Databricks/workspaces
```

<span data-ttu-id="c7aa4-113">이 명령은 Databricks 작업 영역 을 만들고 암호화를 준비하기 위해 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="c7aa4-113">This command creates a Databricks workspace and sets it to prepare for encryption.</span></span>
<span data-ttu-id="c7aa4-114">암호화에 대한 자세한 Update-AzDatabricksWorkspace 예제를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c7aa4-114">Please refer to the examples of Update-AzDatabricksWorkspace for more settings to encryption.</span></span>

## <span data-ttu-id="c7aa4-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c7aa4-115">PARAMETERS</span></span>

### <span data-ttu-id="c7aa4-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c7aa4-116">-AsJob</span></span>
<span data-ttu-id="c7aa4-117">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="c7aa4-117">Run the command as a job</span></span>

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

### <span data-ttu-id="c7aa4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7aa4-118">-DefaultProfile</span></span>
<span data-ttu-id="c7aa4-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c7aa4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7aa4-120">-EnableNoPublicIP</span><span class="sxs-lookup"><span data-stu-id="c7aa4-120">-EnableNoPublicIP</span></span>
<span data-ttu-id="c7aa4-121">이 필드에 사용할 값입니다.</span><span class="sxs-lookup"><span data-stu-id="c7aa4-121">The value which should be used for this field.</span></span>

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

### <span data-ttu-id="c7aa4-122">-Location</span><span class="sxs-lookup"><span data-stu-id="c7aa4-122">-Location</span></span>
<span data-ttu-id="c7aa4-123">리소스가 있는 지리적 위치</span><span class="sxs-lookup"><span data-stu-id="c7aa4-123">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="c7aa4-124">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7aa4-124">-ManagedResourceGroupName</span></span>
<span data-ttu-id="c7aa4-125">관리되는 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c7aa4-125">The managed resource group name.</span></span>

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

### <span data-ttu-id="c7aa4-126">-Name</span><span class="sxs-lookup"><span data-stu-id="c7aa4-126">-Name</span></span>
<span data-ttu-id="c7aa4-127">작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c7aa4-127">The name of the workspace.</span></span>

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

### <span data-ttu-id="c7aa4-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c7aa4-128">-NoWait</span></span>
<span data-ttu-id="c7aa4-129">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="c7aa4-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c7aa4-130">-PrepareEncryption</span><span class="sxs-lookup"><span data-stu-id="c7aa4-130">-PrepareEncryption</span></span>
<span data-ttu-id="c7aa4-131">암호화를 위해 작업 영역 준비.</span><span class="sxs-lookup"><span data-stu-id="c7aa4-131">Prepare the workspace for encryption.</span></span>
<span data-ttu-id="c7aa4-132">관리되는 저장소 계정에 대해 관리 ID를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c7aa4-132">Enables the Managed Identity for managed storage account.</span></span>

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

### <span data-ttu-id="c7aa4-133">-PrivateSubnetName</span><span class="sxs-lookup"><span data-stu-id="c7aa4-133">-PrivateSubnetName</span></span>
<span data-ttu-id="c7aa4-134">가상 네트워크 내의 개인 서브넷의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c7aa4-134">The name of the Private Subnet within the Virtual Network.</span></span>

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

### <span data-ttu-id="c7aa4-135">-PublicSubnetName</span><span class="sxs-lookup"><span data-stu-id="c7aa4-135">-PublicSubnetName</span></span>
<span data-ttu-id="c7aa4-136">Virtual Network 내의 공용 서브넷의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c7aa4-136">The name of a Public Subnet within the Virtual Network.</span></span>

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

### <span data-ttu-id="c7aa4-137">-RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="c7aa4-137">-RequireInfrastructureEncryption</span></span>
<span data-ttu-id="c7aa4-138">DBFS 루트 파일 시스템이 미사용 데이터에 대한 플랫폼 관리 키를 사용하여 보조 암호화 계층을 사용하여 사용하도록 설정될지 여부를 나타내는 부울입니다.</span><span class="sxs-lookup"><span data-stu-id="c7aa4-138">A boolean indicating whether or not the DBFS root file system will be enabled with secondary layer of encryption with platform managed keys for data at rest.</span></span>

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

### <span data-ttu-id="c7aa4-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7aa4-139">-ResourceGroupName</span></span>
<span data-ttu-id="c7aa4-140">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c7aa4-140">The name of the resource group.</span></span>
<span data-ttu-id="c7aa4-141">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="c7aa4-141">The name is case insensitive.</span></span>

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

### <span data-ttu-id="c7aa4-142">-Sku</span><span class="sxs-lookup"><span data-stu-id="c7aa4-142">-Sku</span></span>
<span data-ttu-id="c7aa4-143">SKU 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c7aa4-143">The SKU name.</span></span>

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

### <span data-ttu-id="c7aa4-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c7aa4-144">-SubscriptionId</span></span>
<span data-ttu-id="c7aa4-145">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c7aa4-145">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="c7aa4-146">-Tag</span><span class="sxs-lookup"><span data-stu-id="c7aa4-146">-Tag</span></span>
<span data-ttu-id="c7aa4-147">리소스 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="c7aa4-147">Resource tags.</span></span>

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

### <span data-ttu-id="c7aa4-148">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="c7aa4-148">-VirtualNetworkId</span></span>
<span data-ttu-id="c7aa4-149">이 Databricks 클러스터를 만들어야 하는 가상 네트워크의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c7aa4-149">The ID of a Virtual Network where this Databricks Cluster should be created.</span></span>

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

### <span data-ttu-id="c7aa4-150">-확인</span><span class="sxs-lookup"><span data-stu-id="c7aa4-150">-Confirm</span></span>
<span data-ttu-id="c7aa4-151">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c7aa4-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7aa4-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7aa4-152">-WhatIf</span></span>
<span data-ttu-id="c7aa4-153">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="c7aa4-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7aa4-154">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c7aa4-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7aa4-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7aa4-155">CommonParameters</span></span>
<span data-ttu-id="c7aa4-156">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c7aa4-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7aa4-157">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c7aa4-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7aa4-158">입력</span><span class="sxs-lookup"><span data-stu-id="c7aa4-158">INPUTS</span></span>

## <span data-ttu-id="c7aa4-159">출력</span><span class="sxs-lookup"><span data-stu-id="c7aa4-159">OUTPUTS</span></span>

### <span data-ttu-id="c7aa4-160">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="c7aa4-160">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span></span>

## <span data-ttu-id="c7aa4-161">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c7aa4-161">NOTES</span></span>

<span data-ttu-id="c7aa4-162">별칭</span><span class="sxs-lookup"><span data-stu-id="c7aa4-162">ALIASES</span></span>

## <span data-ttu-id="c7aa4-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c7aa4-163">RELATED LINKS</span></span>

