---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoCluster.md
ms.openlocfilehash: b868633f0217b2048f0a83641f678e9c092d21c7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493450"
---
# <span data-ttu-id="24cdb-101">New-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="24cdb-101">New-AzKustoCluster</span></span>

## <span data-ttu-id="24cdb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24cdb-102">SYNOPSIS</span></span>
<span data-ttu-id="24cdb-103">Kusto 클러스터를 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="24cdb-103">Create or update a Kusto cluster.</span></span>

## <span data-ttu-id="24cdb-104">구문</span><span class="sxs-lookup"><span data-stu-id="24cdb-104">SYNTAX</span></span>

```
New-AzKustoCluster -Name <String> -ResourceGroupName <String> -Location <String> -SkuName <AzureSkuName>
 -SkuTier <AzureSkuTier> [-SubscriptionId <String>] [-EnableDiskEncryption] [-EnableDoubleEncryption]
 [-EnablePurge] [-EnableStreamingIngest] [-EngineType <EngineType>] [-IdentityType <IdentityType>]
 [-IdentityUserAssignedIdentity <Hashtable>] [-KeyVaultPropertyKeyName <String>]
 [-KeyVaultPropertyKeyVaultUri <String>] [-KeyVaultPropertyKeyVersion <String>]
 [-KeyVaultPropertyUserIdentity <String>] [-LanguageExtensionValue <ILanguageExtension[]>]
 [-OptimizedAutoscaleIsEnabled] [-OptimizedAutoscaleMaximum <Int32>] [-OptimizedAutoscaleMinimum <Int32>]
 [-OptimizedAutoscaleVersion <Int32>] [-SkuCapacity <Int32>] [-Tag <Hashtable>]
 [-TrustedExternalTenant <ITrustedExternalTenant[]>]
 [-VirtualNetworkConfigurationDataManagementPublicIPId <String>]
 [-VirtualNetworkConfigurationEnginePublicIPId <String>] [-VirtualNetworkConfigurationSubnetId <String>]
 [-Zone <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="24cdb-105">설명</span><span class="sxs-lookup"><span data-stu-id="24cdb-105">DESCRIPTION</span></span>
<span data-ttu-id="24cdb-106">Kusto 클러스터를 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="24cdb-106">Create or update a Kusto cluster.</span></span>

## <span data-ttu-id="24cdb-107">예제</span><span class="sxs-lookup"><span data-stu-id="24cdb-107">EXAMPLES</span></span>

### <span data-ttu-id="24cdb-108">예제 1: 새 Kusto 클러스터 만들기</span><span class="sxs-lookup"><span data-stu-id="24cdb-108">Example 1: Create a new Kusto cluster</span></span>
```powershell
PS C:\> New-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -Location 'East US' -SkuName Standard_D11_v2 -SkuTier Standard -EnableDoubleEncryption true -EngineType 'V2'

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="24cdb-109">위의 명령은 리소스 그룹 "testrg"에 "testnewkustocluster"라는 새 Kusto 클러스터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="24cdb-109">The above command creates a new Kusto cluster named "testnewkustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="24cdb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="24cdb-110">PARAMETERS</span></span>

### <span data-ttu-id="24cdb-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="24cdb-111">-AsJob</span></span>
<span data-ttu-id="24cdb-112">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="24cdb-112">Run the command as a job</span></span>

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

### <span data-ttu-id="24cdb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24cdb-113">-DefaultProfile</span></span>
<span data-ttu-id="24cdb-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="24cdb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24cdb-115">-EnableDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="24cdb-115">-EnableDiskEncryption</span></span>
<span data-ttu-id="24cdb-116">클러스터의 디스크가 암호화되어 있는 경우를 나타내는 부울 값입니다.</span><span class="sxs-lookup"><span data-stu-id="24cdb-116">A boolean value that indicates if the cluster's disks are encrypted.</span></span>

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

### <span data-ttu-id="24cdb-117">-EnableDoubleEncryption</span><span class="sxs-lookup"><span data-stu-id="24cdb-117">-EnableDoubleEncryption</span></span>
<span data-ttu-id="24cdb-118">이중 암호화를 사용할 수 있는지 나타내는 부울 값입니다.</span><span class="sxs-lookup"><span data-stu-id="24cdb-118">A boolean value that indicates if double encryption is enabled.</span></span>

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

### <span data-ttu-id="24cdb-119">-EnablePurge</span><span class="sxs-lookup"><span data-stu-id="24cdb-119">-EnablePurge</span></span>
<span data-ttu-id="24cdb-120">제거 작업을 사용할 수 있는지 나타내는 부울 값입니다.</span><span class="sxs-lookup"><span data-stu-id="24cdb-120">A boolean value that indicates if the purge operations are enabled.</span></span>

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

### <span data-ttu-id="24cdb-121">-EnableStreamingIngest</span><span class="sxs-lookup"><span data-stu-id="24cdb-121">-EnableStreamingIngest</span></span>
<span data-ttu-id="24cdb-122">스트리밍을 사용할 수 있는지 나타내는 부울 값입니다.</span><span class="sxs-lookup"><span data-stu-id="24cdb-122">A boolean value that indicates if the streaming ingest is enabled.</span></span>

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

### <span data-ttu-id="24cdb-123">-EngineType</span><span class="sxs-lookup"><span data-stu-id="24cdb-123">-EngineType</span></span>
<span data-ttu-id="24cdb-124">엔진 유형</span><span class="sxs-lookup"><span data-stu-id="24cdb-124">The engine type</span></span>

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

### <span data-ttu-id="24cdb-125">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="24cdb-125">-IdentityType</span></span>
<span data-ttu-id="24cdb-126">사용되는 관리 ID의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="24cdb-126">The type of managed identity used.</span></span>
<span data-ttu-id="24cdb-127">'SystemAssigned, UserAssigned' 형식에는 암시적으로 만든 ID와 사용자 할당 ID 집합이 모두 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="24cdb-127">The type 'SystemAssigned, UserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="24cdb-128">'없음' 형식은 모든 ID를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="24cdb-128">The type 'None' will remove all identities.</span></span>

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

### <span data-ttu-id="24cdb-129">-IdentityUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="24cdb-129">-IdentityUserAssignedIdentity</span></span>
<span data-ttu-id="24cdb-130">Kusto 클러스터와 연결된 사용자 ID 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="24cdb-130">The list of user identities associated with the Kusto cluster.</span></span>
<span data-ttu-id="24cdb-131">사용자 ID 사전 키 참조는 '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}' 형식의 ARM 리소스 ID가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="24cdb-131">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="24cdb-132">-KeyVaultPropertyKeyName</span><span class="sxs-lookup"><span data-stu-id="24cdb-132">-KeyVaultPropertyKeyName</span></span>
<span data-ttu-id="24cdb-133">키 자격 증명 모음 키의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24cdb-133">The name of the key vault key.</span></span>

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

### <span data-ttu-id="24cdb-134">-KeyVaultPropertyKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="24cdb-134">-KeyVaultPropertyKeyVaultUri</span></span>
<span data-ttu-id="24cdb-135">키 자격 증명 모음의 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="24cdb-135">The Uri of the key vault.</span></span>

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

### <span data-ttu-id="24cdb-136">-KeyVaultPropertyKeyVersion</span><span class="sxs-lookup"><span data-stu-id="24cdb-136">-KeyVaultPropertyKeyVersion</span></span>
<span data-ttu-id="24cdb-137">키 자격 증명 모음 키의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="24cdb-137">The version of the key vault key.</span></span>

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

### <span data-ttu-id="24cdb-138">-KeyVaultPropertyUserIdentity</span><span class="sxs-lookup"><span data-stu-id="24cdb-138">-KeyVaultPropertyUserIdentity</span></span>
<span data-ttu-id="24cdb-139">키에 대한 액세스 권한이 ARM 사용자 할당 ID(리소스 ID)입니다.</span><span class="sxs-lookup"><span data-stu-id="24cdb-139">The user assigned identity (ARM resource id) that has access to the key.</span></span>

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

### <span data-ttu-id="24cdb-140">-LanguageExtensionValue</span><span class="sxs-lookup"><span data-stu-id="24cdb-140">-LanguageExtensionValue</span></span>
<span data-ttu-id="24cdb-141">언어 확장 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="24cdb-141">The list of language extensions.</span></span>
<span data-ttu-id="24cdb-142">생성을 위해 LANGUAGEEXTENSIONVALUE 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="24cdb-142">To construct, see NOTES section for LANGUAGEEXTENSIONVALUE properties and create a hash table.</span></span>

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

### <span data-ttu-id="24cdb-143">-Location</span><span class="sxs-lookup"><span data-stu-id="24cdb-143">-Location</span></span>
<span data-ttu-id="24cdb-144">리소스가 있는 지리적 위치</span><span class="sxs-lookup"><span data-stu-id="24cdb-144">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="24cdb-145">-Name</span><span class="sxs-lookup"><span data-stu-id="24cdb-145">-Name</span></span>
<span data-ttu-id="24cdb-146">Kusto 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24cdb-146">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24cdb-147">-NoWait</span><span class="sxs-lookup"><span data-stu-id="24cdb-147">-NoWait</span></span>
<span data-ttu-id="24cdb-148">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="24cdb-148">Run the command asynchronously</span></span>

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

### <span data-ttu-id="24cdb-149">-OptimizedAutoscaleIsEnabled</span><span class="sxs-lookup"><span data-stu-id="24cdb-149">-OptimizedAutoscaleIsEnabled</span></span>
<span data-ttu-id="24cdb-150">최적화된 자동 조정 기능이 사용하도록 설정되어 있지 않은지 나타내는 부울 값입니다.</span><span class="sxs-lookup"><span data-stu-id="24cdb-150">A boolean value that indicate if the optimized autoscale feature is enabled or not.</span></span>

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

### <span data-ttu-id="24cdb-151">-OptimizedAutoscaleMaximum</span><span class="sxs-lookup"><span data-stu-id="24cdb-151">-OptimizedAutoscaleMaximum</span></span>
<span data-ttu-id="24cdb-152">허용되는 최대 인스턴스 수입니다.</span><span class="sxs-lookup"><span data-stu-id="24cdb-152">Maximum allowed instances count.</span></span>

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

### <span data-ttu-id="24cdb-153">-OptimizedAutoscaleMinimum</span><span class="sxs-lookup"><span data-stu-id="24cdb-153">-OptimizedAutoscaleMinimum</span></span>
<span data-ttu-id="24cdb-154">허용되는 최소 인스턴스 수입니다.</span><span class="sxs-lookup"><span data-stu-id="24cdb-154">Minimum allowed instances count.</span></span>

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

### <span data-ttu-id="24cdb-155">-OptimizedAutoscaleVersion</span><span class="sxs-lookup"><span data-stu-id="24cdb-155">-OptimizedAutoscaleVersion</span></span>
<span data-ttu-id="24cdb-156">정의된 템플릿의 버전입니다(예: 1).</span><span class="sxs-lookup"><span data-stu-id="24cdb-156">The version of the template defined, for instance 1.</span></span>

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

### <span data-ttu-id="24cdb-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24cdb-157">-ResourceGroupName</span></span>
<span data-ttu-id="24cdb-158">Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24cdb-158">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="24cdb-159">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="24cdb-159">-SkuCapacity</span></span>
<span data-ttu-id="24cdb-160">클러스터의 인스턴스 수입니다.</span><span class="sxs-lookup"><span data-stu-id="24cdb-160">The number of instances of the cluster.</span></span>

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

### <span data-ttu-id="24cdb-161">-SkuName</span><span class="sxs-lookup"><span data-stu-id="24cdb-161">-SkuName</span></span>
<span data-ttu-id="24cdb-162">SKU 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24cdb-162">SKU name.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.AzureSkuName
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24cdb-163">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="24cdb-163">-SkuTier</span></span>
<span data-ttu-id="24cdb-164">SKU 계층.</span><span class="sxs-lookup"><span data-stu-id="24cdb-164">SKU tier.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.AzureSkuTier
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24cdb-165">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="24cdb-165">-SubscriptionId</span></span>
<span data-ttu-id="24cdb-166">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="24cdb-166">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="24cdb-167">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="24cdb-167">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="24cdb-168">-Tag</span><span class="sxs-lookup"><span data-stu-id="24cdb-168">-Tag</span></span>
<span data-ttu-id="24cdb-169">리소스 태그.</span><span class="sxs-lookup"><span data-stu-id="24cdb-169">Resource tags.</span></span>

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

### <span data-ttu-id="24cdb-170">-TrustedExternalTenant</span><span class="sxs-lookup"><span data-stu-id="24cdb-170">-TrustedExternalTenant</span></span>
<span data-ttu-id="24cdb-171">클러스터의 외부 테넌트입니다.</span><span class="sxs-lookup"><span data-stu-id="24cdb-171">The cluster's external tenants.</span></span>
<span data-ttu-id="24cdb-172">생성을 위해 TRUSTEDEXTERNALTENANT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="24cdb-172">To construct, see NOTES section for TRUSTEDEXTERNALTENANT properties and create a hash table.</span></span>

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

### <span data-ttu-id="24cdb-173">-VirtualNetworkConfigurationDataManagementPublicIPId</span><span class="sxs-lookup"><span data-stu-id="24cdb-173">-VirtualNetworkConfigurationDataManagementPublicIPId</span></span>
<span data-ttu-id="24cdb-174">데이터 관리의 서비스 공용 IP 주소 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="24cdb-174">Data management's service public IP address resource id.</span></span>

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

### <span data-ttu-id="24cdb-175">-VirtualNetworkConfigurationEnginePublicIPId</span><span class="sxs-lookup"><span data-stu-id="24cdb-175">-VirtualNetworkConfigurationEnginePublicIPId</span></span>
<span data-ttu-id="24cdb-176">엔진 서비스의 공용 IP 주소 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="24cdb-176">Engine service's public IP address resource id.</span></span>

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

### <span data-ttu-id="24cdb-177">-VirtualNetworkConfigurationSubnetId</span><span class="sxs-lookup"><span data-stu-id="24cdb-177">-VirtualNetworkConfigurationSubnetId</span></span>
<span data-ttu-id="24cdb-178">서브넷 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="24cdb-178">The subnet resource id.</span></span>

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

### <span data-ttu-id="24cdb-179">-Zone</span><span class="sxs-lookup"><span data-stu-id="24cdb-179">-Zone</span></span>
<span data-ttu-id="24cdb-180">클러스터의 가용성 영역입니다.</span><span class="sxs-lookup"><span data-stu-id="24cdb-180">The availability zones of the cluster.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24cdb-181">-Confirm</span><span class="sxs-lookup"><span data-stu-id="24cdb-181">-Confirm</span></span>
<span data-ttu-id="24cdb-182">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="24cdb-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24cdb-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24cdb-183">-WhatIf</span></span>
<span data-ttu-id="24cdb-184">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="24cdb-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24cdb-185">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="24cdb-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24cdb-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24cdb-186">CommonParameters</span></span>
<span data-ttu-id="24cdb-187">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="24cdb-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24cdb-188">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="24cdb-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24cdb-189">입력</span><span class="sxs-lookup"><span data-stu-id="24cdb-189">INPUTS</span></span>

## <span data-ttu-id="24cdb-190">출력</span><span class="sxs-lookup"><span data-stu-id="24cdb-190">OUTPUTS</span></span>

### <span data-ttu-id="24cdb-191">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span><span class="sxs-lookup"><span data-stu-id="24cdb-191">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span></span>

## <span data-ttu-id="24cdb-192">참고 사항</span><span class="sxs-lookup"><span data-stu-id="24cdb-192">NOTES</span></span>

<span data-ttu-id="24cdb-193">별칭</span><span class="sxs-lookup"><span data-stu-id="24cdb-193">ALIASES</span></span>

<span data-ttu-id="24cdb-194">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="24cdb-194">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="24cdb-195">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="24cdb-195">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="24cdb-196">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="24cdb-196">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="24cdb-197">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: 언어 확장 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="24cdb-197">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="24cdb-198">`[Name <LanguageExtensionName?>]`: 언어 확장 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24cdb-198">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

<span data-ttu-id="24cdb-199">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: 클러스터의 외부 테넌트입니다.</span><span class="sxs-lookup"><span data-stu-id="24cdb-199">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: The cluster's external tenants.</span></span>
  - <span data-ttu-id="24cdb-200">`[Value <String>]`: 외부 테넌트에 대한 GUID입니다.</span><span class="sxs-lookup"><span data-stu-id="24cdb-200">`[Value <String>]`: GUID representing an external tenant.</span></span>

## <span data-ttu-id="24cdb-201">관련 링크</span><span class="sxs-lookup"><span data-stu-id="24cdb-201">RELATED LINKS</span></span>

