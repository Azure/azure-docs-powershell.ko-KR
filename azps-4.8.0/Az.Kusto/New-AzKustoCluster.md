---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoCluster.md
ms.openlocfilehash: b8b6c11da622b7fa0ee67dc418f2055dd72c1d13
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213553"
---
# <span data-ttu-id="06740-101">New-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="06740-101">New-AzKustoCluster</span></span>

## <span data-ttu-id="06740-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06740-102">SYNOPSIS</span></span>
<span data-ttu-id="06740-103">클러스터에 대 한 Kusto 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="06740-103">Create or update a Kusto cluster.</span></span>

## <span data-ttu-id="06740-104">구문과</span><span class="sxs-lookup"><span data-stu-id="06740-104">SYNTAX</span></span>

```
New-AzKustoCluster -Name <String> -ResourceGroupName <String> -Location <String> -SkuName <AzureSkuName>
 -SkuTier <AzureSkuTier> [-SubscriptionId <String>] [-EnableDiskEncryption] [-EnableDoubleEncryption]
 [-EnablePurge] [-EnableStreamingIngest] [-IdentityType <IdentityType>]
 [-IdentityUserAssignedIdentity <Hashtable>] [-KeyVaultPropertyKeyName <String>]
 [-KeyVaultPropertyKeyVaultUri <String>] [-KeyVaultPropertyKeyVersion <String>]
 [-LanguageExtensionValue <ILanguageExtension[]>] [-OptimizedAutoscaleIsEnabled]
 [-OptimizedAutoscaleMaximum <Int32>] [-OptimizedAutoscaleMinimum <Int32>]
 [-OptimizedAutoscaleVersion <Int32>] [-SkuCapacity <Int32>] [-Tag <Hashtable>]
 [-TrustedExternalTenant <ITrustedExternalTenant[]>]
 [-VirtualNetworkConfigurationDataManagementPublicIPId <String>]
 [-VirtualNetworkConfigurationEnginePublicIPId <String>] [-VirtualNetworkConfigurationSubnetId <String>]
 [-Zone <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="06740-105">설명은</span><span class="sxs-lookup"><span data-stu-id="06740-105">DESCRIPTION</span></span>
<span data-ttu-id="06740-106">클러스터에 대 한 Kusto 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="06740-106">Create or update a Kusto cluster.</span></span>

## <span data-ttu-id="06740-107">예제의</span><span class="sxs-lookup"><span data-stu-id="06740-107">EXAMPLES</span></span>

### <span data-ttu-id="06740-108">예제 1: 클러스터에 새 Kusto 만들기</span><span class="sxs-lookup"><span data-stu-id="06740-108">Example 1: Create a new Kusto cluster</span></span>
```powershell
PS C:\> New-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -Location 'East US' -SkuName Standard_D11_v2 -SkuTier Standard -EnableDoubleEncryption true

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="06740-109">위의 명령은 리소스 그룹 "testrg"에 "testnewkustocluster" 이라는 새 클러스터에 대 한 새로운 Kusto를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="06740-109">The above command creates a new Kusto cluster named "testnewkustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="06740-110">변수</span><span class="sxs-lookup"><span data-stu-id="06740-110">PARAMETERS</span></span>

### <span data-ttu-id="06740-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="06740-111">-AsJob</span></span>
<span data-ttu-id="06740-112">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="06740-112">Run the command as a job</span></span>

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

### <span data-ttu-id="06740-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06740-113">-DefaultProfile</span></span>
<span data-ttu-id="06740-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="06740-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06740-115">-EnableDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="06740-115">-EnableDiskEncryption</span></span>
<span data-ttu-id="06740-116">클러스터의 디스크가 암호화 되었는지 여부를 나타내는 부울 값입니다.</span><span class="sxs-lookup"><span data-stu-id="06740-116">A boolean value that indicates if the cluster's disks are encrypted.</span></span>

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

### <span data-ttu-id="06740-117">-EnableDoubleEncryption</span><span class="sxs-lookup"><span data-stu-id="06740-117">-EnableDoubleEncryption</span></span>
<span data-ttu-id="06740-118">이중 암호화를 사용 하는지 여부를 나타내는 부울 값입니다.</span><span class="sxs-lookup"><span data-stu-id="06740-118">A boolean value that indicates if double encryption is enabled.</span></span>

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

### <span data-ttu-id="06740-119">-EnablePurge</span><span class="sxs-lookup"><span data-stu-id="06740-119">-EnablePurge</span></span>
<span data-ttu-id="06740-120">지우기 작업을 사용할 수 있는지 여부를 나타내는 부울 값입니다.</span><span class="sxs-lookup"><span data-stu-id="06740-120">A boolean value that indicates if the purge operations are enabled.</span></span>

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

### <span data-ttu-id="06740-121">-EnableStreamingIngest</span><span class="sxs-lookup"><span data-stu-id="06740-121">-EnableStreamingIngest</span></span>
<span data-ttu-id="06740-122">스트리밍 수집을 사용할 수 있는지 여부를 나타내는 부울 값입니다.</span><span class="sxs-lookup"><span data-stu-id="06740-122">A boolean value that indicates if the streaming ingest is enabled.</span></span>

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

### <span data-ttu-id="06740-123">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="06740-123">-IdentityType</span></span>
<span data-ttu-id="06740-124">Id 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="06740-124">The identity type.</span></span>

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

### <span data-ttu-id="06740-125">-IdentityUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="06740-125">-IdentityUserAssignedIdentity</span></span>
<span data-ttu-id="06740-126">Kusto cluster와 연결 된 사용자 id 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="06740-126">The list of user identities associated with the Kusto cluster.</span></span>
<span data-ttu-id="06740-127">사용자 id 사전 키 참조는 '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName} ' 형식으로 팔로 리소스 id를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="06740-127">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="06740-128">-KeyVaultPropertyKeyName</span><span class="sxs-lookup"><span data-stu-id="06740-128">-KeyVaultPropertyKeyName</span></span>
<span data-ttu-id="06740-129">키 보관소 키의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="06740-129">The name of the key vault key.</span></span>

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

### <span data-ttu-id="06740-130">-KeyVaultPropertyKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="06740-130">-KeyVaultPropertyKeyVaultUri</span></span>
<span data-ttu-id="06740-131">키 보관소의 Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="06740-131">The Uri of the key vault.</span></span>

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

### <span data-ttu-id="06740-132">-KeyVaultPropertyKeyVersion</span><span class="sxs-lookup"><span data-stu-id="06740-132">-KeyVaultPropertyKeyVersion</span></span>
<span data-ttu-id="06740-133">키 보관소 키의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="06740-133">The version of the key vault key.</span></span>

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

### <span data-ttu-id="06740-134">-LanguageExtensionValue</span><span class="sxs-lookup"><span data-stu-id="06740-134">-LanguageExtensionValue</span></span>
<span data-ttu-id="06740-135">언어 확장 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="06740-135">The list of language extensions.</span></span>
<span data-ttu-id="06740-136">생성 하려면 LANGUAGEEXTENSIONVALUE 속성에 대 한 메모 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="06740-136">To construct, see NOTES section for LANGUAGEEXTENSIONVALUE properties and create a hash table.</span></span>

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

### <span data-ttu-id="06740-137">-위치</span><span class="sxs-lookup"><span data-stu-id="06740-137">-Location</span></span>
<span data-ttu-id="06740-138">리소스가 상주 하는 지리적 위치</span><span class="sxs-lookup"><span data-stu-id="06740-138">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="06740-139">-이름</span><span class="sxs-lookup"><span data-stu-id="06740-139">-Name</span></span>
<span data-ttu-id="06740-140">Kusto의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="06740-140">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="06740-141">-NoWait</span><span class="sxs-lookup"><span data-stu-id="06740-141">-NoWait</span></span>
<span data-ttu-id="06740-142">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="06740-142">Run the command asynchronously</span></span>

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

### <span data-ttu-id="06740-143">-OptimizedAutoscaleIsEnabled</span><span class="sxs-lookup"><span data-stu-id="06740-143">-OptimizedAutoscaleIsEnabled</span></span>
<span data-ttu-id="06740-144">최적화 된 자동 크기 조정 기능을 사용할 수 있는지 여부를 나타내는 부울 값입니다.</span><span class="sxs-lookup"><span data-stu-id="06740-144">A boolean value that indicate if the optimized autoscale feature is enabled or not.</span></span>

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

### <span data-ttu-id="06740-145">-OptimizedAutoscaleMaximum</span><span class="sxs-lookup"><span data-stu-id="06740-145">-OptimizedAutoscaleMaximum</span></span>
<span data-ttu-id="06740-146">허용 되는 최대 인스턴스 수입니다.</span><span class="sxs-lookup"><span data-stu-id="06740-146">Maximum allowed instances count.</span></span>

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

### <span data-ttu-id="06740-147">-OptimizedAutoscaleMinimum</span><span class="sxs-lookup"><span data-stu-id="06740-147">-OptimizedAutoscaleMinimum</span></span>
<span data-ttu-id="06740-148">허용 되는 최소 인스턴스 수입니다.</span><span class="sxs-lookup"><span data-stu-id="06740-148">Minimum allowed instances count.</span></span>

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

### <span data-ttu-id="06740-149">-OptimizedAutoscaleVersion</span><span class="sxs-lookup"><span data-stu-id="06740-149">-OptimizedAutoscaleVersion</span></span>
<span data-ttu-id="06740-150">인스턴스 1에 대해 정의 된 서식 파일의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="06740-150">The version of the template defined, for instance 1.</span></span>

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

### <span data-ttu-id="06740-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06740-151">-ResourceGroupName</span></span>
<span data-ttu-id="06740-152">Kusto cluster를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="06740-152">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="06740-153">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="06740-153">-SkuCapacity</span></span>
<span data-ttu-id="06740-154">클러스터 인스턴스의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="06740-154">The number of instances of the cluster.</span></span>

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

### <span data-ttu-id="06740-155">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="06740-155">-SkuName</span></span>
<span data-ttu-id="06740-156">SKU 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="06740-156">SKU name.</span></span>

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

### <span data-ttu-id="06740-157">-서 고 U계층</span><span class="sxs-lookup"><span data-stu-id="06740-157">-SkuTier</span></span>
<span data-ttu-id="06740-158">SKU 계층.</span><span class="sxs-lookup"><span data-stu-id="06740-158">SKU tier.</span></span>

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

### <span data-ttu-id="06740-159">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="06740-159">-SubscriptionId</span></span>
<span data-ttu-id="06740-160">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="06740-160">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="06740-161">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="06740-161">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="06740-162">태그</span><span class="sxs-lookup"><span data-stu-id="06740-162">-Tag</span></span>
<span data-ttu-id="06740-163">리소스 태그.</span><span class="sxs-lookup"><span data-stu-id="06740-163">Resource tags.</span></span>

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

### <span data-ttu-id="06740-164">-TrustedExternalTenant</span><span class="sxs-lookup"><span data-stu-id="06740-164">-TrustedExternalTenant</span></span>
<span data-ttu-id="06740-165">클러스터의 외부 테 넌 트입니다.</span><span class="sxs-lookup"><span data-stu-id="06740-165">The cluster's external tenants.</span></span>
<span data-ttu-id="06740-166">생성 하려면 TRUSTEDEXTERNALTENANT 속성에 대 한 메모 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="06740-166">To construct, see NOTES section for TRUSTEDEXTERNALTENANT properties and create a hash table.</span></span>

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

### <span data-ttu-id="06740-167">-VirtualNetworkConfigurationDataManagementPublicIPId</span><span class="sxs-lookup"><span data-stu-id="06740-167">-VirtualNetworkConfigurationDataManagementPublicIPId</span></span>
<span data-ttu-id="06740-168">데이터 관리 서비스 공용 IP 주소 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="06740-168">Data management's service public IP address resource id.</span></span>

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

### <span data-ttu-id="06740-169">-VirtualNetworkConfigurationEnginePublicIPId</span><span class="sxs-lookup"><span data-stu-id="06740-169">-VirtualNetworkConfigurationEnginePublicIPId</span></span>
<span data-ttu-id="06740-170">엔진 서비스의 공용 IP 주소 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="06740-170">Engine service's public IP address resource id.</span></span>

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

### <span data-ttu-id="06740-171">-VirtualNetworkConfigurationSubnetId</span><span class="sxs-lookup"><span data-stu-id="06740-171">-VirtualNetworkConfigurationSubnetId</span></span>
<span data-ttu-id="06740-172">서브넷 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="06740-172">The subnet resource id.</span></span>

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

### <span data-ttu-id="06740-173">-Zone</span><span class="sxs-lookup"><span data-stu-id="06740-173">-Zone</span></span>
<span data-ttu-id="06740-174">클러스터의 가용성 영역입니다.</span><span class="sxs-lookup"><span data-stu-id="06740-174">The availability zones of the cluster.</span></span>

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

### <span data-ttu-id="06740-175">-확인</span><span class="sxs-lookup"><span data-stu-id="06740-175">-Confirm</span></span>
<span data-ttu-id="06740-176">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="06740-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06740-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06740-177">-WhatIf</span></span>
<span data-ttu-id="06740-178">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="06740-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06740-179">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="06740-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06740-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06740-180">CommonParameters</span></span>
<span data-ttu-id="06740-181">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="06740-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06740-182">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="06740-182">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06740-183">입력</span><span class="sxs-lookup"><span data-stu-id="06740-183">INPUTS</span></span>

## <span data-ttu-id="06740-184">출력</span><span class="sxs-lookup"><span data-stu-id="06740-184">OUTPUTS</span></span>

### <span data-ttu-id="06740-185">Microsoft. Api20200614. ICluster에 대 한.</span><span class="sxs-lookup"><span data-stu-id="06740-185">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICluster</span></span>

## <span data-ttu-id="06740-186">상속자</span><span class="sxs-lookup"><span data-stu-id="06740-186">NOTES</span></span>

<span data-ttu-id="06740-187">별칭과</span><span class="sxs-lookup"><span data-stu-id="06740-187">ALIASES</span></span>

<span data-ttu-id="06740-188">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="06740-188">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="06740-189">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="06740-189">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="06740-190">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="06740-190">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="06740-191">LANGUAGEEXTENSIONVALUE <ILanguageExtension [] >: 언어 확장 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="06740-191">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="06740-192">`[Name <LanguageExtensionName?>]`: 언어 확장 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="06740-192">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

<span data-ttu-id="06740-193">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant [] >: 클러스터의 외부 테 넌 트.</span><span class="sxs-lookup"><span data-stu-id="06740-193">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: The cluster's external tenants.</span></span>
  - <span data-ttu-id="06740-194">`[Value <String>]`: 외부 테 넌 트를 나타내는 GUID입니다.</span><span class="sxs-lookup"><span data-stu-id="06740-194">`[Value <String>]`: GUID representing an external tenant.</span></span>

## <span data-ttu-id="06740-195">관련 링크</span><span class="sxs-lookup"><span data-stu-id="06740-195">RELATED LINKS</span></span>

