---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoCluster.md
ms.openlocfilehash: a3e1561feb470708420015bac1e2f0688f182896
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214491"
---
# <span data-ttu-id="ea232-101">Update-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="ea232-101">Update-AzKustoCluster</span></span>

## <span data-ttu-id="ea232-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea232-102">SYNOPSIS</span></span>
<span data-ttu-id="ea232-103">Kusto 클러스터를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea232-103">Update a Kusto cluster.</span></span>

## <span data-ttu-id="ea232-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ea232-104">SYNTAX</span></span>

### <span data-ttu-id="ea232-105">UpdateExpanded 됨 (기본값)</span><span class="sxs-lookup"><span data-stu-id="ea232-105">UpdateExpanded (Default)</span></span>
```
Update-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-EnableDiskEncryption] [-EnableDoubleEncryption] [-EnablePurge] [-EnableStreamingIngest]
 [-IdentityType <IdentityType>] [-IdentityUserAssignedIdentity <Hashtable>]
 [-KeyVaultPropertyKeyName <String>] [-KeyVaultPropertyKeyVaultUri <String>]
 [-KeyVaultPropertyKeyVersion <String>] [-LanguageExtensionValue <ILanguageExtension[]>] [-Location <String>]
 [-OptimizedAutoscaleIsEnabled] [-OptimizedAutoscaleMaximum <Int32>] [-OptimizedAutoscaleMinimum <Int32>]
 [-OptimizedAutoscaleVersion <Int32>] [-SkuCapacity <Int32>] [-SkuName <AzureSkuName>]
 [-SkuTier <AzureSkuTier>] [-Tag <Hashtable>] [-TrustedExternalTenant <ITrustedExternalTenant[]>]
 [-VirtualNetworkConfigurationDataManagementPublicIPId <String>]
 [-VirtualNetworkConfigurationEnginePublicIPId <String>] [-VirtualNetworkConfigurationSubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ea232-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="ea232-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzKustoCluster -InputObject <IKustoIdentity> [-EnableDiskEncryption] [-EnableDoubleEncryption]
 [-EnablePurge] [-EnableStreamingIngest] [-IdentityType <IdentityType>]
 [-IdentityUserAssignedIdentity <Hashtable>] [-KeyVaultPropertyKeyName <String>]
 [-KeyVaultPropertyKeyVaultUri <String>] [-KeyVaultPropertyKeyVersion <String>]
 [-LanguageExtensionValue <ILanguageExtension[]>] [-Location <String>] [-OptimizedAutoscaleIsEnabled]
 [-OptimizedAutoscaleMaximum <Int32>] [-OptimizedAutoscaleMinimum <Int32>]
 [-OptimizedAutoscaleVersion <Int32>] [-SkuCapacity <Int32>] [-SkuName <AzureSkuName>]
 [-SkuTier <AzureSkuTier>] [-Tag <Hashtable>] [-TrustedExternalTenant <ITrustedExternalTenant[]>]
 [-VirtualNetworkConfigurationDataManagementPublicIPId <String>]
 [-VirtualNetworkConfigurationEnginePublicIPId <String>] [-VirtualNetworkConfigurationSubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ea232-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ea232-107">DESCRIPTION</span></span>
<span data-ttu-id="ea232-108">Kusto 클러스터를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea232-108">Update a Kusto cluster.</span></span>

## <span data-ttu-id="ea232-109">예제의</span><span class="sxs-lookup"><span data-stu-id="ea232-109">EXAMPLES</span></span>

### <span data-ttu-id="ea232-110">예제 1: 이름으로 기존 클러스터 업데이트</span><span class="sxs-lookup"><span data-stu-id="ea232-110">Example 1: Update an existing cluster by name</span></span>
```powershell
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -SkuName Standard_D12_v2 -SkuTier Standard

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="ea232-111">위 명령은 Kusto의 sku를 리소스 그룹 "testrg"에 있는 "testnewkustocluster" 클러스터로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea232-111">The above command updates the sku of the Kusto cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="ea232-112">예제 2: 이름으로 기존 클러스터 업데이트</span><span class="sxs-lookup"><span data-stu-id="ea232-112">Example 2: Update an existing cluster by name</span></span>
```powershell
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -KeyVaultPropertyKeyName "TestKey" -KeyVaultPropertyKeyVaultUri "https://testpskeyvault.vault.azure.net" -KeyVaultPropertyKeyVersion "4bd66f0e0d7c403fac80305e0355d982"

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="ea232-113">위의 명령은 리소스 그룹 "testrg"에서 찾은 클러스터 "testnewkustocluster"를 고객 관리 키를 사용 하 여 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea232-113">The above command updates the cluster "testnewkustocluster" found in the resource group "testrg" with a customer managed key.</span></span>

## <span data-ttu-id="ea232-114">변수</span><span class="sxs-lookup"><span data-stu-id="ea232-114">PARAMETERS</span></span>

### <span data-ttu-id="ea232-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ea232-115">-AsJob</span></span>
<span data-ttu-id="ea232-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="ea232-116">Run the command as a job</span></span>

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

### <span data-ttu-id="ea232-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea232-117">-DefaultProfile</span></span>
<span data-ttu-id="ea232-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ea232-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea232-119">-EnableDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="ea232-119">-EnableDiskEncryption</span></span>
<span data-ttu-id="ea232-120">클러스터의 디스크가 암호화 되었는지 여부를 나타내는 부울 값입니다.</span><span class="sxs-lookup"><span data-stu-id="ea232-120">A boolean value that indicates if the cluster's disks are encrypted.</span></span>

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

### <span data-ttu-id="ea232-121">-EnableDoubleEncryption</span><span class="sxs-lookup"><span data-stu-id="ea232-121">-EnableDoubleEncryption</span></span>
<span data-ttu-id="ea232-122">이중 암호화를 사용 하는지 여부를 나타내는 부울 값입니다.</span><span class="sxs-lookup"><span data-stu-id="ea232-122">A boolean value that indicates if double encryption is enabled.</span></span>

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

### <span data-ttu-id="ea232-123">-EnablePurge</span><span class="sxs-lookup"><span data-stu-id="ea232-123">-EnablePurge</span></span>
<span data-ttu-id="ea232-124">지우기 작업을 사용할 수 있는지 여부를 나타내는 부울 값입니다.</span><span class="sxs-lookup"><span data-stu-id="ea232-124">A boolean value that indicates if the purge operations are enabled.</span></span>

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

### <span data-ttu-id="ea232-125">-EnableStreamingIngest</span><span class="sxs-lookup"><span data-stu-id="ea232-125">-EnableStreamingIngest</span></span>
<span data-ttu-id="ea232-126">스트리밍 수집을 사용할 수 있는지 여부를 나타내는 부울 값입니다.</span><span class="sxs-lookup"><span data-stu-id="ea232-126">A boolean value that indicates if the streaming ingest is enabled.</span></span>

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

### <span data-ttu-id="ea232-127">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="ea232-127">-IdentityType</span></span>
<span data-ttu-id="ea232-128">Id 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="ea232-128">The identity type.</span></span>

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

### <span data-ttu-id="ea232-129">-IdentityUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="ea232-129">-IdentityUserAssignedIdentity</span></span>
<span data-ttu-id="ea232-130">Kusto cluster와 연결 된 사용자 id 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="ea232-130">The list of user identities associated with the Kusto cluster.</span></span>
<span data-ttu-id="ea232-131">사용자 id 사전 키 참조는 '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName} ' 형식으로 팔로 리소스 id를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea232-131">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="ea232-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea232-132">-InputObject</span></span>
<span data-ttu-id="ea232-133">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ea232-133">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ea232-134">-KeyVaultPropertyKeyName</span><span class="sxs-lookup"><span data-stu-id="ea232-134">-KeyVaultPropertyKeyName</span></span>
<span data-ttu-id="ea232-135">키 보관소 키의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ea232-135">The name of the key vault key.</span></span>

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

### <span data-ttu-id="ea232-136">-KeyVaultPropertyKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="ea232-136">-KeyVaultPropertyKeyVaultUri</span></span>
<span data-ttu-id="ea232-137">키 보관소의 Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="ea232-137">The Uri of the key vault.</span></span>

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

### <span data-ttu-id="ea232-138">-KeyVaultPropertyKeyVersion</span><span class="sxs-lookup"><span data-stu-id="ea232-138">-KeyVaultPropertyKeyVersion</span></span>
<span data-ttu-id="ea232-139">키 보관소 키의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="ea232-139">The version of the key vault key.</span></span>

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

### <span data-ttu-id="ea232-140">-LanguageExtensionValue</span><span class="sxs-lookup"><span data-stu-id="ea232-140">-LanguageExtensionValue</span></span>
<span data-ttu-id="ea232-141">언어 확장 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="ea232-141">The list of language extensions.</span></span>
<span data-ttu-id="ea232-142">생성 하려면 LANGUAGEEXTENSIONVALUE 속성에 대 한 메모 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ea232-142">To construct, see NOTES section for LANGUAGEEXTENSIONVALUE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ILanguageExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea232-143">-위치</span><span class="sxs-lookup"><span data-stu-id="ea232-143">-Location</span></span>
<span data-ttu-id="ea232-144">리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="ea232-144">Resource location.</span></span>

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

### <span data-ttu-id="ea232-145">-이름</span><span class="sxs-lookup"><span data-stu-id="ea232-145">-Name</span></span>
<span data-ttu-id="ea232-146">Kusto의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ea232-146">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="ea232-147">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ea232-147">-NoWait</span></span>
<span data-ttu-id="ea232-148">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="ea232-148">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ea232-149">-OptimizedAutoscaleIsEnabled</span><span class="sxs-lookup"><span data-stu-id="ea232-149">-OptimizedAutoscaleIsEnabled</span></span>
<span data-ttu-id="ea232-150">최적화 된 자동 크기 조정 기능을 사용할 수 있는지 여부를 나타내는 부울 값입니다.</span><span class="sxs-lookup"><span data-stu-id="ea232-150">A boolean value that indicate if the optimized autoscale feature is enabled or not.</span></span>

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

### <span data-ttu-id="ea232-151">-OptimizedAutoscaleMaximum</span><span class="sxs-lookup"><span data-stu-id="ea232-151">-OptimizedAutoscaleMaximum</span></span>
<span data-ttu-id="ea232-152">허용 되는 최대 인스턴스 수입니다.</span><span class="sxs-lookup"><span data-stu-id="ea232-152">Maximum allowed instances count.</span></span>

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

### <span data-ttu-id="ea232-153">-OptimizedAutoscaleMinimum</span><span class="sxs-lookup"><span data-stu-id="ea232-153">-OptimizedAutoscaleMinimum</span></span>
<span data-ttu-id="ea232-154">허용 되는 최소 인스턴스 수입니다.</span><span class="sxs-lookup"><span data-stu-id="ea232-154">Minimum allowed instances count.</span></span>

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

### <span data-ttu-id="ea232-155">-OptimizedAutoscaleVersion</span><span class="sxs-lookup"><span data-stu-id="ea232-155">-OptimizedAutoscaleVersion</span></span>
<span data-ttu-id="ea232-156">인스턴스 1에 대해 정의 된 서식 파일의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="ea232-156">The version of the template defined, for instance 1.</span></span>

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

### <span data-ttu-id="ea232-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea232-157">-ResourceGroupName</span></span>
<span data-ttu-id="ea232-158">Kusto cluster를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ea232-158">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="ea232-159">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="ea232-159">-SkuCapacity</span></span>
<span data-ttu-id="ea232-160">클러스터 인스턴스의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="ea232-160">The number of instances of the cluster.</span></span>

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

### <span data-ttu-id="ea232-161">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="ea232-161">-SkuName</span></span>
<span data-ttu-id="ea232-162">SKU 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ea232-162">SKU name.</span></span>

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

### <span data-ttu-id="ea232-163">-서 고 U계층</span><span class="sxs-lookup"><span data-stu-id="ea232-163">-SkuTier</span></span>
<span data-ttu-id="ea232-164">SKU 계층.</span><span class="sxs-lookup"><span data-stu-id="ea232-164">SKU tier.</span></span>

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

### <span data-ttu-id="ea232-165">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ea232-165">-SubscriptionId</span></span>
<span data-ttu-id="ea232-166">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ea232-166">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ea232-167">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea232-167">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ea232-168">태그</span><span class="sxs-lookup"><span data-stu-id="ea232-168">-Tag</span></span>
<span data-ttu-id="ea232-169">리소스 태그.</span><span class="sxs-lookup"><span data-stu-id="ea232-169">Resource tags.</span></span>

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

### <span data-ttu-id="ea232-170">-TrustedExternalTenant</span><span class="sxs-lookup"><span data-stu-id="ea232-170">-TrustedExternalTenant</span></span>
<span data-ttu-id="ea232-171">클러스터의 외부 테 넌 트입니다.</span><span class="sxs-lookup"><span data-stu-id="ea232-171">The cluster's external tenants.</span></span>
<span data-ttu-id="ea232-172">생성 하려면 TRUSTEDEXTERNALTENANT 속성에 대 한 메모 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ea232-172">To construct, see NOTES section for TRUSTEDEXTERNALTENANT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ITrustedExternalTenant[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea232-173">-VirtualNetworkConfigurationDataManagementPublicIPId</span><span class="sxs-lookup"><span data-stu-id="ea232-173">-VirtualNetworkConfigurationDataManagementPublicIPId</span></span>
<span data-ttu-id="ea232-174">데이터 관리 서비스 공용 IP 주소 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="ea232-174">Data management's service public IP address resource id.</span></span>

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

### <span data-ttu-id="ea232-175">-VirtualNetworkConfigurationEnginePublicIPId</span><span class="sxs-lookup"><span data-stu-id="ea232-175">-VirtualNetworkConfigurationEnginePublicIPId</span></span>
<span data-ttu-id="ea232-176">엔진 서비스의 공용 IP 주소 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="ea232-176">Engine service's public IP address resource id.</span></span>

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

### <span data-ttu-id="ea232-177">-VirtualNetworkConfigurationSubnetId</span><span class="sxs-lookup"><span data-stu-id="ea232-177">-VirtualNetworkConfigurationSubnetId</span></span>
<span data-ttu-id="ea232-178">서브넷 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="ea232-178">The subnet resource id.</span></span>

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

### <span data-ttu-id="ea232-179">-확인</span><span class="sxs-lookup"><span data-stu-id="ea232-179">-Confirm</span></span>
<span data-ttu-id="ea232-180">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea232-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea232-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea232-181">-WhatIf</span></span>
<span data-ttu-id="ea232-182">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ea232-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea232-183">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ea232-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea232-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea232-184">CommonParameters</span></span>
<span data-ttu-id="ea232-185">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea232-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea232-186">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ea232-186">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea232-187">입력</span><span class="sxs-lookup"><span data-stu-id="ea232-187">INPUTS</span></span>

### <span data-ttu-id="ea232-188">IKustoIdentity (Microsoft. PowerShell. m a us</span><span class="sxs-lookup"><span data-stu-id="ea232-188">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="ea232-189">출력</span><span class="sxs-lookup"><span data-stu-id="ea232-189">OUTPUTS</span></span>

### <span data-ttu-id="ea232-190">Microsoft. Api20200614. ICluster에 대 한.</span><span class="sxs-lookup"><span data-stu-id="ea232-190">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICluster</span></span>

## <span data-ttu-id="ea232-191">상속자</span><span class="sxs-lookup"><span data-stu-id="ea232-191">NOTES</span></span>

<span data-ttu-id="ea232-192">별칭과</span><span class="sxs-lookup"><span data-stu-id="ea232-192">ALIASES</span></span>

<span data-ttu-id="ea232-193">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="ea232-193">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ea232-194">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea232-194">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ea232-195">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="ea232-195">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ea232-196">INPUTOBJECT <IKustoIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="ea232-196">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ea232-197">`[AttachedDatabaseConfigurationName <String>]`: 연결 된 데이터베이스 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ea232-197">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="ea232-198">`[ClusterName <String>]`: Kusto의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ea232-198">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="ea232-199">`[DataConnectionName <String>]`: 데이터 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ea232-199">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="ea232-200">`[DatabaseName <String>]`: Kusto cluster의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ea232-200">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="ea232-201">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="ea232-201">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ea232-202">`[Location <String>]`: Azure 위치.</span><span class="sxs-lookup"><span data-stu-id="ea232-202">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="ea232-203">`[PrincipalAssignmentName <String>]`:%에 대 한 Kusto principalAssignment의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ea232-203">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="ea232-204">`[ResourceGroupName <String>]`: Kusto cluster를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ea232-204">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="ea232-205">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ea232-205">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="ea232-206">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea232-206">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="ea232-207">LANGUAGEEXTENSIONVALUE <ILanguageExtension [] >: 언어 확장 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="ea232-207">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="ea232-208">`[Name <LanguageExtensionName?>]`: 언어 확장 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ea232-208">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

<span data-ttu-id="ea232-209">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant [] >: 클러스터의 외부 테 넌 트.</span><span class="sxs-lookup"><span data-stu-id="ea232-209">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: The cluster's external tenants.</span></span>
  - <span data-ttu-id="ea232-210">`[Value <String>]`: 외부 테 넌 트를 나타내는 GUID입니다.</span><span class="sxs-lookup"><span data-stu-id="ea232-210">`[Value <String>]`: GUID representing an external tenant.</span></span>

## <span data-ttu-id="ea232-211">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ea232-211">RELATED LINKS</span></span>

