---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/update-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseWorkspace.md
ms.openlocfilehash: 60631b8d4c42ac314268453c5dedf16893281861
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995848"
---
# <span data-ttu-id="005dc-101">Update-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="005dc-101">Update-AzSynapseWorkspace</span></span>

## <span data-ttu-id="005dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="005dc-102">SYNOPSIS</span></span>
<span data-ttu-id="005dc-103">Synapse Analytics 작업 영역이 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="005dc-103">Updates a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="005dc-104">구문</span><span class="sxs-lookup"><span data-stu-id="005dc-104">SYNTAX</span></span>

### <span data-ttu-id="005dc-105">SetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="005dc-105">SetByNameParameterSet (Default)</span></span>
```
Update-AzSynapseWorkspace [-ResourceGroupName <String>] [-Name <String>] [-Tag <Hashtable>]
 [-SqlAdministratorLoginPassword <SecureString>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="005dc-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="005dc-106">SetByInputObjectParameterSet</span></span>
```
Update-AzSynapseWorkspace -InputObject <PSSynapseWorkspace> [-Tag <Hashtable>]
 [-SqlAdministratorLoginPassword <SecureString>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="005dc-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="005dc-107">SetByResourceIdParameterSet</span></span>
```
Update-AzSynapseWorkspace -ResourceId <String> [-Tag <Hashtable>]
 [-SqlAdministratorLoginPassword <SecureString>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="005dc-108">설명</span><span class="sxs-lookup"><span data-stu-id="005dc-108">DESCRIPTION</span></span>
<span data-ttu-id="005dc-109">**Update-AzSynapseWorkspace** cmdlet은 Azure Synapse Analytics 작업 영역이 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="005dc-109">The **Update-AzSynapseWorkspace** cmdlet updates an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="005dc-110">예제</span><span class="sxs-lookup"><span data-stu-id="005dc-110">EXAMPLES</span></span>

### <span data-ttu-id="005dc-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="005dc-111">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseWorkspace -Name ContosoWorkspace -Tag @{'key'='value'}
```

<span data-ttu-id="005dc-112">이 명령은 지정한 Azure Synapse Analytics 작업 영역의 태그를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="005dc-112">This commands updates tags for the specififed Azure Synapse Analytics workspace.</span></span>

### <span data-ttu-id="005dc-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="005dc-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseWorkspace -Tag @{'key'='value1'}
```

<span data-ttu-id="005dc-114">이 명령은 파이프라인을 통해 지정한 Azure Synapse Analytics 작업 영역의 태그를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="005dc-114">This commands updates tags for the specififed Azure Synapse Analytics workspace through pipeline.</span></span>

### <span data-ttu-id="005dc-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="005dc-115">Example 3</span></span>
```powershell
PS C:\> Update-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace -Tag @{'key'='value2'}
```

<span data-ttu-id="005dc-116">이 명령은 리소스 ID를 사용하여 파이프라인을 통해 지정된 Azure Synapse Analytics 작업 영역의 태그를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="005dc-116">This commands updates tags for the specififed Azure Synapse Analytics workspace through pipeline with resource ID.</span></span>

## <span data-ttu-id="005dc-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="005dc-117">PARAMETERS</span></span>

### <span data-ttu-id="005dc-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="005dc-118">-AsJob</span></span>
<span data-ttu-id="005dc-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="005dc-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="005dc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="005dc-120">-DefaultProfile</span></span>
<span data-ttu-id="005dc-121">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="005dc-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="005dc-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="005dc-122">-InputObject</span></span>
<span data-ttu-id="005dc-123">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="005dc-123">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="005dc-124">-Name</span><span class="sxs-lookup"><span data-stu-id="005dc-124">-Name</span></span>
<span data-ttu-id="005dc-125">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="005dc-125">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: WorkspaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="005dc-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="005dc-126">-ResourceGroupName</span></span>
<span data-ttu-id="005dc-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="005dc-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="005dc-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="005dc-128">-ResourceId</span></span>
<span data-ttu-id="005dc-129">Synapse 작업 영역의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="005dc-129">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="005dc-130">-SqlAdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="005dc-130">-SqlAdministratorLoginPassword</span></span>
<span data-ttu-id="005dc-131">작업 SQL 관리자 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="005dc-131">The new SQL administrator password for the workspace.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="005dc-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="005dc-132">-Tag</span></span>
<span data-ttu-id="005dc-133">문자열, 리소스와 연결된 태그의 문자열 사전입니다.</span><span class="sxs-lookup"><span data-stu-id="005dc-133">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="005dc-134">-확인</span><span class="sxs-lookup"><span data-stu-id="005dc-134">-Confirm</span></span>
<span data-ttu-id="005dc-135">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="005dc-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="005dc-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="005dc-136">-WhatIf</span></span>
<span data-ttu-id="005dc-137">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="005dc-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="005dc-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="005dc-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="005dc-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="005dc-139">CommonParameters</span></span>
<span data-ttu-id="005dc-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="005dc-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="005dc-141">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="005dc-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="005dc-142">입력</span><span class="sxs-lookup"><span data-stu-id="005dc-142">INPUTS</span></span>

### <span data-ttu-id="005dc-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="005dc-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="005dc-144">출력</span><span class="sxs-lookup"><span data-stu-id="005dc-144">OUTPUTS</span></span>

### <span data-ttu-id="005dc-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="005dc-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="005dc-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="005dc-146">NOTES</span></span>

## <span data-ttu-id="005dc-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="005dc-147">RELATED LINKS</span></span>
