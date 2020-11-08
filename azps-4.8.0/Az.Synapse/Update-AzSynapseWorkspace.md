---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseWorkspace.md
ms.openlocfilehash: 84180165e835678dc74a7ed08f6a06c51cec8134
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056054"
---
# <span data-ttu-id="cf06f-101">Update-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="cf06f-101">Update-AzSynapseWorkspace</span></span>

## <span data-ttu-id="cf06f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf06f-102">SYNOPSIS</span></span>
<span data-ttu-id="cf06f-103">Synapse Analytics 작업 영역을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf06f-103">Updates a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="cf06f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cf06f-104">SYNTAX</span></span>

### <span data-ttu-id="cf06f-105">SetByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="cf06f-105">SetByNameParameterSet (Default)</span></span>
```
Update-AzSynapseWorkspace [-ResourceGroupName <String>] [-Name <String>] [-Tag <Hashtable>]
 [-SqlAdministratorLoginPassword <SecureString>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf06f-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf06f-106">SetByInputObjectParameterSet</span></span>
```
Update-AzSynapseWorkspace -InputObject <PSSynapseWorkspace> [-Tag <Hashtable>]
 [-SqlAdministratorLoginPassword <SecureString>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf06f-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf06f-107">SetByResourceIdParameterSet</span></span>
```
Update-AzSynapseWorkspace -ResourceId <String> [-Tag <Hashtable>]
 [-SqlAdministratorLoginPassword <SecureString>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf06f-108">설명은</span><span class="sxs-lookup"><span data-stu-id="cf06f-108">DESCRIPTION</span></span>
<span data-ttu-id="cf06f-109">**업데이트 AzSynapseWorkspace** Cmdlet은 Azure Synapse Analytics 작업 영역을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf06f-109">The **Update-AzSynapseWorkspace** cmdlet updates an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="cf06f-110">예제의</span><span class="sxs-lookup"><span data-stu-id="cf06f-110">EXAMPLES</span></span>

### <span data-ttu-id="cf06f-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="cf06f-111">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseWorkspace -Name ContosoWorkspace -Tag @{'key'='value'}
```

<span data-ttu-id="cf06f-112">이 명령은 specififed Azure Synapse Analytics 작업 영역의 태그를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf06f-112">This commands updates tags for the specififed Azure Synapse Analytics workspace.</span></span>

### <span data-ttu-id="cf06f-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="cf06f-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseWorkspace -Tag @{'key'='value1'}
```

<span data-ttu-id="cf06f-114">이 명령은 파이프라인을 통해 specififed Azure Synapse Analytics 작업 영역에 대 한 태그를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf06f-114">This commands updates tags for the specififed Azure Synapse Analytics workspace through pipeline.</span></span>

### <span data-ttu-id="cf06f-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="cf06f-115">Example 3</span></span>
```powershell
PS C:\> Update-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace -Tag @{'key'='value2'}
```

<span data-ttu-id="cf06f-116">이 명령은 리소스 ID가 있는 파이프라인을 통해 specififed Azure Synapse Analytics 작업 영역의 태그를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf06f-116">This commands updates tags for the specififed Azure Synapse Analytics workspace through pipeline with resource ID.</span></span>

## <span data-ttu-id="cf06f-117">변수</span><span class="sxs-lookup"><span data-stu-id="cf06f-117">PARAMETERS</span></span>

### <span data-ttu-id="cf06f-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cf06f-118">-AsJob</span></span>
<span data-ttu-id="cf06f-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="cf06f-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cf06f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf06f-120">-DefaultProfile</span></span>
<span data-ttu-id="cf06f-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cf06f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf06f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf06f-122">-InputObject</span></span>
<span data-ttu-id="cf06f-123">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="cf06f-123">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="cf06f-124">-이름</span><span class="sxs-lookup"><span data-stu-id="cf06f-124">-Name</span></span>
<span data-ttu-id="cf06f-125">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cf06f-125">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="cf06f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf06f-126">-ResourceGroupName</span></span>
<span data-ttu-id="cf06f-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cf06f-127">Resource group name.</span></span>

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

### <span data-ttu-id="cf06f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf06f-128">-ResourceId</span></span>
<span data-ttu-id="cf06f-129">Synapse workspace의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="cf06f-129">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="cf06f-130">-SqlAdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="cf06f-130">-SqlAdministratorLoginPassword</span></span>
<span data-ttu-id="cf06f-131">작업 영역에 대 한 새 SQL 관리자 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="cf06f-131">The new SQL administrator password for the workspace.</span></span>

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

### <span data-ttu-id="cf06f-132">태그</span><span class="sxs-lookup"><span data-stu-id="cf06f-132">-Tag</span></span>
<span data-ttu-id="cf06f-133">리소스와 연결 된 태그의 문자열 사전입니다.</span><span class="sxs-lookup"><span data-stu-id="cf06f-133">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="cf06f-134">-확인</span><span class="sxs-lookup"><span data-stu-id="cf06f-134">-Confirm</span></span>
<span data-ttu-id="cf06f-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf06f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf06f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf06f-136">-WhatIf</span></span>
<span data-ttu-id="cf06f-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cf06f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf06f-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cf06f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf06f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf06f-139">CommonParameters</span></span>
<span data-ttu-id="cf06f-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf06f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf06f-141">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cf06f-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf06f-142">입력</span><span class="sxs-lookup"><span data-stu-id="cf06f-142">INPUTS</span></span>

### <span data-ttu-id="cf06f-143">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="cf06f-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="cf06f-144">출력</span><span class="sxs-lookup"><span data-stu-id="cf06f-144">OUTPUTS</span></span>

### <span data-ttu-id="cf06f-145">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="cf06f-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="cf06f-146">상속자</span><span class="sxs-lookup"><span data-stu-id="cf06f-146">NOTES</span></span>

## <span data-ttu-id="cf06f-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cf06f-147">RELATED LINKS</span></span>
