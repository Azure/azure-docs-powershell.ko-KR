---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/powershell/module/az.hanaonazure/new-azsapmonitorproviderinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitorProviderInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitorProviderInstance.md
ms.openlocfilehash: eb84936310be355ece858884a1e27b7cc954cb51
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013355"
---
# <span data-ttu-id="27435-101">New-AzSapMonitorProviderInstance</span><span class="sxs-lookup"><span data-stu-id="27435-101">New-AzSapMonitorProviderInstance</span></span>

## <span data-ttu-id="27435-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27435-102">SYNOPSIS</span></span>
<span data-ttu-id="27435-103">지정된 구독, 리소스 그룹, SapMonitor 이름 및 리소스 이름에 대한 공급자 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="27435-103">Creates a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="27435-104">구문</span><span class="sxs-lookup"><span data-stu-id="27435-104">SYNTAX</span></span>

### <span data-ttu-id="27435-105">ByString(기본값)</span><span class="sxs-lookup"><span data-stu-id="27435-105">ByString (Default)</span></span>
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -HanaDatabaseName <String> -HanaDatabasePassword <SecureString> -HanaDatabaseSqlPort <Int32>
 -HanaDatabaseUsername <String> -HanaHostname <String> -ProviderType <String> [-SubscriptionId <String>]
 [-Metadata <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="27435-106">ByDict</span><span class="sxs-lookup"><span data-stu-id="27435-106">ByDict</span></span>
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -InstanceProperty <Hashtable> -ProviderType <String> [-SubscriptionId <String>] [-Metadata <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="27435-107">ByKeyVault</span><span class="sxs-lookup"><span data-stu-id="27435-107">ByKeyVault</span></span>
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -HanaDatabaseName <String> -HanaDatabasePasswordKeyVaultResourceId <String>
 -HanaDatabasePasswordSecretId <String> -HanaDatabaseSqlPort <Int32> -HanaDatabaseUsername <String>
 -HanaHostname <String> -ProviderType <String> [-SubscriptionId <String>] [-Metadata <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="27435-108">설명</span><span class="sxs-lookup"><span data-stu-id="27435-108">DESCRIPTION</span></span>
<span data-ttu-id="27435-109">지정된 구독, 리소스 그룹, SapMonitor 이름 및 리소스 이름에 대한 공급자 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="27435-109">Creates a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="27435-110">예제</span><span class="sxs-lookup"><span data-stu-id="27435-110">EXAMPLES</span></span>

### <span data-ttu-id="27435-111">예제 1: HANA에 대한 문자열로 SAP 모니터 인스턴스 만들기</span><span class="sxs-lookup"><span data-stu-id="27435-111">Example 1: Create an instance of SAP monitor by string for HANA</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -Name ps-sapmonitorins-t01 -SapMonitorName yemingmonitor -ProviderType SapHana -HanaHostname 'hdb1-0' -HanaDatabaseName 'SYSTEMDB' -HanaDatabaseSqlPort 30015 -HanaDatabaseUsername SYSTEM -HanaDatabasePassword (ConvertTo-SecureString "Manager1" -AsPlainText -Force)

Name                 Type
----                 ----
ps-sapmonitorins-t01 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="27435-112">이 명령은 HANA에 대한 문자열로 SAP 모니터 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="27435-112">This command creates an instance of SAP monitor by string for HANA.</span></span>

### <span data-ttu-id="27435-113">예제 2: HANA용 키 자격 증명 모음으로 SAP 모니터 인스턴스 만들기</span><span class="sxs-lookup"><span data-stu-id="27435-113">Example 2: Create an instance of SAP monitor by key vault for HANA</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName sapMonitor-vayh7q-test -ProviderType SapHana -HanaHostname 'hdb1-0' -HanaDatabaseName 'SYSTEMDB' -HanaDatabaseSqlPort 30015 -HanaDatabaseUsername SYSTEM -HanaDatabasePasswordSecretId https://kv-9gosjc-test.vault.azure.net/secrets/hanaPassword/bf516d1dfcc144138e5cf55114f3344b -HanaDatabasePasswordKeyVaultResourceId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/costmanagement-rg-8p50xe/providers/Microsoft.KeyVault/vaults/kv-9gosjc-test -Name sapins-kv-test

Name           Type
----           ----
sapins-kv-test Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="27435-114">이 명령은 HANA의 키 자격 증명 모음에 따라 SAP 모니터 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="27435-114">This command creates an instance of SAP monitor by key vault for HANA.</span></span>

### <span data-ttu-id="27435-115">예제 3: PrometheusHaCluster에 대한 사전으로 SAP 모니터 인스턴스 만들기</span><span class="sxs-lookup"><span data-stu-id="27435-115">Example 3: Create an instance of SAP monitor by dictionary for PrometheusHaCluster</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName donaliu-HN1 -Name dolauli-instance-promclt   -SapMonitorName dolauli-test04 -ProviderType PrometheusHaCluster -InstanceProperty @{prometheusUrl='http://10.4.1.10:9664/metrics'}


Name                     Type
----                     ----
dolauli-instance-promclt Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="27435-116">이 명령은 PrometheusHaCluster에 대한 사전으로 SAP 모니터 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="27435-116">This command creates an instance of SAP monitor by dictionary for PrometheusHaCluster.</span></span>

### <span data-ttu-id="27435-117">예제 4: PrometheusOS에 대한 사전으로 SAP 모니터 인스턴스 만들기</span><span class="sxs-lookup"><span data-stu-id="27435-117">Example 4: Create an instance of SAP monitor by dictionary for PrometheusOS</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName donaliu-HN1 -Name dolauli-instance-prom   -SapMonitorName dolauli-test04 -ProviderType PrometheusOS -InstanceProperty @{prometheusUrl='http://10.3.1.6:9100/metrics'}

Name                  Type
----                  ----
dolauli-instance-prom Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="27435-118">이 명령은 PrometheusOS에 대한 사전으로 SAP 모니터 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="27435-118">This command creates an instance of SAP monitor by dictionary for PrometheusOS.</span></span>

### <span data-ttu-id="27435-119">예제 5: MsSqlServer에 대한 사전으로 SAP 모니터 인스턴스 만들기</span><span class="sxs-lookup"><span data-stu-id="27435-119">Example 5: Create an instance of SAP monitor by dictionary for MsSqlServer</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName donaliu-HN1 -Name dolauli-instance-ms   -SapMonitorName dolauli-test04 -ProviderType MsSqlServer -InstanceProperty @{sqlHostname="10.4.8.90";sqlPort=1433;sqlUsername="AMFSS";sqlPassword="fakepassword"}

Name                Type
----                ----
dolauli-instance-ms Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="27435-120">이 명령은 MsSqlServer에 대한 사전으로 SAP 모니터 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="27435-120">This command creates an instance of SAP monitor by dictionary for MsSqlServer.</span></span>

### <span data-ttu-id="27435-121">예제 6: SapHana에 대한 사전으로 SAP 모니터 인스턴스 만들기</span><span class="sxs-lookup"><span data-stu-id="27435-121">Example 6: Create an instance of SAP monitor by dictionary for SapHana</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName donaliu-HN1 -Name dolauli-instance-hana   -SapMonitorName dolauli-test04 -ProviderType SapHana -InstanceProperty @{hanaHostname="10.1.2.6";hanaDbName="SYSTEMDB";hanaDbSqlPort=30113;hanaDbUsername="SYSTEM"; hanaDbPassword="Manager1"}

Name                  Type
----                  ----
dolauli-instance-hana Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="27435-122">이 명령은 SapHana에 대한 사전으로 SAP 모니터 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="27435-122">This command creates an instance of SAP monitor by dictionary for SapHana.</span></span>

## <span data-ttu-id="27435-123">매개 변수</span><span class="sxs-lookup"><span data-stu-id="27435-123">PARAMETERS</span></span>

### <span data-ttu-id="27435-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="27435-124">-AsJob</span></span>
<span data-ttu-id="27435-125">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="27435-125">Run the command as a job</span></span>

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

### <span data-ttu-id="27435-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27435-126">-DefaultProfile</span></span>
<span data-ttu-id="27435-127">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="27435-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27435-128">-HanaDatabaseName</span><span class="sxs-lookup"><span data-stu-id="27435-128">-HanaDatabaseName</span></span>
<span data-ttu-id="27435-129">SAP HANA 인스턴스의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="27435-129">The database name of SAP HANA instance.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyVault, ByString
Aliases: HanaDbName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27435-130">-HanaDatabasePassword</span><span class="sxs-lookup"><span data-stu-id="27435-130">-HanaDatabasePassword</span></span>
<span data-ttu-id="27435-131">SAP HANA 인스턴스 데이터베이스의 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="27435-131">The password of the database of SAP HANA instance.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByString
Aliases: HanaDbPassword

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27435-132">-HanaDatabasePasswordKeyVaultResourceId</span><span class="sxs-lookup"><span data-stu-id="27435-132">-HanaDatabasePasswordKeyVaultResourceId</span></span>
<span data-ttu-id="27435-133">HANA 자격 증명을 포함하는 Key Vault의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="27435-133">Resource ID of the Key Vault that contains the HANA credentials.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyVault
Aliases: HanaDbPasswordKeyVaultId, KeyVaultId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27435-134">-HanaDatabasePasswordSecretId</span><span class="sxs-lookup"><span data-stu-id="27435-134">-HanaDatabasePasswordSecretId</span></span>
<span data-ttu-id="27435-135">HANA 자격 증명을 포함하는 Key Vault 비밀에 대한 비밀 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="27435-135">Secret identifier to the Key Vault secret that contains the HANA credentials.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyVault
Aliases: HanaDbPasswordSecretId, SecretId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27435-136">-HanaDatabaseSqlPort</span><span class="sxs-lookup"><span data-stu-id="27435-136">-HanaDatabaseSqlPort</span></span>
<span data-ttu-id="27435-137">SAP HANA 인스턴스의 데이터베이스의 SQL 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="27435-137">The SQL port of the database of SAP HANA instance.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByKeyVault, ByString
Aliases: HanaDbSqlPort

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27435-138">-HanaDatabaseUsername</span><span class="sxs-lookup"><span data-stu-id="27435-138">-HanaDatabaseUsername</span></span>
<span data-ttu-id="27435-139">SAP HANA 인스턴스의 데이터베이스 사용자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="27435-139">The username of the database of SAP HANA instance.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyVault, ByString
Aliases: HanaDbUsername

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27435-140">-HanaHostname</span><span class="sxs-lookup"><span data-stu-id="27435-140">-HanaHostname</span></span>
<span data-ttu-id="27435-141">SAP HANA 인스턴스의 호스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="27435-141">The hostname of SAP HANA instance.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyVault, ByString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27435-142">-InstanceProperty</span><span class="sxs-lookup"><span data-stu-id="27435-142">-InstanceProperty</span></span>
<span data-ttu-id="27435-143">HANA 인스턴스의 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="27435-143">The property of HANA instance.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByDict
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27435-144">-메타데이터</span><span class="sxs-lookup"><span data-stu-id="27435-144">-Metadata</span></span>
<span data-ttu-id="27435-145">공급자 인스턴스의 메타데이터를 포함하는 JSON 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="27435-145">A JSON string containing metadata of the provider instance.</span></span>

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

### <span data-ttu-id="27435-146">-Name</span><span class="sxs-lookup"><span data-stu-id="27435-146">-Name</span></span>
<span data-ttu-id="27435-147">공급자 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="27435-147">Name of the provider instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProviderInstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27435-148">-NoWait</span><span class="sxs-lookup"><span data-stu-id="27435-148">-NoWait</span></span>
<span data-ttu-id="27435-149">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="27435-149">Run the command asynchronously</span></span>

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

### <span data-ttu-id="27435-150">-ProviderType</span><span class="sxs-lookup"><span data-stu-id="27435-150">-ProviderType</span></span>
<span data-ttu-id="27435-151">공급자 인스턴스의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="27435-151">The type of provider instance.</span></span>
<span data-ttu-id="27435-152">지원되는 값은 "SapHana"입니다.</span><span class="sxs-lookup"><span data-stu-id="27435-152">Supported values are: "SapHana".</span></span>

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

### <span data-ttu-id="27435-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27435-153">-ResourceGroupName</span></span>
<span data-ttu-id="27435-154">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="27435-154">Name of the resource group.</span></span>

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

### <span data-ttu-id="27435-155">-SapMonitorName</span><span class="sxs-lookup"><span data-stu-id="27435-155">-SapMonitorName</span></span>
<span data-ttu-id="27435-156">SAP 모니터 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="27435-156">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="27435-157">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="27435-157">-SubscriptionId</span></span>
<span data-ttu-id="27435-158">Microsoft Azure 구독을 고유하게 식별하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="27435-158">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="27435-159">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="27435-159">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="27435-160">-확인</span><span class="sxs-lookup"><span data-stu-id="27435-160">-Confirm</span></span>
<span data-ttu-id="27435-161">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="27435-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27435-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27435-162">-WhatIf</span></span>
<span data-ttu-id="27435-163">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="27435-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27435-164">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="27435-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27435-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27435-165">CommonParameters</span></span>
<span data-ttu-id="27435-166">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="27435-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27435-167">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="27435-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27435-168">입력</span><span class="sxs-lookup"><span data-stu-id="27435-168">INPUTS</span></span>

## <span data-ttu-id="27435-169">출력</span><span class="sxs-lookup"><span data-stu-id="27435-169">OUTPUTS</span></span>

### <span data-ttu-id="27435-170">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.IProviderInstance</span><span class="sxs-lookup"><span data-stu-id="27435-170">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.IProviderInstance</span></span>

## <span data-ttu-id="27435-171">참고 사항</span><span class="sxs-lookup"><span data-stu-id="27435-171">NOTES</span></span>

<span data-ttu-id="27435-172">별칭</span><span class="sxs-lookup"><span data-stu-id="27435-172">ALIASES</span></span>

## <span data-ttu-id="27435-173">관련 링크</span><span class="sxs-lookup"><span data-stu-id="27435-173">RELATED LINKS</span></span>

