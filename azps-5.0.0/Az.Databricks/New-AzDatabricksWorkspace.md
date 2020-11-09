---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/new-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksWorkspace.md
ms.openlocfilehash: 09f1cd27e9af0c6442afa00d5301975cae8fbdeb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94305072"
---
# <span data-ttu-id="fdacc-101">New-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="fdacc-101">New-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="fdacc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fdacc-102">SYNOPSIS</span></span>
<span data-ttu-id="fdacc-103">새 작업 영역을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fdacc-103">Creates a new workspace.</span></span>

## <span data-ttu-id="fdacc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fdacc-104">SYNTAX</span></span>

```
New-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> -Location <String>
 [-SubscriptionId <String>] [-ManagedResourceGroupName <String>] [-PrepareEncryption]
 [-PrivateSubnetName <String>] [-PublicSubnetName <String>] [-RequireInfrastructureEncryption] [-Sku <String>]
 [-Tag <Hashtable>] [-VirtualNetworkId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fdacc-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fdacc-105">DESCRIPTION</span></span>
<span data-ttu-id="fdacc-106">새 작업 영역을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fdacc-106">Creates a new workspace.</span></span>

## <span data-ttu-id="fdacc-107">예제의</span><span class="sxs-lookup"><span data-stu-id="fdacc-107">EXAMPLES</span></span>

### <span data-ttu-id="fdacc-108">예제 1: Databricks 작업 영역 만들기</span><span class="sxs-lookup"><span data-stu-id="fdacc-108">Example 1: Create a Databricks workspace</span></span>
```powershell
PS C:\> New-AzDatabricksWorkspace -Name databricks-test -ResourceGroupName testgroup -Location eastus -ManagedResourceGroupName databricks-group -Sku standard

Location Name            Type
-------- ----            ----
eastus   databricks-test Microsoft.Databricks/workspaces
```

<span data-ttu-id="fdacc-109">이 명령은 Databricks 작업 영역을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fdacc-109">This command creates a Databricks workspace.</span></span>

### <span data-ttu-id="fdacc-110">예제 2: 사용자 지정 된 가상 네트워크를 사용 하 여 Databricks 작업 영역 만들기</span><span class="sxs-lookup"><span data-stu-id="fdacc-110">Example 2: Create a Databricks workspace with a customized virtual network</span></span>
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

<span data-ttu-id="fdacc-111">이 명령은 리소스 그룹에서 사용자 지정 된 가상 네트워크를 사용 하 여 Databricks 작업 영역을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fdacc-111">This command creates a Databricks workspace with customized virtual network in a resource group.</span></span>

### <span data-ttu-id="fdacc-112">예제 3: 암호화를 사용 하 여 Databricks 작업 영역 만들기</span><span class="sxs-lookup"><span data-stu-id="fdacc-112">Example 3: Create a Databricks workspace with enable encryption</span></span>
```powershell
PS C:\> New-AzDatabricksWorkspace -Name databricks-test02 -ResourceGroupName testgroup -PrepareEncryption -Location "East US 2 EUAP" -Sku premium

Location Name            Type
-------- ----            ----
eastus   databricks-test02 Microsoft.Databricks/workspaces
```

<span data-ttu-id="fdacc-113">이 명령은 Databricks 작업 영역을 만들고 암호화를 준비 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdacc-113">This command creates a Databricks workspace and sets it to prepare for encryption.</span></span>
<span data-ttu-id="fdacc-114">암호화에 대 한 자세한 설정은 Update-AzDatabricksWorkspace의 예제를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fdacc-114">Please refer to the examples of Update-AzDatabricksWorkspace for more settings to encryption.</span></span>

## <span data-ttu-id="fdacc-115">변수</span><span class="sxs-lookup"><span data-stu-id="fdacc-115">PARAMETERS</span></span>

### <span data-ttu-id="fdacc-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fdacc-116">-AsJob</span></span>
<span data-ttu-id="fdacc-117">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="fdacc-117">Run the command as a job</span></span>

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

### <span data-ttu-id="fdacc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdacc-118">-DefaultProfile</span></span>
<span data-ttu-id="fdacc-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fdacc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdacc-120">-위치</span><span class="sxs-lookup"><span data-stu-id="fdacc-120">-Location</span></span>
<span data-ttu-id="fdacc-121">리소스가 상주 하는 지리적 위치</span><span class="sxs-lookup"><span data-stu-id="fdacc-121">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="fdacc-122">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdacc-122">-ManagedResourceGroupName</span></span>
<span data-ttu-id="fdacc-123">관리 되는 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fdacc-123">The managed resource group name.</span></span>

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

### <span data-ttu-id="fdacc-124">-이름</span><span class="sxs-lookup"><span data-stu-id="fdacc-124">-Name</span></span>
<span data-ttu-id="fdacc-125">작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fdacc-125">The name of the workspace.</span></span>

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

### <span data-ttu-id="fdacc-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="fdacc-126">-NoWait</span></span>
<span data-ttu-id="fdacc-127">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="fdacc-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="fdacc-128">-PrepareEncryption</span><span class="sxs-lookup"><span data-stu-id="fdacc-128">-PrepareEncryption</span></span>
<span data-ttu-id="fdacc-129">암호화를 위해 작업 영역을 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdacc-129">Prepare the workspace for encryption.</span></span>
<span data-ttu-id="fdacc-130">관리 되는 저장소 계정에 관리 되는 Id를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdacc-130">Enables the Managed Identity for managed storage account.</span></span>

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

### <span data-ttu-id="fdacc-131">-PrivateSubnetName</span><span class="sxs-lookup"><span data-stu-id="fdacc-131">-PrivateSubnetName</span></span>
<span data-ttu-id="fdacc-132">가상 네트워크 내의 개인 서브넷 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fdacc-132">The name of the Private Subnet within the Virtual Network.</span></span>

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

### <span data-ttu-id="fdacc-133">-PublicSubnetName</span><span class="sxs-lookup"><span data-stu-id="fdacc-133">-PublicSubnetName</span></span>
<span data-ttu-id="fdacc-134">가상 네트워크 내의 공용 서브넷 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fdacc-134">The name of a Public Subnet within the Virtual Network.</span></span>

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

### <span data-ttu-id="fdacc-135">-RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="fdacc-135">-RequireInfrastructureEncryption</span></span>
<span data-ttu-id="fdacc-136">데이터에 대 한 플랫폼 관리 키를 사용 하 여 DBFS 루트 파일 시스템을 사용할 수 있는지 여부를 나타내는 부울 값입니다.</span><span class="sxs-lookup"><span data-stu-id="fdacc-136">A boolean indicating whether or not the DBFS root file system will be enabled with secondary layer of encryption with platform managed keys for data at rest.</span></span>

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

### <span data-ttu-id="fdacc-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdacc-137">-ResourceGroupName</span></span>
<span data-ttu-id="fdacc-138">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fdacc-138">The name of the resource group.</span></span>
<span data-ttu-id="fdacc-139">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdacc-139">The name is case insensitive.</span></span>

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

### <span data-ttu-id="fdacc-140">-Sku</span><span class="sxs-lookup"><span data-stu-id="fdacc-140">-Sku</span></span>
<span data-ttu-id="fdacc-141">SKU 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fdacc-141">The SKU name.</span></span>

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

### <span data-ttu-id="fdacc-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fdacc-142">-SubscriptionId</span></span>
<span data-ttu-id="fdacc-143">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="fdacc-143">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="fdacc-144">태그</span><span class="sxs-lookup"><span data-stu-id="fdacc-144">-Tag</span></span>
<span data-ttu-id="fdacc-145">리소스 태그.</span><span class="sxs-lookup"><span data-stu-id="fdacc-145">Resource tags.</span></span>

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

### <span data-ttu-id="fdacc-146">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="fdacc-146">-VirtualNetworkId</span></span>
<span data-ttu-id="fdacc-147">이 Databricks 클러스터를 만들어야 하는 가상 네트워크의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="fdacc-147">The ID of a Virtual Network where this Databricks Cluster should be created.</span></span>

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

### <span data-ttu-id="fdacc-148">-확인</span><span class="sxs-lookup"><span data-stu-id="fdacc-148">-Confirm</span></span>
<span data-ttu-id="fdacc-149">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdacc-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fdacc-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdacc-150">-WhatIf</span></span>
<span data-ttu-id="fdacc-151">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fdacc-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fdacc-152">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fdacc-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fdacc-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdacc-153">CommonParameters</span></span>
<span data-ttu-id="fdacc-154">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdacc-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdacc-155">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fdacc-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdacc-156">입력</span><span class="sxs-lookup"><span data-stu-id="fdacc-156">INPUTS</span></span>

## <span data-ttu-id="fdacc-157">출력</span><span class="sxs-lookup"><span data-stu-id="fdacc-157">OUTPUTS</span></span>

### <span data-ttu-id="fdacc-158">Databricks. Api20180401에 대 한 작업 영역</span><span class="sxs-lookup"><span data-stu-id="fdacc-158">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span></span>

## <span data-ttu-id="fdacc-159">상속자</span><span class="sxs-lookup"><span data-stu-id="fdacc-159">NOTES</span></span>

<span data-ttu-id="fdacc-160">별칭과</span><span class="sxs-lookup"><span data-stu-id="fdacc-160">ALIASES</span></span>

## <span data-ttu-id="fdacc-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fdacc-161">RELATED LINKS</span></span>

