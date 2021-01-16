---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesqladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 4fb27d1d822d72de9564e9acc900122016940c6d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375845"
---
# <span data-ttu-id="089d5-101">Update-AzSynapseSqlAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="089d5-101">Update-AzSynapseSqlAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="089d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="089d5-102">SYNOPSIS</span></span>
<span data-ttu-id="089d5-103">작업 영역의 고급 위협 방지 설정을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="089d5-103">Updates an advanced threat protection settings on a workspace.</span></span>

## <span data-ttu-id="089d5-104">구문</span><span class="sxs-lookup"><span data-stu-id="089d5-104">SYNTAX</span></span>

### <span data-ttu-id="089d5-105">UpdateByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="089d5-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="089d5-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="089d5-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlAdvancedThreatProtectionSetting -InputObject <PSSynapseWorkspace>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="089d5-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="089d5-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlAdvancedThreatProtectionSetting -ResourceId <String> [-NotificationRecipientsEmail <String>]
 [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="089d5-108">설명</span><span class="sxs-lookup"><span data-stu-id="089d5-108">DESCRIPTION</span></span>
<span data-ttu-id="089d5-109">**Update-AzSynapseSqlAdvancedThreatProtectionSetting** cmdlet은 Azure Synapse 분석 작업 영역의 고급 위협 보호 설정을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="089d5-109">The **Update-AzSynapseSqlAdvancedThreatProtectionSetting** cmdlet updates an advanced threat protection settings on an Azure Synapse Analytics Workspace.</span></span> <span data-ttu-id="089d5-110">작업 영역의 고급 위협 방지를 사용하려면 해당 작업 영역의 감사 설정을 사용하도록 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="089d5-110">In order to enable advanced threat protection on a workspace an auditing settings must be enabled on that workspace.</span></span>

## <span data-ttu-id="089d5-111">예제</span><span class="sxs-lookup"><span data-stu-id="089d5-111">EXAMPLES</span></span>

### <span data-ttu-id="089d5-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="089d5-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace -NotificationRecipientsEmail "admin01@contoso.com;secadmin@contoso.com" -EmailAdmin $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="089d5-113">이 명령은 ContosoWorkspace라는 작업 영역의 고급 위협 보호 설정을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="089d5-113">This command updates the advanced threat protection settings for a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="089d5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="089d5-114">PARAMETERS</span></span>

### <span data-ttu-id="089d5-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="089d5-115">-AsJob</span></span>
<span data-ttu-id="089d5-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="089d5-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="089d5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="089d5-117">-DefaultProfile</span></span>
<span data-ttu-id="089d5-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="089d5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="089d5-119">-EmailAdmin</span><span class="sxs-lookup"><span data-stu-id="089d5-119">-EmailAdmin</span></span>
<span data-ttu-id="089d5-120">관리자에게 전자 메일로 보낼지 여부를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="089d5-120">Defines whether to email administrators.</span></span>

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

### <span data-ttu-id="089d5-121">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="089d5-121">-ExcludedDetectionType</span></span>
<span data-ttu-id="089d5-122">제외할 검색 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="089d5-122">Detection types to exclude.</span></span>

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

### <span data-ttu-id="089d5-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="089d5-123">-InputObject</span></span>
<span data-ttu-id="089d5-124">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="089d5-124">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="089d5-125">-NotificationRecipientsEmail</span><span class="sxs-lookup"><span data-stu-id="089d5-125">-NotificationRecipientsEmail</span></span>
<span data-ttu-id="089d5-126">경고를 보낼 세미코론으로 구분된 전자 메일 주소 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="089d5-126">A semicolon separated list of email addresses to send the alerts to.</span></span>

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

### <span data-ttu-id="089d5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="089d5-127">-ResourceGroupName</span></span>
<span data-ttu-id="089d5-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="089d5-128">Resource group name.</span></span>

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

### <span data-ttu-id="089d5-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="089d5-129">-ResourceId</span></span>
<span data-ttu-id="089d5-130">Synapse 작업 영역의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="089d5-130">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="089d5-131">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="089d5-131">-RetentionInDays</span></span>
<span data-ttu-id="089d5-132">감사 로그에 대한 보존 일 수입니다.</span><span class="sxs-lookup"><span data-stu-id="089d5-132">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="089d5-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="089d5-133">-StorageAccountName</span></span>
<span data-ttu-id="089d5-134">저장소 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="089d5-134">The name of the storage account.</span></span>

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

### <span data-ttu-id="089d5-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="089d5-135">-WorkspaceName</span></span>
<span data-ttu-id="089d5-136">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="089d5-136">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="089d5-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="089d5-137">-Confirm</span></span>
<span data-ttu-id="089d5-138">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="089d5-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="089d5-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="089d5-139">-WhatIf</span></span>
<span data-ttu-id="089d5-140">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="089d5-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="089d5-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="089d5-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="089d5-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="089d5-142">CommonParameters</span></span>
<span data-ttu-id="089d5-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="089d5-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="089d5-144">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="089d5-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="089d5-145">입력</span><span class="sxs-lookup"><span data-stu-id="089d5-145">INPUTS</span></span>

### <span data-ttu-id="089d5-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="089d5-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="089d5-147">출력</span><span class="sxs-lookup"><span data-stu-id="089d5-147">OUTPUTS</span></span>

### <span data-ttu-id="089d5-148">Microsoft.Azure.Commands.Synapse.Models.PSServerSecurityAlertPolicy</span><span class="sxs-lookup"><span data-stu-id="089d5-148">Microsoft.Azure.Commands.Synapse.Models.PSServerSecurityAlertPolicy</span></span>

## <span data-ttu-id="089d5-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="089d5-149">NOTES</span></span>

## <span data-ttu-id="089d5-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="089d5-150">RELATED LINKS</span></span>
