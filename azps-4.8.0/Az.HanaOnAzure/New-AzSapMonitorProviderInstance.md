---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/new-azsapmonitorproviderinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitorProviderInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitorProviderInstance.md
ms.openlocfilehash: f0d8486bc26043ee4f2cb2126c7ffdc64829a7cd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94049055"
---
# <span data-ttu-id="96093-101">New-AzSapMonitorProviderInstance</span><span class="sxs-lookup"><span data-stu-id="96093-101">New-AzSapMonitorProviderInstance</span></span>

## <span data-ttu-id="96093-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96093-102">SYNOPSIS</span></span>
<span data-ttu-id="96093-103">지정 된 구독, 리소스 그룹, SapMonitor 이름 및 리소스 이름에 대 한 공급자 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="96093-103">Creates a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="96093-104">구문과</span><span class="sxs-lookup"><span data-stu-id="96093-104">SYNTAX</span></span>

### <span data-ttu-id="96093-105">ByString (기본값)</span><span class="sxs-lookup"><span data-stu-id="96093-105">ByString (Default)</span></span>
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -HanaDatabaseName <String> -HanaDatabasePassword <SecureString> -HanaDatabaseSqlPort <Int32>
 -HanaDatabaseUsername <String> -HanaHostname <String> -ProviderType <String> [-SubscriptionId <String>]
 [-Metadata <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="96093-106">ByKeyVault</span><span class="sxs-lookup"><span data-stu-id="96093-106">ByKeyVault</span></span>
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -HanaDatabaseName <String> -HanaDatabasePasswordKeyVaultResourceId <String>
 -HanaDatabasePasswordSecretId <String> -HanaDatabaseSqlPort <Int32> -HanaDatabaseUsername <String>
 -HanaHostname <String> -ProviderType <String> [-SubscriptionId <String>] [-Metadata <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="96093-107">설명은</span><span class="sxs-lookup"><span data-stu-id="96093-107">DESCRIPTION</span></span>
<span data-ttu-id="96093-108">지정 된 구독, 리소스 그룹, SapMonitor 이름 및 리소스 이름에 대 한 공급자 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="96093-108">Creates a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="96093-109">예제의</span><span class="sxs-lookup"><span data-stu-id="96093-109">EXAMPLES</span></span>

### <span data-ttu-id="96093-110">예제 1: HANA에 대 한 문자열을 기준으로 SAP 모니터의 인스턴스 만들기</span><span class="sxs-lookup"><span data-stu-id="96093-110">Example 1: Create an instance of SAP monitor by string for HANA</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -Name ps-sapmonitorins-t01 -SapMonitorName yemingmonitor -ProviderType SapHana -HanaHostname 'hdb1-0' -HanaDatabaseName 'SYSTEMDB' -HanaDatabaseSqlPort 30015 -HanaDatabaseUsername SYSTEM -HanaDatabasePassword (ConvertTo-SecureString "Manager1" -AsPlainText -Force)

Name                 Type
----                 ----
ps-sapmonitorins-t01 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="96093-111">이 명령은 HANA 용 문자열을 기준으로 SAP 모니터의 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="96093-111">This command creates an instance of SAP monitor by string for HANA.</span></span>

### <span data-ttu-id="96093-112">예제 2: HANA 용 키 보관소에 따라 SAP 모니터의 인스턴스 만들기</span><span class="sxs-lookup"><span data-stu-id="96093-112">Example 2: Create an instance of SAP monitor by key vault for HANA</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName sapMonitor-vayh7q-test -ProviderType SapHana -HanaHostname 'hdb1-0' -HanaDatabaseName 'SYSTEMDB' -HanaDatabaseSqlPort 30015 -HanaDatabaseUsername SYSTEM -HanaDatabasePasswordSecretId https://kv-9gosjc-test.vault.azure.net/secrets/hanaPassword/bf516d1dfcc144138e5cf55114f3344b -HanaDatabasePasswordKeyVaultResourceId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/costmanagement-rg-8p50xe/providers/Microsoft.KeyVault/vaults/kv-9gosjc-test -Name sapins-kv-test

Name           Type
----           ----
sapins-kv-test Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="96093-113">이 명령은 HANA 용 키 보관소에 따라 SAP 모니터의 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="96093-113">This command creates an instance of SAP monitor by key vault for HANA.</span></span>

## <span data-ttu-id="96093-114">변수</span><span class="sxs-lookup"><span data-stu-id="96093-114">PARAMETERS</span></span>

### <span data-ttu-id="96093-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="96093-115">-AsJob</span></span>
<span data-ttu-id="96093-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="96093-116">Run the command as a job</span></span>

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

### <span data-ttu-id="96093-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96093-117">-DefaultProfile</span></span>
<span data-ttu-id="96093-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="96093-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96093-119">-HanaDatabaseName</span><span class="sxs-lookup"><span data-stu-id="96093-119">-HanaDatabaseName</span></span>
<span data-ttu-id="96093-120">SAP HANA 인스턴스의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="96093-120">The database name of SAP HANA instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HanaDbName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96093-121">-HanaDatabasePassword</span><span class="sxs-lookup"><span data-stu-id="96093-121">-HanaDatabasePassword</span></span>
<span data-ttu-id="96093-122">SAP HANA 인스턴스 데이터베이스의 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="96093-122">The password of the database of SAP HANA instance.</span></span>

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

### <span data-ttu-id="96093-123">-HanaDatabasePasswordKeyVaultResourceId</span><span class="sxs-lookup"><span data-stu-id="96093-123">-HanaDatabasePasswordKeyVaultResourceId</span></span>
<span data-ttu-id="96093-124">HANA 자격 증명을 포함 하는 키 보관소의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="96093-124">Resource ID of the Key Vault that contains the HANA credentials.</span></span>

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

### <span data-ttu-id="96093-125">-HanaDatabasePasswordSecretId</span><span class="sxs-lookup"><span data-stu-id="96093-125">-HanaDatabasePasswordSecretId</span></span>
<span data-ttu-id="96093-126">HANA 자격 증명을 포함 하는 키 보관소 비밀에 대 한 비밀 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="96093-126">Secret identifier to the Key Vault secret that contains the HANA credentials.</span></span>

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

### <span data-ttu-id="96093-127">-HanaDatabaseSqlPort</span><span class="sxs-lookup"><span data-stu-id="96093-127">-HanaDatabaseSqlPort</span></span>
<span data-ttu-id="96093-128">SAP HANA 인스턴스 데이터베이스의 SQL 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="96093-128">The SQL port of the database of SAP HANA instance.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: HanaDbSqlPort

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96093-129">-HanaDatabaseUsername</span><span class="sxs-lookup"><span data-stu-id="96093-129">-HanaDatabaseUsername</span></span>
<span data-ttu-id="96093-130">SAP HANA 인스턴스 데이터베이스의 사용자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="96093-130">The username of the database of SAP HANA instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HanaDbUsername

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96093-131">-HanaHostname</span><span class="sxs-lookup"><span data-stu-id="96093-131">-HanaHostname</span></span>
<span data-ttu-id="96093-132">SAP HANA 인스턴스의 호스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="96093-132">The hostname of SAP HANA instance.</span></span>

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

### <span data-ttu-id="96093-133">-Metadata</span><span class="sxs-lookup"><span data-stu-id="96093-133">-Metadata</span></span>
<span data-ttu-id="96093-134">공급자 인스턴스의 메타 데이터를 포함 하는 JSON 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="96093-134">A JSON string containing metadata of the provider instance.</span></span>

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

### <span data-ttu-id="96093-135">-이름</span><span class="sxs-lookup"><span data-stu-id="96093-135">-Name</span></span>
<span data-ttu-id="96093-136">공급자 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="96093-136">Name of the provider instance.</span></span>

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

### <span data-ttu-id="96093-137">-NoWait</span><span class="sxs-lookup"><span data-stu-id="96093-137">-NoWait</span></span>
<span data-ttu-id="96093-138">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="96093-138">Run the command asynchronously</span></span>

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

### <span data-ttu-id="96093-139">-ProviderType</span><span class="sxs-lookup"><span data-stu-id="96093-139">-ProviderType</span></span>
<span data-ttu-id="96093-140">공급자 인스턴스의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="96093-140">The type of provider instance.</span></span>
<span data-ttu-id="96093-141">지원 되는 값은 "SapHana"입니다.</span><span class="sxs-lookup"><span data-stu-id="96093-141">Supported values are: "SapHana".</span></span>

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

### <span data-ttu-id="96093-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96093-142">-ResourceGroupName</span></span>
<span data-ttu-id="96093-143">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="96093-143">Name of the resource group.</span></span>

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

### <span data-ttu-id="96093-144">-SapMonitorName</span><span class="sxs-lookup"><span data-stu-id="96093-144">-SapMonitorName</span></span>
<span data-ttu-id="96093-145">SAP 모니터 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="96093-145">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="96093-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="96093-146">-SubscriptionId</span></span>
<span data-ttu-id="96093-147">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="96093-147">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="96093-148">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="96093-148">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="96093-149">-확인</span><span class="sxs-lookup"><span data-stu-id="96093-149">-Confirm</span></span>
<span data-ttu-id="96093-150">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="96093-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96093-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96093-151">-WhatIf</span></span>
<span data-ttu-id="96093-152">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="96093-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96093-153">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="96093-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96093-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96093-154">CommonParameters</span></span>
<span data-ttu-id="96093-155">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="96093-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96093-156">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="96093-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96093-157">입력</span><span class="sxs-lookup"><span data-stu-id="96093-157">INPUTS</span></span>

## <span data-ttu-id="96093-158">출력</span><span class="sxs-lookup"><span data-stu-id="96093-158">OUTPUTS</span></span>

### <span data-ttu-id="96093-159">HanaOnAzure. Api20200207Preview. IProviderInstance에 대 한</span><span class="sxs-lookup"><span data-stu-id="96093-159">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.IProviderInstance</span></span>

## <span data-ttu-id="96093-160">상속자</span><span class="sxs-lookup"><span data-stu-id="96093-160">NOTES</span></span>

<span data-ttu-id="96093-161">별칭과</span><span class="sxs-lookup"><span data-stu-id="96093-161">ALIASES</span></span>

## <span data-ttu-id="96093-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="96093-162">RELATED LINKS</span></span>

