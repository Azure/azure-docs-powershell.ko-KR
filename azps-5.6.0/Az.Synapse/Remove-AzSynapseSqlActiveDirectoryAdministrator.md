---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsesqlactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlActiveDirectoryAdministrator.md
ms.openlocfilehash: 88e65b1c38f7550e5e7f90aa436fd510e203acf4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999180"
---
# <span data-ttu-id="59b91-101">Remove-AzSynapseSqlActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="59b91-101">Remove-AzSynapseSqlActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="59b91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59b91-102">SYNOPSIS</span></span>
<span data-ttu-id="59b91-103">Synapse Analytics 작업 영역의 Azure AD 관리자를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="59b91-103">Removes an Azure AD administrator for Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="59b91-104">구문</span><span class="sxs-lookup"><span data-stu-id="59b91-104">SYNTAX</span></span>

### <span data-ttu-id="59b91-105">RemoveByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="59b91-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlActiveDirectoryAdministrator [-ResourceGroupName <String>] -WorkspaceName <String>
 [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="59b91-106">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="59b91-106">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlActiveDirectoryAdministrator -InputObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59b91-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="59b91-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlActiveDirectoryAdministrator -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59b91-108">설명</span><span class="sxs-lookup"><span data-stu-id="59b91-108">DESCRIPTION</span></span>
<span data-ttu-id="59b91-109">**Remove-AzSynapseSqlActiveDirectoryAdministrator** cmdlet은 Azure Synapse Analytics 작업 영역의 Azure AD(Azure Active Directory) 관리자를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="59b91-109">The **Remove-AzSynapseSqlActiveDirectoryAdministrator** cmdlet removes an Azure Active Directory (Azure AD) administrator for Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="59b91-110">예제</span><span class="sxs-lookup"><span data-stu-id="59b91-110">EXAMPLES</span></span>

### <span data-ttu-id="59b91-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="59b91-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlActiveDirectoryAdministrator -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="59b91-112">이 명령은 ContosoWorkspace라는 작업 영역의 Azure AD 관리자를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="59b91-112">This command removes the Azure AD administrator for the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="59b91-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="59b91-113">PARAMETERS</span></span>

### <span data-ttu-id="59b91-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="59b91-114">-AsJob</span></span>
<span data-ttu-id="59b91-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="59b91-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="59b91-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59b91-116">-DefaultProfile</span></span>
<span data-ttu-id="59b91-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="59b91-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59b91-118">-Force</span><span class="sxs-lookup"><span data-stu-id="59b91-118">-Force</span></span>
<span data-ttu-id="59b91-119">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="59b91-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="59b91-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59b91-120">-InputObject</span></span>
<span data-ttu-id="59b91-121">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="59b91-121">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59b91-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="59b91-122">-PassThru</span></span>
<span data-ttu-id="59b91-123">이 Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="59b91-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="59b91-124">이 스위치가 지정되어 있는 경우 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="59b91-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="59b91-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59b91-125">-ResourceGroupName</span></span>
<span data-ttu-id="59b91-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59b91-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59b91-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="59b91-127">-ResourceId</span></span>
<span data-ttu-id="59b91-128">Synapse 작업 영역의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="59b91-128">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59b91-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="59b91-129">-WorkspaceName</span></span>
<span data-ttu-id="59b91-130">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59b91-130">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59b91-131">-확인</span><span class="sxs-lookup"><span data-stu-id="59b91-131">-Confirm</span></span>
<span data-ttu-id="59b91-132">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="59b91-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59b91-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59b91-133">-WhatIf</span></span>
<span data-ttu-id="59b91-134">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="59b91-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59b91-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="59b91-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59b91-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59b91-136">CommonParameters</span></span>
<span data-ttu-id="59b91-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="59b91-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59b91-138">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="59b91-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59b91-139">입력</span><span class="sxs-lookup"><span data-stu-id="59b91-139">INPUTS</span></span>

### <span data-ttu-id="59b91-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="59b91-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="59b91-141">출력</span><span class="sxs-lookup"><span data-stu-id="59b91-141">OUTPUTS</span></span>

### <span data-ttu-id="59b91-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="59b91-142">System.Boolean</span></span>

## <span data-ttu-id="59b91-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="59b91-143">NOTES</span></span>

## <span data-ttu-id="59b91-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="59b91-144">RELATED LINKS</span></span>
