---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/new-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoCluster.md
ms.openlocfilehash: c8378e9be3c92cc799eb92b9ff913be98116b019
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959595"
---
# <span data-ttu-id="8bdb9-101">New-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="8bdb9-101">New-AzKustoCluster</span></span>

## <span data-ttu-id="8bdb9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8bdb9-102">SYNOPSIS</span></span>
<span data-ttu-id="8bdb9-103">Kusto 클러스터를 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-103">Create or update a Kusto cluster.</span></span>

## <span data-ttu-id="8bdb9-104">구문</span><span class="sxs-lookup"><span data-stu-id="8bdb9-104">SYNTAX</span></span>

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

## <span data-ttu-id="8bdb9-105">설명</span><span class="sxs-lookup"><span data-stu-id="8bdb9-105">DESCRIPTION</span></span>
<span data-ttu-id="8bdb9-106">Kusto 클러스터를 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-106">Create or update a Kusto cluster.</span></span>

## <span data-ttu-id="8bdb9-107">예제</span><span class="sxs-lookup"><span data-stu-id="8bdb9-107">EXAMPLES</span></span>

### <span data-ttu-id="8bdb9-108">예제 1: 새 Kusto 클러스터 만들기</span><span class="sxs-lookup"><span data-stu-id="8bdb9-108">Example 1: Create a new Kusto cluster</span></span>
```powershell
PS C:\> New-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -Location 'East US' -SkuName Standard_D11_v2 -SkuTier Standard -EnableDoubleEncryption true -EngineType 'V2'

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="8bdb9-109">위의 명령은 리소스 그룹 "testrg"에서 "testnewkustocluster"라는 새 Kusto 클러스터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-109">The above command creates a new Kusto cluster named "testnewkustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="8bdb9-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="8bdb9-110">PARAMETERS</span></span>

### <span data-ttu-id="8bdb9-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8bdb9-111">-AsJob</span></span>
<span data-ttu-id="8bdb9-112">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-112">Run the command as a job</span></span>

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

### <span data-ttu-id="8bdb9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bdb9-113">-DefaultProfile</span></span>
<span data-ttu-id="8bdb9-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8bdb9-115">-EnableDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="8bdb9-115">-EnableDiskEncryption</span></span>
<span data-ttu-id="8bdb9-116">클러스터의 디스크가 암호화되어 있는 경우를 나타내는 부울 값입니다.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-116">A boolean value that indicates if the cluster's disks are encrypted.</span></span>

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

### <span data-ttu-id="8bdb9-117">-enableDoubleEncryption</span><span class="sxs-lookup"><span data-stu-id="8bdb9-117">-EnableDoubleEncryption</span></span>
<span data-ttu-id="8bdb9-118">두 번 암호화를 사용하도록 설정되어 있는 경우를 나타내는 부울 값입니다.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-118">A boolean value that indicates if double encryption is enabled.</span></span>

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

### <span data-ttu-id="8bdb9-119">-EnablePurge</span><span class="sxs-lookup"><span data-stu-id="8bdb9-119">-EnablePurge</span></span>
<span data-ttu-id="8bdb9-120">제거 작업이 활성화되어 있는 경우를 나타내는 부울 값입니다.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-120">A boolean value that indicates if the purge operations are enabled.</span></span>

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

### <span data-ttu-id="8bdb9-121">-EnableStreamingIngest</span><span class="sxs-lookup"><span data-stu-id="8bdb9-121">-EnableStreamingIngest</span></span>
<span data-ttu-id="8bdb9-122">스트리밍 인제스트를 사용하도록 설정되어 있는 경우를 나타내는 부울 값입니다.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-122">A boolean value that indicates if the streaming ingest is enabled.</span></span>

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

### <span data-ttu-id="8bdb9-123">-EngineType</span><span class="sxs-lookup"><span data-stu-id="8bdb9-123">-EngineType</span></span>
<span data-ttu-id="8bdb9-124">엔진 유형</span><span class="sxs-lookup"><span data-stu-id="8bdb9-124">The engine type</span></span>

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

### <span data-ttu-id="8bdb9-125">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="8bdb9-125">-IdentityType</span></span>
<span data-ttu-id="8bdb9-126">사용된 관리 ID의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-126">The type of managed identity used.</span></span>
<span data-ttu-id="8bdb9-127">'SystemAssigned, UserAssigned' 형식에는 암시적으로 만든 ID와 사용자 할당 ID 집합이 모두 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-127">The type 'SystemAssigned, UserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="8bdb9-128">'None' 형식은 모든 ID를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-128">The type 'None' will remove all identities.</span></span>

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

### <span data-ttu-id="8bdb9-129">-IdentityUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="8bdb9-129">-IdentityUserAssignedIdentity</span></span>
<span data-ttu-id="8bdb9-130">Kusto 클러스터와 연결된 사용자 ID 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-130">The list of user identities associated with the Kusto cluster.</span></span>
<span data-ttu-id="8bdb9-131">사용자 ARM ID 사전 키 참조는 '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}' 형식의 리소스 ID로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-131">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="8bdb9-132">-KeyVaultPropertyKeyName</span><span class="sxs-lookup"><span data-stu-id="8bdb9-132">-KeyVaultPropertyKeyName</span></span>
<span data-ttu-id="8bdb9-133">키 자격 증명 모음 키의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-133">The name of the key vault key.</span></span>

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

### <span data-ttu-id="8bdb9-134">-KeyVaultPropertyKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="8bdb9-134">-KeyVaultPropertyKeyVaultUri</span></span>
<span data-ttu-id="8bdb9-135">키 자격 증명 모음의 Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-135">The Uri of the key vault.</span></span>

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

### <span data-ttu-id="8bdb9-136">-KeyVaultPropertyKeyVersion</span><span class="sxs-lookup"><span data-stu-id="8bdb9-136">-KeyVaultPropertyKeyVersion</span></span>
<span data-ttu-id="8bdb9-137">키 자격 증명 모음 키의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-137">The version of the key vault key.</span></span>

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

### <span data-ttu-id="8bdb9-138">-KeyVaultPropertyUserIdentity</span><span class="sxs-lookup"><span data-stu-id="8bdb9-138">-KeyVaultPropertyUserIdentity</span></span>
<span data-ttu-id="8bdb9-139">키에 대한 액세스 권한이 ARM 사용자 할당 ID(리소스 ID)입니다.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-139">The user assigned identity (ARM resource id) that has access to the key.</span></span>

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

### <span data-ttu-id="8bdb9-140">-LanguageExtensionValue</span><span class="sxs-lookup"><span data-stu-id="8bdb9-140">-LanguageExtensionValue</span></span>
<span data-ttu-id="8bdb9-141">언어 확장 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-141">The list of language extensions.</span></span>
<span data-ttu-id="8bdb9-142">생성을 위해 LANGUAGEEXTENSIONVALUE 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-142">To construct, see NOTES section for LANGUAGEEXTENSIONVALUE properties and create a hash table.</span></span>

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

### <span data-ttu-id="8bdb9-143">-Location</span><span class="sxs-lookup"><span data-stu-id="8bdb9-143">-Location</span></span>
<span data-ttu-id="8bdb9-144">리소스가 있는 지리적 위치</span><span class="sxs-lookup"><span data-stu-id="8bdb9-144">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="8bdb9-145">-Name</span><span class="sxs-lookup"><span data-stu-id="8bdb9-145">-Name</span></span>
<span data-ttu-id="8bdb9-146">Kusto 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-146">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="8bdb9-147">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8bdb9-147">-NoWait</span></span>
<span data-ttu-id="8bdb9-148">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="8bdb9-148">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8bdb9-149">-OptimizedAutoscaleIsEnabled</span><span class="sxs-lookup"><span data-stu-id="8bdb9-149">-OptimizedAutoscaleIsEnabled</span></span>
<span data-ttu-id="8bdb9-150">최적화된 자동 조정 기능을 사용하도록 설정되어 있는지 아닌지 나타내는 부울 값입니다.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-150">A boolean value that indicate if the optimized autoscale feature is enabled or not.</span></span>

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

### <span data-ttu-id="8bdb9-151">-OptimizedAutoscaleMaximum</span><span class="sxs-lookup"><span data-stu-id="8bdb9-151">-OptimizedAutoscaleMaximum</span></span>
<span data-ttu-id="8bdb9-152">허용되는 최대 인스턴스 수입니다.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-152">Maximum allowed instances count.</span></span>

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

### <span data-ttu-id="8bdb9-153">-OptimizedAutoscaleMinimum</span><span class="sxs-lookup"><span data-stu-id="8bdb9-153">-OptimizedAutoscaleMinimum</span></span>
<span data-ttu-id="8bdb9-154">허용되는 최소 인스턴스 수입니다.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-154">Minimum allowed instances count.</span></span>

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

### <span data-ttu-id="8bdb9-155">-OptimizedAutoscaleVersion</span><span class="sxs-lookup"><span data-stu-id="8bdb9-155">-OptimizedAutoscaleVersion</span></span>
<span data-ttu-id="8bdb9-156">정의된 템플릿 버전(예: 1)입니다.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-156">The version of the template defined, for instance 1.</span></span>

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

### <span data-ttu-id="8bdb9-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bdb9-157">-ResourceGroupName</span></span>
<span data-ttu-id="8bdb9-158">Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-158">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="8bdb9-159">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="8bdb9-159">-SkuCapacity</span></span>
<span data-ttu-id="8bdb9-160">클러스터의 인스턴스 수입니다.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-160">The number of instances of the cluster.</span></span>

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

### <span data-ttu-id="8bdb9-161">-SkuName</span><span class="sxs-lookup"><span data-stu-id="8bdb9-161">-SkuName</span></span>
<span data-ttu-id="8bdb9-162">SKU 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-162">SKU name.</span></span>

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

### <span data-ttu-id="8bdb9-163">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="8bdb9-163">-SkuTier</span></span>
<span data-ttu-id="8bdb9-164">SKU 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-164">SKU tier.</span></span>

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

### <span data-ttu-id="8bdb9-165">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8bdb9-165">-SubscriptionId</span></span>
<span data-ttu-id="8bdb9-166">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-166">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8bdb9-167">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-167">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8bdb9-168">-Tag</span><span class="sxs-lookup"><span data-stu-id="8bdb9-168">-Tag</span></span>
<span data-ttu-id="8bdb9-169">리소스 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-169">Resource tags.</span></span>

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

### <span data-ttu-id="8bdb9-170">-TrustedExternalTenant</span><span class="sxs-lookup"><span data-stu-id="8bdb9-170">-TrustedExternalTenant</span></span>
<span data-ttu-id="8bdb9-171">클러스터의 외부 테넌트입니다.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-171">The cluster's external tenants.</span></span>
<span data-ttu-id="8bdb9-172">생성을 위해 TRUSTEDEXTERNALTENANT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-172">To construct, see NOTES section for TRUSTEDEXTERNALTENANT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8bdb9-173">-VirtualNetworkConfigurationDataManagementPublicIPId</span><span class="sxs-lookup"><span data-stu-id="8bdb9-173">-VirtualNetworkConfigurationDataManagementPublicIPId</span></span>
<span data-ttu-id="8bdb9-174">데이터 관리의 서비스 공용 IP 주소 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-174">Data management's service public IP address resource id.</span></span>

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

### <span data-ttu-id="8bdb9-175">-VirtualNetworkConfigurationEnginePublicIPId</span><span class="sxs-lookup"><span data-stu-id="8bdb9-175">-VirtualNetworkConfigurationEnginePublicIPId</span></span>
<span data-ttu-id="8bdb9-176">엔진 서비스의 공용 IP 주소 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-176">Engine service's public IP address resource id.</span></span>

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

### <span data-ttu-id="8bdb9-177">-VirtualNetworkConfigurationSubnetId</span><span class="sxs-lookup"><span data-stu-id="8bdb9-177">-VirtualNetworkConfigurationSubnetId</span></span>
<span data-ttu-id="8bdb9-178">서브넷 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-178">The subnet resource id.</span></span>

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

### <span data-ttu-id="8bdb9-179">-Zone</span><span class="sxs-lookup"><span data-stu-id="8bdb9-179">-Zone</span></span>
<span data-ttu-id="8bdb9-180">클러스터의 가용성 영역입니다.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-180">The availability zones of the cluster.</span></span>

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

### <span data-ttu-id="8bdb9-181">-확인</span><span class="sxs-lookup"><span data-stu-id="8bdb9-181">-Confirm</span></span>
<span data-ttu-id="8bdb9-182">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bdb9-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bdb9-183">-WhatIf</span></span>
<span data-ttu-id="8bdb9-184">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bdb9-185">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8bdb9-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bdb9-186">CommonParameters</span></span>
<span data-ttu-id="8bdb9-187">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bdb9-188">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8bdb9-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bdb9-189">입력</span><span class="sxs-lookup"><span data-stu-id="8bdb9-189">INPUTS</span></span>

## <span data-ttu-id="8bdb9-190">출력</span><span class="sxs-lookup"><span data-stu-id="8bdb9-190">OUTPUTS</span></span>

### <span data-ttu-id="8bdb9-191">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span><span class="sxs-lookup"><span data-stu-id="8bdb9-191">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span></span>

## <span data-ttu-id="8bdb9-192">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8bdb9-192">NOTES</span></span>

<span data-ttu-id="8bdb9-193">별칭</span><span class="sxs-lookup"><span data-stu-id="8bdb9-193">ALIASES</span></span>

<span data-ttu-id="8bdb9-194">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="8bdb9-194">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8bdb9-195">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-195">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8bdb9-196">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-196">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8bdb9-197">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: 언어 확장 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-197">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="8bdb9-198">`[Name <LanguageExtensionName?>]`: 언어 확장 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-198">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

<span data-ttu-id="8bdb9-199">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: 클러스터의 외부 테넌트입니다.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-199">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: The cluster's external tenants.</span></span>
  - <span data-ttu-id="8bdb9-200">`[Value <String>]`: 외부 테넌트를 나타내는 GUID입니다.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-200">`[Value <String>]`: GUID representing an external tenant.</span></span>

## <span data-ttu-id="8bdb9-201">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8bdb9-201">RELATED LINKS</span></span>

