---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/update-azsynapsesqlpooladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 2267f9420e545fd693b734aaf8f90e89cce000a4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994728"
---
# <span data-ttu-id="a60a0-101">Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="a60a0-101">Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="a60a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a60a0-102">SYNOPSIS</span></span>
<span data-ttu-id="a60a0-103">보안 풀에서 고급 위협 SQL 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a60a0-103">Sets a advanced threat protection settings on a SQL pool.</span></span>

## <span data-ttu-id="a60a0-104">구문</span><span class="sxs-lookup"><span data-stu-id="a60a0-104">SYNTAX</span></span>

### <span data-ttu-id="a60a0-105">UpdateByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="a60a0-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>]
 [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a60a0-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a60a0-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a60a0-107">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a60a0-107">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -InputObject <PSSynapseSqlPool>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a60a0-108">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a60a0-108">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -ResourceId <String>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a60a0-109">설명</span><span class="sxs-lookup"><span data-stu-id="a60a0-109">DESCRIPTION</span></span>
<span data-ttu-id="a60a0-110">**Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting** cmdlet은 Azure Synapse Analytics SQL 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a60a0-110">The **Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting** cmdlet sets a advanced threat protection settings on an Azure Synapse Analytics SQL pool.</span></span>
<span data-ttu-id="a60a0-111">풀에서 고급 위협 보호를 사용하도록 SQL 해당 풀에서 감사 설정을 사용하도록 SQL 합니다.</span><span class="sxs-lookup"><span data-stu-id="a60a0-111">In order to enable advanced threat protection on a SQL pool an auditing settings must be enabled on that SQL pool.</span></span>

## <span data-ttu-id="a60a0-112">예제</span><span class="sxs-lookup"><span data-stu-id="a60a0-112">EXAMPLES</span></span>

### <span data-ttu-id="a60a0-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="a60a0-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="a60a0-114">이 명령은 ContosoWorkspace라는 작업 SQL ContosoSqlPool이라는 풀에 대한 고급 위협 보호 설정을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a60a0-114">This command sets the advanced threat protection settings for a SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="a60a0-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a60a0-115">PARAMETERS</span></span>

### <span data-ttu-id="a60a0-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a60a0-116">-AsJob</span></span>
<span data-ttu-id="a60a0-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="a60a0-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a60a0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a60a0-118">-DefaultProfile</span></span>
<span data-ttu-id="a60a0-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a60a0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a60a0-120">-EmailAdmin</span><span class="sxs-lookup"><span data-stu-id="a60a0-120">-EmailAdmin</span></span>
<span data-ttu-id="a60a0-121">관리자에게 전자 메일로 보낼지 여부를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="a60a0-121">Defines whether to email administrators.</span></span>

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

### <span data-ttu-id="a60a0-122">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="a60a0-122">-ExcludedDetectionType</span></span>
<span data-ttu-id="a60a0-123">제외할 검색 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="a60a0-123">Detection types to exclude.</span></span>

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

### <span data-ttu-id="a60a0-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a60a0-124">-InputObject</span></span>
<span data-ttu-id="a60a0-125">SQL 입력 개체를 입력합니다. 일반적으로 파이프라인을 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="a60a0-125">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a60a0-126">-Name</span><span class="sxs-lookup"><span data-stu-id="a60a0-126">-Name</span></span>
<span data-ttu-id="a60a0-127">Synapse SQL 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a60a0-127">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="a60a0-128">-NotificationRecipientsEmail</span><span class="sxs-lookup"><span data-stu-id="a60a0-128">-NotificationRecipientsEmail</span></span>
<span data-ttu-id="a60a0-129">경고를 보낼 세미코론으로 구분된 전자 메일 주소 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="a60a0-129">A semicolon separated list of email addresses to send the alerts to.</span></span>

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

### <span data-ttu-id="a60a0-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a60a0-130">-ResourceGroupName</span></span>
<span data-ttu-id="a60a0-131">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a60a0-131">Resource group name.</span></span>

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

### <span data-ttu-id="a60a0-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a60a0-132">-ResourceId</span></span>
<span data-ttu-id="a60a0-133">Synapse SQL 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="a60a0-133">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="a60a0-134">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="a60a0-134">-RetentionInDays</span></span>
<span data-ttu-id="a60a0-135">감사 로그에 대한 보존 일 수입니다.</span><span class="sxs-lookup"><span data-stu-id="a60a0-135">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="a60a0-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a60a0-136">-StorageAccountName</span></span>
<span data-ttu-id="a60a0-137">저장소 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a60a0-137">The name of the storage account.</span></span>

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

### <span data-ttu-id="a60a0-138">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a60a0-138">-WorkspaceName</span></span>
<span data-ttu-id="a60a0-139">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a60a0-139">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a60a0-140">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a60a0-140">-WorkspaceObject</span></span>
<span data-ttu-id="a60a0-141">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a60a0-141">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a60a0-142">-확인</span><span class="sxs-lookup"><span data-stu-id="a60a0-142">-Confirm</span></span>
<span data-ttu-id="a60a0-143">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a60a0-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a60a0-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a60a0-144">-WhatIf</span></span>
<span data-ttu-id="a60a0-145">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="a60a0-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a60a0-146">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a60a0-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a60a0-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a60a0-147">CommonParameters</span></span>
<span data-ttu-id="a60a0-148">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a60a0-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a60a0-149">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a60a0-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a60a0-150">입력</span><span class="sxs-lookup"><span data-stu-id="a60a0-150">INPUTS</span></span>

### <span data-ttu-id="a60a0-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a60a0-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="a60a0-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="a60a0-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="a60a0-153">출력</span><span class="sxs-lookup"><span data-stu-id="a60a0-153">OUTPUTS</span></span>

### <span data-ttu-id="a60a0-154">Microsoft.Azure.Commands.Synapse.Models.PSSqlPoolSecurityAlertPolicy</span><span class="sxs-lookup"><span data-stu-id="a60a0-154">Microsoft.Azure.Commands.Synapse.Models.PSSqlPoolSecurityAlertPolicy</span></span>

## <span data-ttu-id="a60a0-155">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a60a0-155">NOTES</span></span>

## <span data-ttu-id="a60a0-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a60a0-156">RELATED LINKS</span></span>
