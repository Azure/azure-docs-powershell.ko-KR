---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoCluster.md
ms.openlocfilehash: 7cc359b230bc3e4480b1cc6a03db768c17ebf60c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180420"
---
# <span data-ttu-id="85a6f-101">Update-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="85a6f-101">Update-AzKustoCluster</span></span>

## <span data-ttu-id="85a6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85a6f-102">SYNOPSIS</span></span>
<span data-ttu-id="85a6f-103">Kusto 클러스터를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="85a6f-103">Update a Kusto cluster.</span></span>

## <span data-ttu-id="85a6f-104">구문</span><span class="sxs-lookup"><span data-stu-id="85a6f-104">SYNTAX</span></span>

### <span data-ttu-id="85a6f-105">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="85a6f-105">UpdateExpanded (Default)</span></span>
```
Update-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-EnableDiskEncryption] [-EnableDoubleEncryption] [-EnablePurge] [-EnableStreamingIngest]
 [-EngineType <EngineType>] [-IdentityType <IdentityType>] [-IdentityUserAssignedIdentity <Hashtable>]
 [-KeyVaultPropertyKeyName <String>] [-KeyVaultPropertyKeyVaultUri <String>]
 [-KeyVaultPropertyKeyVersion <String>] [-KeyVaultPropertyUserIdentity <String>]
 [-LanguageExtensionValue <ILanguageExtension[]>] [-Location <String>] [-OptimizedAutoscaleIsEnabled]
 [-OptimizedAutoscaleMaximum <Int32>] [-OptimizedAutoscaleMinimum <Int32>]
 [-OptimizedAutoscaleVersion <Int32>] [-SkuCapacity <Int32>] [-SkuName <AzureSkuName>]
 [-SkuTier <AzureSkuTier>] [-Tag <Hashtable>] [-TrustedExternalTenant <ITrustedExternalTenant[]>]
 [-VirtualNetworkConfigurationDataManagementPublicIPId <String>]
 [-VirtualNetworkConfigurationEnginePublicIPId <String>] [-VirtualNetworkConfigurationSubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="85a6f-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="85a6f-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzKustoCluster -InputObject <IKustoIdentity> [-EnableDiskEncryption] [-EnableDoubleEncryption]
 [-EnablePurge] [-EnableStreamingIngest] [-EngineType <EngineType>] [-IdentityType <IdentityType>]
 [-IdentityUserAssignedIdentity <Hashtable>] [-KeyVaultPropertyKeyName <String>]
 [-KeyVaultPropertyKeyVaultUri <String>] [-KeyVaultPropertyKeyVersion <String>]
 [-KeyVaultPropertyUserIdentity <String>] [-LanguageExtensionValue <ILanguageExtension[]>]
 [-Location <String>] [-OptimizedAutoscaleIsEnabled] [-OptimizedAutoscaleMaximum <Int32>]
 [-OptimizedAutoscaleMinimum <Int32>] [-OptimizedAutoscaleVersion <Int32>] [-SkuCapacity <Int32>]
 [-SkuName <AzureSkuName>] [-SkuTier <AzureSkuTier>] [-Tag <Hashtable>]
 [-TrustedExternalTenant <ITrustedExternalTenant[]>]
 [-VirtualNetworkConfigurationDataManagementPublicIPId <String>]
 [-VirtualNetworkConfigurationEnginePublicIPId <String>] [-VirtualNetworkConfigurationSubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="85a6f-107">설명</span><span class="sxs-lookup"><span data-stu-id="85a6f-107">DESCRIPTION</span></span>
<span data-ttu-id="85a6f-108">Kusto 클러스터를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="85a6f-108">Update a Kusto cluster.</span></span>

## <span data-ttu-id="85a6f-109">예제</span><span class="sxs-lookup"><span data-stu-id="85a6f-109">EXAMPLES</span></span>

### <span data-ttu-id="85a6f-110">예제 1: 이름에 의해 기존 클러스터 업데이트</span><span class="sxs-lookup"><span data-stu-id="85a6f-110">Example 1: Update an existing cluster by name</span></span>
```powershell
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -SkuName Standard_D12_v2 -SkuTier Standard -EngineType 'V2'

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="85a6f-111">위의 명령은 리소스 그룹 "testrg"에 있는 Kusto 클러스터 "testnewkustocluster"의 SKU를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="85a6f-111">The above command updates the sku of the Kusto cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="85a6f-112">예제 2: 이름에 의해 기존 클러스터 업데이트</span><span class="sxs-lookup"><span data-stu-id="85a6f-112">Example 2: Update an existing cluster by name</span></span>
```powershell
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -KeyVaultPropertyKeyName "TestKey" -KeyVaultPropertyKeyVaultUri "https://testpskeyvault.vault.azure.net" -KeyVaultPropertyKeyVersion "4bd66f0e0d7c403fac80305e0355d982"

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="85a6f-113">위의 명령은 리소스 그룹 "testrg"에 있는 클러스터 "testnewkustocluster"를 고객 관리 키로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="85a6f-113">The above command updates the cluster "testnewkustocluster" found in the resource group "testrg" with a customer managed key.</span></span>

## <span data-ttu-id="85a6f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85a6f-114">PARAMETERS</span></span>

### <span data-ttu-id="85a6f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="85a6f-115">-AsJob</span></span>
<span data-ttu-id="85a6f-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="85a6f-116">Run the command as a job</span></span>

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

### <span data-ttu-id="85a6f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85a6f-117">-DefaultProfile</span></span>
<span data-ttu-id="85a6f-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="85a6f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85a6f-119">-EnableDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="85a6f-119">-EnableDiskEncryption</span></span>
<span data-ttu-id="85a6f-120">클러스터의 디스크가 암호화되어 있는 경우를 나타내는 부울 값입니다.</span><span class="sxs-lookup"><span data-stu-id="85a6f-120">A boolean value that indicates if the cluster's disks are encrypted.</span></span>

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

### <span data-ttu-id="85a6f-121">-EnableDoubleEncryption</span><span class="sxs-lookup"><span data-stu-id="85a6f-121">-EnableDoubleEncryption</span></span>
<span data-ttu-id="85a6f-122">이중 암호화를 사용할 수 있는 경우를 나타내는 부울 값입니다.</span><span class="sxs-lookup"><span data-stu-id="85a6f-122">A boolean value that indicates if double encryption is enabled.</span></span>

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

### <span data-ttu-id="85a6f-123">-EnablePurge</span><span class="sxs-lookup"><span data-stu-id="85a6f-123">-EnablePurge</span></span>
<span data-ttu-id="85a6f-124">제거 작업이 사용 가능한지 나타내는 부울 값입니다.</span><span class="sxs-lookup"><span data-stu-id="85a6f-124">A boolean value that indicates if the purge operations are enabled.</span></span>

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

### <span data-ttu-id="85a6f-125">-EnableStreamingIngest</span><span class="sxs-lookup"><span data-stu-id="85a6f-125">-EnableStreamingIngest</span></span>
<span data-ttu-id="85a6f-126">스트리밍을 사용할 수 있는지 나타내는 부울 값입니다.</span><span class="sxs-lookup"><span data-stu-id="85a6f-126">A boolean value that indicates if the streaming ingest is enabled.</span></span>

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

### <span data-ttu-id="85a6f-127">-EngineType</span><span class="sxs-lookup"><span data-stu-id="85a6f-127">-EngineType</span></span>
<span data-ttu-id="85a6f-128">엔진 유형</span><span class="sxs-lookup"><span data-stu-id="85a6f-128">The engine type</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.EngineType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85a6f-129">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="85a6f-129">-IdentityType</span></span>
<span data-ttu-id="85a6f-130">사용되는 관리 ID의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="85a6f-130">The type of managed identity used.</span></span>
<span data-ttu-id="85a6f-131">'SystemAssigned, UserAssigned' 형식에는 암시적으로 만든 ID와 사용자 할당 ID 집합이 모두 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="85a6f-131">The type 'SystemAssigned, UserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="85a6f-132">'없음' 형식은 모든 ID를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="85a6f-132">The type 'None' will remove all identities.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.IdentityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85a6f-133">-IdentityUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="85a6f-133">-IdentityUserAssignedIdentity</span></span>
<span data-ttu-id="85a6f-134">Kusto 클러스터와 연결된 사용자 ID 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="85a6f-134">The list of user identities associated with the Kusto cluster.</span></span>
<span data-ttu-id="85a6f-135">사용자 ID 사전 키 참조는 '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}' 형식의 ARM 리소스 ID가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="85a6f-135">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="85a6f-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="85a6f-136">-InputObject</span></span>
<span data-ttu-id="85a6f-137">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="85a6f-137">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="85a6f-138">-KeyVaultPropertyKeyName</span><span class="sxs-lookup"><span data-stu-id="85a6f-138">-KeyVaultPropertyKeyName</span></span>
<span data-ttu-id="85a6f-139">키 자격 증명 모음 키의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="85a6f-139">The name of the key vault key.</span></span>

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

### <span data-ttu-id="85a6f-140">-KeyVaultPropertyKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="85a6f-140">-KeyVaultPropertyKeyVaultUri</span></span>
<span data-ttu-id="85a6f-141">키 자격 증명 모음의 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="85a6f-141">The Uri of the key vault.</span></span>

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

### <span data-ttu-id="85a6f-142">-KeyVaultPropertyKeyVersion</span><span class="sxs-lookup"><span data-stu-id="85a6f-142">-KeyVaultPropertyKeyVersion</span></span>
<span data-ttu-id="85a6f-143">키 자격 증명 모음 키의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="85a6f-143">The version of the key vault key.</span></span>

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

### <span data-ttu-id="85a6f-144">-KeyVaultPropertyUserIdentity</span><span class="sxs-lookup"><span data-stu-id="85a6f-144">-KeyVaultPropertyUserIdentity</span></span>
<span data-ttu-id="85a6f-145">키에 대한 액세스 권한이 ARM 사용자 할당 ID(리소스 ID)입니다.</span><span class="sxs-lookup"><span data-stu-id="85a6f-145">The user assigned identity (ARM resource id) that has access to the key.</span></span>

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

### <span data-ttu-id="85a6f-146">-LanguageExtensionValue</span><span class="sxs-lookup"><span data-stu-id="85a6f-146">-LanguageExtensionValue</span></span>
<span data-ttu-id="85a6f-147">언어 확장 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="85a6f-147">The list of language extensions.</span></span>
<span data-ttu-id="85a6f-148">생성을 위해 LANGUAGEEXTENSIONVALUE 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="85a6f-148">To construct, see NOTES section for LANGUAGEEXTENSIONVALUE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ILanguageExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85a6f-149">-Location</span><span class="sxs-lookup"><span data-stu-id="85a6f-149">-Location</span></span>
<span data-ttu-id="85a6f-150">리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="85a6f-150">Resource location.</span></span>

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

### <span data-ttu-id="85a6f-151">-Name</span><span class="sxs-lookup"><span data-stu-id="85a6f-151">-Name</span></span>
<span data-ttu-id="85a6f-152">Kusto 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="85a6f-152">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85a6f-153">-NoWait</span><span class="sxs-lookup"><span data-stu-id="85a6f-153">-NoWait</span></span>
<span data-ttu-id="85a6f-154">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="85a6f-154">Run the command asynchronously</span></span>

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

### <span data-ttu-id="85a6f-155">-OptimizedAutoscaleIsEnabled</span><span class="sxs-lookup"><span data-stu-id="85a6f-155">-OptimizedAutoscaleIsEnabled</span></span>
<span data-ttu-id="85a6f-156">최적화된 자동 조정 기능이 사용하도록 설정되어 있지 않은지 나타내는 부울 값입니다.</span><span class="sxs-lookup"><span data-stu-id="85a6f-156">A boolean value that indicate if the optimized autoscale feature is enabled or not.</span></span>

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

### <span data-ttu-id="85a6f-157">-OptimizedAutoscaleMaximum</span><span class="sxs-lookup"><span data-stu-id="85a6f-157">-OptimizedAutoscaleMaximum</span></span>
<span data-ttu-id="85a6f-158">허용되는 최대 인스턴스 수입니다.</span><span class="sxs-lookup"><span data-stu-id="85a6f-158">Maximum allowed instances count.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85a6f-159">-OptimizedAutoscaleMinimum</span><span class="sxs-lookup"><span data-stu-id="85a6f-159">-OptimizedAutoscaleMinimum</span></span>
<span data-ttu-id="85a6f-160">허용되는 최소 인스턴스 수입니다.</span><span class="sxs-lookup"><span data-stu-id="85a6f-160">Minimum allowed instances count.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85a6f-161">-OptimizedAutoscaleVersion</span><span class="sxs-lookup"><span data-stu-id="85a6f-161">-OptimizedAutoscaleVersion</span></span>
<span data-ttu-id="85a6f-162">정의된 템플릿의 버전입니다(예: 1).</span><span class="sxs-lookup"><span data-stu-id="85a6f-162">The version of the template defined, for instance 1.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85a6f-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85a6f-163">-ResourceGroupName</span></span>
<span data-ttu-id="85a6f-164">Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="85a6f-164">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85a6f-165">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="85a6f-165">-SkuCapacity</span></span>
<span data-ttu-id="85a6f-166">클러스터의 인스턴스 수입니다.</span><span class="sxs-lookup"><span data-stu-id="85a6f-166">The number of instances of the cluster.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85a6f-167">-SkuName</span><span class="sxs-lookup"><span data-stu-id="85a6f-167">-SkuName</span></span>
<span data-ttu-id="85a6f-168">SKU 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="85a6f-168">SKU name.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.AzureSkuName
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85a6f-169">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="85a6f-169">-SkuTier</span></span>
<span data-ttu-id="85a6f-170">SKU 계층.</span><span class="sxs-lookup"><span data-stu-id="85a6f-170">SKU tier.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.AzureSkuTier
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85a6f-171">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="85a6f-171">-SubscriptionId</span></span>
<span data-ttu-id="85a6f-172">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="85a6f-172">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="85a6f-173">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="85a6f-173">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85a6f-174">-Tag</span><span class="sxs-lookup"><span data-stu-id="85a6f-174">-Tag</span></span>
<span data-ttu-id="85a6f-175">리소스 태그.</span><span class="sxs-lookup"><span data-stu-id="85a6f-175">Resource tags.</span></span>

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

### <span data-ttu-id="85a6f-176">-TrustedExternalTenant</span><span class="sxs-lookup"><span data-stu-id="85a6f-176">-TrustedExternalTenant</span></span>
<span data-ttu-id="85a6f-177">클러스터의 외부 테넌트입니다.</span><span class="sxs-lookup"><span data-stu-id="85a6f-177">The cluster's external tenants.</span></span>
<span data-ttu-id="85a6f-178">생성을 위해 TRUSTEDEXTERNALTENANT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="85a6f-178">To construct, see NOTES section for TRUSTEDEXTERNALTENANT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ITrustedExternalTenant[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85a6f-179">-VirtualNetworkConfigurationDataManagementPublicIPId</span><span class="sxs-lookup"><span data-stu-id="85a6f-179">-VirtualNetworkConfigurationDataManagementPublicIPId</span></span>
<span data-ttu-id="85a6f-180">데이터 관리의 서비스 공용 IP 주소 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="85a6f-180">Data management's service public IP address resource id.</span></span>

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

### <span data-ttu-id="85a6f-181">-VirtualNetworkConfigurationEnginePublicIPId</span><span class="sxs-lookup"><span data-stu-id="85a6f-181">-VirtualNetworkConfigurationEnginePublicIPId</span></span>
<span data-ttu-id="85a6f-182">엔진 서비스의 공용 IP 주소 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="85a6f-182">Engine service's public IP address resource id.</span></span>

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

### <span data-ttu-id="85a6f-183">-VirtualNetworkConfigurationSubnetId</span><span class="sxs-lookup"><span data-stu-id="85a6f-183">-VirtualNetworkConfigurationSubnetId</span></span>
<span data-ttu-id="85a6f-184">서브넷 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="85a6f-184">The subnet resource id.</span></span>

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

### <span data-ttu-id="85a6f-185">-Confirm</span><span class="sxs-lookup"><span data-stu-id="85a6f-185">-Confirm</span></span>
<span data-ttu-id="85a6f-186">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="85a6f-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85a6f-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85a6f-187">-WhatIf</span></span>
<span data-ttu-id="85a6f-188">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="85a6f-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85a6f-189">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="85a6f-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85a6f-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85a6f-190">CommonParameters</span></span>
<span data-ttu-id="85a6f-191">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="85a6f-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85a6f-192">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="85a6f-192">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85a6f-193">입력</span><span class="sxs-lookup"><span data-stu-id="85a6f-193">INPUTS</span></span>

### <span data-ttu-id="85a6f-194">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="85a6f-194">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="85a6f-195">출력</span><span class="sxs-lookup"><span data-stu-id="85a6f-195">OUTPUTS</span></span>

### <span data-ttu-id="85a6f-196">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span><span class="sxs-lookup"><span data-stu-id="85a6f-196">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span></span>

## <span data-ttu-id="85a6f-197">참고 사항</span><span class="sxs-lookup"><span data-stu-id="85a6f-197">NOTES</span></span>

<span data-ttu-id="85a6f-198">별칭</span><span class="sxs-lookup"><span data-stu-id="85a6f-198">ALIASES</span></span>

<span data-ttu-id="85a6f-199">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="85a6f-199">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="85a6f-200">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="85a6f-200">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="85a6f-201">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="85a6f-201">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="85a6f-202">INPUTOBJECT: <IKustoIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="85a6f-202">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="85a6f-203">`[AttachedDatabaseConfigurationName <String>]`: 연결된 데이터베이스 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="85a6f-203">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="85a6f-204">`[ClusterName <String>]`: Kusto 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="85a6f-204">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="85a6f-205">`[DataConnectionName <String>]`: 데이터 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="85a6f-205">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="85a6f-206">`[DatabaseName <String>]`: Kusto 클러스터의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="85a6f-206">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="85a6f-207">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="85a6f-207">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="85a6f-208">`[Location <String>]`: Azure 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="85a6f-208">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="85a6f-209">`[PrincipalAssignmentName <String>]`: Kusto principalAssignment의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="85a6f-209">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="85a6f-210">`[ResourceGroupName <String>]`: Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="85a6f-210">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="85a6f-211">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="85a6f-211">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="85a6f-212">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="85a6f-212">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="85a6f-213">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: 언어 확장 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="85a6f-213">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="85a6f-214">`[Name <LanguageExtensionName?>]`: 언어 확장 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="85a6f-214">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

<span data-ttu-id="85a6f-215">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: 클러스터의 외부 테넌트입니다.</span><span class="sxs-lookup"><span data-stu-id="85a6f-215">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: The cluster's external tenants.</span></span>
  - <span data-ttu-id="85a6f-216">`[Value <String>]`: 외부 테넌트를 나타내는 GUID입니다.</span><span class="sxs-lookup"><span data-stu-id="85a6f-216">`[Value <String>]`: GUID representing an external tenant.</span></span>

## <span data-ttu-id="85a6f-217">관련 링크</span><span class="sxs-lookup"><span data-stu-id="85a6f-217">RELATED LINKS</span></span>

