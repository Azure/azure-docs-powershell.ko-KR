---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesqlpooladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 87c3f0e2e86f2867d659b26b5acc9df5a6dfe8c7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207565"
---
# <span data-ttu-id="6f501-101">Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="6f501-101">Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="6f501-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f501-102">SYNOPSIS</span></span>
<span data-ttu-id="6f501-103">보안 풀에서 고급 위협 방지 SQL 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="6f501-103">Sets a advanced threat protection settings on a SQL pool.</span></span>

## <span data-ttu-id="6f501-104">구문</span><span class="sxs-lookup"><span data-stu-id="6f501-104">SYNTAX</span></span>

### <span data-ttu-id="6f501-105">UpdateByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="6f501-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>]
 [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f501-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f501-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f501-107">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f501-107">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -InputObject <PSSynapseSqlPool>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f501-108">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f501-108">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -ResourceId <String>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f501-109">설명</span><span class="sxs-lookup"><span data-stu-id="6f501-109">DESCRIPTION</span></span>
<span data-ttu-id="6f501-110">**Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting** cmdlet은 Azure Synapse Analytics 풀에서 고급 위협 보호 설정을 SQL.</span><span class="sxs-lookup"><span data-stu-id="6f501-110">The **Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting** cmdlet sets a advanced threat protection settings on an Azure Synapse Analytics SQL pool.</span></span>
<span data-ttu-id="6f501-111">SQL 풀에서 고급 위협 방지를 사용하려면 해당 풀에서 감사 설정을 사용하도록 SQL 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f501-111">In order to enable advanced threat protection on a SQL pool an auditing settings must be enabled on that SQL pool.</span></span>

## <span data-ttu-id="6f501-112">예제</span><span class="sxs-lookup"><span data-stu-id="6f501-112">EXAMPLES</span></span>

### <span data-ttu-id="6f501-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="6f501-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="6f501-114">이 명령은 ContosoWorkspace라는 작업 영역 아래에 contosoSqlPool이라는 SQL 풀에 대한 고급 위협 보호 설정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6f501-114">This command sets the advanced threat protection settings for a SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="6f501-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6f501-115">PARAMETERS</span></span>

### <span data-ttu-id="6f501-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6f501-116">-AsJob</span></span>
<span data-ttu-id="6f501-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="6f501-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6f501-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f501-118">-DefaultProfile</span></span>
<span data-ttu-id="6f501-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6f501-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f501-120">-EmailAdmin</span><span class="sxs-lookup"><span data-stu-id="6f501-120">-EmailAdmin</span></span>
<span data-ttu-id="6f501-121">관리자에게 전자 메일로 보낼지 여부를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="6f501-121">Defines whether to email administrators.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: EmailAdmins

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f501-122">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="6f501-122">-ExcludedDetectionType</span></span>
<span data-ttu-id="6f501-123">제외할 검색 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="6f501-123">Detection types to exclude.</span></span>

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

### <span data-ttu-id="6f501-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6f501-124">-InputObject</span></span>
<span data-ttu-id="6f501-125">SQL 풀 입력 개체를 만듭니다. 일반적으로 파이프라인을 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="6f501-125">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f501-126">-Name</span><span class="sxs-lookup"><span data-stu-id="6f501-126">-Name</span></span>
<span data-ttu-id="6f501-127">Synapse SQL 풀입니다.</span><span class="sxs-lookup"><span data-stu-id="6f501-127">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f501-128">-NotificationRecipientsEmail</span><span class="sxs-lookup"><span data-stu-id="6f501-128">-NotificationRecipientsEmail</span></span>
<span data-ttu-id="6f501-129">경고를 보낼 세미코론으로 구분된 전자 메일 주소 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="6f501-129">A semicolon separated list of email addresses to send the alerts to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NotificationRecipientsEmails

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f501-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f501-130">-ResourceGroupName</span></span>
<span data-ttu-id="6f501-131">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f501-131">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f501-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6f501-132">-ResourceId</span></span>
<span data-ttu-id="6f501-133">Synapse SQL 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="6f501-133">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f501-134">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="6f501-134">-RetentionInDays</span></span>
<span data-ttu-id="6f501-135">감사 로그에 대한 보존 일 수입니다.</span><span class="sxs-lookup"><span data-stu-id="6f501-135">The number of retention days for the audit logs.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f501-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6f501-136">-StorageAccountName</span></span>
<span data-ttu-id="6f501-137">저장소 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f501-137">The name of the storage account.</span></span>

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

### <span data-ttu-id="6f501-138">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6f501-138">-WorkspaceName</span></span>
<span data-ttu-id="6f501-139">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f501-139">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f501-140">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="6f501-140">-WorkspaceObject</span></span>
<span data-ttu-id="6f501-141">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="6f501-141">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f501-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6f501-142">-Confirm</span></span>
<span data-ttu-id="6f501-143">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6f501-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f501-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f501-144">-WhatIf</span></span>
<span data-ttu-id="6f501-145">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="6f501-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f501-146">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6f501-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f501-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f501-147">CommonParameters</span></span>
<span data-ttu-id="6f501-148">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6f501-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f501-149">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6f501-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f501-150">입력</span><span class="sxs-lookup"><span data-stu-id="6f501-150">INPUTS</span></span>

### <span data-ttu-id="6f501-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="6f501-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="6f501-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="6f501-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="6f501-153">출력</span><span class="sxs-lookup"><span data-stu-id="6f501-153">OUTPUTS</span></span>

### <span data-ttu-id="6f501-154">Microsoft.Azure.Commands.Synapse.Models.PSSqlPoolSecurityAlertPolicy</span><span class="sxs-lookup"><span data-stu-id="6f501-154">Microsoft.Azure.Commands.Synapse.Models.PSSqlPoolSecurityAlertPolicy</span></span>

## <span data-ttu-id="6f501-155">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6f501-155">NOTES</span></span>

## <span data-ttu-id="6f501-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6f501-156">RELATED LINKS</span></span>
