---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratediscoveredserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateDiscoveredServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateDiscoveredServer.md
ms.openlocfilehash: 367d22f4cea200b59b63e3ddb39c1eaad749fc43
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185113"
---
# <span data-ttu-id="64a15-101">Get-AzMigrateDiscoveredServer</span><span class="sxs-lookup"><span data-stu-id="64a15-101">Get-AzMigrateDiscoveredServer</span></span>

## <span data-ttu-id="64a15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64a15-102">SYNOPSIS</span></span>
<span data-ttu-id="64a15-103">마이그레이션 프로젝트에서 검색된 모든 서버를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="64a15-103">Get All discovered servers in a migrate project.</span></span>

## <span data-ttu-id="64a15-104">구문</span><span class="sxs-lookup"><span data-stu-id="64a15-104">SYNTAX</span></span>

### <span data-ttu-id="64a15-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="64a15-105">List (Default)</span></span>
```
Get-AzMigrateDiscoveredServer -ProjectName <String> -ResourceGroupName <String> [-DisplayName <String>]
 [-SubscriptionId <String[]>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="64a15-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="64a15-106">Get</span></span>
```
Get-AzMigrateDiscoveredServer -Name <String> -ProjectName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="64a15-107">GetInSite</span><span class="sxs-lookup"><span data-stu-id="64a15-107">GetInSite</span></span>
```
Get-AzMigrateDiscoveredServer -ApplianceName <String> -Name <String> -ProjectName <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="64a15-108">ListInSite</span><span class="sxs-lookup"><span data-stu-id="64a15-108">ListInSite</span></span>
```
Get-AzMigrateDiscoveredServer -ApplianceName <String> -ProjectName <String> -ResourceGroupName <String>
 [-DisplayName <String>] [-SubscriptionId <String[]>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="64a15-109">설명</span><span class="sxs-lookup"><span data-stu-id="64a15-109">DESCRIPTION</span></span>
<span data-ttu-id="64a15-110">Azure Migrate 서버 commandlet을 사용하여 마이그레이션 프로젝트의 모든 서버를 페치합니다.</span><span class="sxs-lookup"><span data-stu-id="64a15-110">Get Azure migrate server commandlet fetches all servers in a migrate project.</span></span>

## <span data-ttu-id="64a15-111">예제</span><span class="sxs-lookup"><span data-stu-id="64a15-111">EXAMPLES</span></span>

### <span data-ttu-id="64a15-112">예제 1: 목록</span><span class="sxs-lookup"><span data-stu-id="64a15-112">Example 1: List</span></span>
```powershell
PS C:\> Get-AzMigrateDiscoveredServer -SubscriptionId xxx-xxx-xxx -ResourceGroupName julytest -ProjectName julytest

Name                                                                                                      Typeo…
----                                                                                                      ----o…
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029e62c-31d2-a6c3-5316-aa39f47c49fc Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029c180-1359-5e3c-3f56-05632aa4a37f Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029d80d-d014-72f3-8d05-d43ee49a023d Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029bd24-6d40-88dc-4f29-329596f9a50b Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_50292d97-2025-bfdf-1f07-86afa50d144f Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_50293685-fb73-0a89-204f-f79cb1f0061e Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029c9aa-3c8c-aba8-834e-1058bc457e5b Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029dabc-cc94-780f-76fd-e39acb0e9dce Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_50299579-fc18-4152-ade2-c4a57946f72b Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029cc18-efdc-7315-3b09-9d12a0f337e2 Microsoft.OffAzure/VMwareSites/machines

```

<span data-ttu-id="64a15-113">마이그레이션 프로젝트의 모든 서버를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="64a15-113">Get All servers in a migrate project.</span></span>

### <span data-ttu-id="64a15-114">예제 2: Get</span><span class="sxs-lookup"><span data-stu-id="64a15-114">Example 2: Get</span></span>
```powershell
PS C:\> Get-AzMigrateDiscoveredServer -Name idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029e62c-31d2-a6c3-5316-aa39f47c49fc -SubscriptionId xxx-xxx-xxx -ResourceGroupName julytest -ProjectName julytest

Name                                                                                                      Typeo…
----                                                                                                      ----o…
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029e62c-31d2-a6c3-5316-aa39f47c49fc Microsoft.OffAzure/VMwareSites/machines

```

<span data-ttu-id="64a15-115">이름으로 마이그레이션 프로젝트의 서버를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="64a15-115">Get a server in a migrate project by name.</span></span>
<span data-ttu-id="64a15-116">이름은 서버에 대한 고유한 파라메더입니다.</span><span class="sxs-lookup"><span data-stu-id="64a15-116">Name is a unique paramenter for a server.</span></span>

### <span data-ttu-id="64a15-117">예제 3: 어플라이언스에 나열</span><span class="sxs-lookup"><span data-stu-id="64a15-117">Example 3: List in an appliance</span></span>
```powershell
PS C:\> Get-AzMigrateDiscoveredServer  -ApplianceName BBVMwareAVS -SubscriptionId xxx-xxx-xxx -ResourceGroupName julytest -ProjectName julytest

Name                                                                                                      Typeo…
----                                                                                                      ----o…
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029e62c-31d2-a6c3-5316-aa39f47c49fc Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029c180-1359-5e3c-3f56-05632aa4a37f Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029d80d-d014-72f3-8d05-d43ee49a023d Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029bd24-6d40-88dc-4f29-329596f9a50b Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_50292d97-2025-bfdf-1f07-86afa50d144f Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_50293685-fb73-0a89-204f-f79cb1f0061e Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029c9aa-3c8c-aba8-834e-1058bc457e5b Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029dabc-cc94-780f-76fd-e39acb0e9dce Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_50299579-fc18-4152-ade2-c4a57946f72b Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029cc18-efdc-7315-3b09-9d12a0f337e2 Microsoft.OffAzure/VMwareSites/machines

```

<span data-ttu-id="64a15-118">프로젝트의 어플라이언스에 대한 모든 서버를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="64a15-118">List all servers for an appliance in a project.</span></span>

### <span data-ttu-id="64a15-119">예제 4: 어플라이언스에 추가</span><span class="sxs-lookup"><span data-stu-id="64a15-119">Example 4: Get in an appliance</span></span>
```powershell
PS C:\> Get-AzMigrateDiscoveredServer -Name idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029e62c-31d2-a6c3-5316-aa39f47c49fc -ApplianceName BBVMwareAVS -SubscriptionId xxx-xxx-xxx -ResourceGroupName julytest -ProjectName julytest

Name                                                                                                      Typeo…
----                                                                                                      ----o…
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029e62c-31d2-a6c3-5316-aa39f47c49fc Microsoft.OffAzure/VMwareSites/machines

```

<span data-ttu-id="64a15-120">프로젝트에서 어플라이언스에 대한 서버를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="64a15-120">Get a server for an appliance in a project.</span></span>
<span data-ttu-id="64a15-121">이름은 서버에 대한 고유한 파라메더입니다.</span><span class="sxs-lookup"><span data-stu-id="64a15-121">Name is a unique paramenter for a server.</span></span>

### <span data-ttu-id="64a15-122">예제 5: 표시 이름으로 나열 및 필터링</span><span class="sxs-lookup"><span data-stu-id="64a15-122">Example 5: List and filter by display name</span></span>
```powershell
PS C:\> Get-AzMigrateDiscoveredServer  -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -ProjectName BugBashAVSVMware -DisplayName Contoso | Format-Table DisplayName,Name,Type

DisplayName                   Name                                                                                  Type
-----------                   ----                                                                                  ----
Contoso-ConfigurationServer   10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50098b08-5701-4c58-f6ad-1daf127a8ed9 Microsoft.OffAzure/VMwareSites/machines
Contoso-FrontTier1            10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_5009c31a-241a-8213-5627-4ea4af00df93 Microsoft.OffAzure/VMwareSites/machines
Contoso-MiddleTier1           10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50097bb8-f32c-39d6-f475-5aaa6194f016 Microsoft.OffAzure/VMwareSites/machines
ContosoAppSrv2                10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_5009b455-1721-fa03-7ceb-8177cd2c5de6 Microsoft.OffAzure/VMwareSites/machines
ContosoCSASR                  10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50096b80-7061-672c-8db0-07ee41212869 Microsoft.OffAzure/VMwareSites/machines
ContosoVMwareMigration2       10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50099d31-71d5-2bd1-fada-8c4eba2f279a Microsoft.OffAzure/VMwareSites/machines
ContosoAppSrv1                10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50097d3f-c1f6-9217-825c-936db54043df Microsoft.OffAzure/VMwareSites/machines

```

<span data-ttu-id="64a15-123">마이그레이션 프로젝트의 서버를 나열하고 표시 이름으로 응답을 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="64a15-123">List servers in a migrate project and filter responses with display name.</span></span>

### <span data-ttu-id="64a15-124">예제 6: 어플라이언스에 나열 및 표시 이름으로 필터링</span><span class="sxs-lookup"><span data-stu-id="64a15-124">Example 6: List in an appliance and filter by display name</span></span>
```powershell
PS C:\> PS /src/Migrate [Az.Migrate]> Get-AzMigrateDiscoveredServer  -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -ProjectName BugBashAVSVMware -ApplianceName BBVMwareAVS -DisplayName Contoso | Format-Table DisplayName,Name,Type

DisplayName                   Name                                                                                  Type
-----------                   ----                                                                                  ----
Contoso-ConfigurationServer   10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50098b08-5701-4c58-f6ad-1daf127a8ed9 Microsoft.OffAzure/VMwareSites/machines
Contoso-FrontTier1            10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_5009c31a-241a-8213-5627-4ea4af00df93 Microsoft.OffAzure/VMwareSites/machines
Contoso-MiddleTier1           10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50097bb8-f32c-39d6-f475-5aaa6194f016 Microsoft.OffAzure/VMwareSites/machines
ContosoAppSrv2                10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_5009b455-1721-fa03-7ceb-8177cd2c5de6 Microsoft.OffAzure/VMwareSites/machines
ContosoCSASR                  10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50096b80-7061-672c-8db0-07ee41212869 Microsoft.OffAzure/VMwareSites/machines
ContosoVMwareMigration2       10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50099d31-71d5-2bd1-fada-8c4eba2f279a Microsoft.OffAzure/VMwareSites/machines
ContosoAppSrv1                10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50097d3f-c1f6-9217-825c-936db54043df Microsoft.OffAzure/VMwareSites/machines
Contoso-DataTier3             10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_500986e5-7720-471e-11d7-d4e8ae9edc45 Microsoft.OffAzure/VMwareSites/machines
```

<span data-ttu-id="64a15-125">마이그레이션 프로젝트에서 어플라이언스에 대한 서버를 나열하고 표시 이름으로 응답을 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="64a15-125">List servers for an appliance in a migrate project and filter responses with display name.</span></span>

## <span data-ttu-id="64a15-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="64a15-126">PARAMETERS</span></span>

### <span data-ttu-id="64a15-127">-ApplianceName</span><span class="sxs-lookup"><span data-stu-id="64a15-127">-ApplianceName</span></span>
<span data-ttu-id="64a15-128">어플라이언스 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="64a15-128">Specifies the appliance name.</span></span>
<span data-ttu-id="64a15-129">내부적으로 사이트에 매핑됩니다.</span><span class="sxs-lookup"><span data-stu-id="64a15-129">This internally maps to a site.</span></span>

```yaml
Type: System.String
Parameter Sets: GetInSite, ListInSite
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64a15-130">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="64a15-130">-DisplayName</span></span>
<span data-ttu-id="64a15-131">VMware 컴퓨터 표시 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="64a15-131">Specifies the VMware machine display name.</span></span>

```yaml
Type: System.String
Parameter Sets: List, ListInSite
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64a15-132">-Name</span><span class="sxs-lookup"><span data-stu-id="64a15-132">-Name</span></span>
<span data-ttu-id="64a15-133">VMware 컴퓨터 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="64a15-133">Specifies the VMware machine name.</span></span>
<span data-ttu-id="64a15-134">내부 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="64a15-134">This is an internal Name.</span></span>
<span data-ttu-id="64a15-135">사용자의 경우 표시 이름을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="64a15-135">For users, use display name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, GetInSite
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64a15-136">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="64a15-136">-ProjectName</span></span>
<span data-ttu-id="64a15-137">마이그레이션 프로젝트 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="64a15-137">Specifies the migrate project name.</span></span>

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

### <span data-ttu-id="64a15-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64a15-138">-ResourceGroupName</span></span>
<span data-ttu-id="64a15-139">리소스 그룹 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="64a15-139">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="64a15-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="64a15-140">-SubscriptionId</span></span>
<span data-ttu-id="64a15-141">구독 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="64a15-141">Specifies the subscription id.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64a15-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="64a15-142">-Confirm</span></span>
<span data-ttu-id="64a15-143">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="64a15-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64a15-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64a15-144">-WhatIf</span></span>
<span data-ttu-id="64a15-145">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="64a15-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64a15-146">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="64a15-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64a15-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64a15-147">CommonParameters</span></span>
<span data-ttu-id="64a15-148">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="64a15-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64a15-149">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="64a15-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64a15-150">입력</span><span class="sxs-lookup"><span data-stu-id="64a15-150">INPUTS</span></span>

## <span data-ttu-id="64a15-151">출력</span><span class="sxs-lookup"><span data-stu-id="64a15-151">OUTPUTS</span></span>

### <span data-ttu-id="64a15-152">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareMachine</span><span class="sxs-lookup"><span data-stu-id="64a15-152">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareMachine</span></span>

## <span data-ttu-id="64a15-153">참고 사항</span><span class="sxs-lookup"><span data-stu-id="64a15-153">NOTES</span></span>

<span data-ttu-id="64a15-154">별칭</span><span class="sxs-lookup"><span data-stu-id="64a15-154">ALIASES</span></span>

## <span data-ttu-id="64a15-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="64a15-155">RELATED LINKS</span></span>

