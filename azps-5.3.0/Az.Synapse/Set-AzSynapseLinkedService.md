---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapselinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseLinkedService.md
ms.openlocfilehash: 635c1e064dbc081a5207f5c912c14166b2b01e17
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383223"
---
# <span data-ttu-id="7450d-101">Set-AzSynapseLinkedService</span><span class="sxs-lookup"><span data-stu-id="7450d-101">Set-AzSynapseLinkedService</span></span>

## <span data-ttu-id="7450d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7450d-102">SYNOPSIS</span></span>
<span data-ttu-id="7450d-103">데이터 저장소 또는 클라우드 서비스를 작업 영역으로 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="7450d-103">Links a data store or a cloud service to workspace.</span></span>

## <span data-ttu-id="7450d-104">구문</span><span class="sxs-lookup"><span data-stu-id="7450d-104">SYNTAX</span></span>

### <span data-ttu-id="7450d-105">SetByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="7450d-105">SetByName (Default)</span></span>
```
Set-AzSynapseLinkedService -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7450d-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="7450d-106">SetByObject</span></span>
```
Set-AzSynapseLinkedService -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7450d-107">설명</span><span class="sxs-lookup"><span data-stu-id="7450d-107">DESCRIPTION</span></span>
<span data-ttu-id="7450d-108">**Set-AzSynapseLinkedService** cmdlet은 데이터 저장소 또는 클라우드 서비스를 작업 영역으로 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="7450d-108">The **Set-AzSynapseLinkedService** cmdlet links a data store or a cloud service to workspace.</span></span>

## <span data-ttu-id="7450d-109">예제</span><span class="sxs-lookup"><span data-stu-id="7450d-109">EXAMPLES</span></span>

### <span data-ttu-id="7450d-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="7450d-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService -DefinitionFile "C:\\samples\\LinkedService.json"
```

<span data-ttu-id="7450d-111">이 명령은 ContosoWorkspace라는 작업 영역의 ContosoLinkedService라는 연결된 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7450d-111">This command creates a linked service named ContosoLinkedService in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="7450d-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="7450d-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapseLinkedService -Name ContosoLinkedService -DefinitionFile "C:\\samples\\LinkedService.json"
```

<span data-ttu-id="7450d-113">이 명령은 파이프라인을 통해 ContosoWorkspace라는 작업 영역의 ContosoLinkedService라는 연결된 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7450d-113">This command creates a linked service named ContosoLinkedService in the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="7450d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7450d-114">PARAMETERS</span></span>

### <span data-ttu-id="7450d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7450d-115">-AsJob</span></span>
<span data-ttu-id="7450d-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="7450d-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7450d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7450d-117">-DefaultProfile</span></span>
<span data-ttu-id="7450d-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7450d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7450d-119">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="7450d-119">-DefinitionFile</span></span>
<span data-ttu-id="7450d-120">JSON 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="7450d-120">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7450d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="7450d-121">-Name</span></span>
<span data-ttu-id="7450d-122">연결된 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7450d-122">The linked service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: LinkedServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7450d-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7450d-123">-WorkspaceName</span></span>
<span data-ttu-id="7450d-124">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7450d-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7450d-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="7450d-125">-WorkspaceObject</span></span>
<span data-ttu-id="7450d-126">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7450d-126">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7450d-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7450d-127">-Confirm</span></span>
<span data-ttu-id="7450d-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7450d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7450d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7450d-129">-WhatIf</span></span>
<span data-ttu-id="7450d-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="7450d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7450d-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7450d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7450d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7450d-132">CommonParameters</span></span>
<span data-ttu-id="7450d-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7450d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7450d-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7450d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7450d-135">입력</span><span class="sxs-lookup"><span data-stu-id="7450d-135">INPUTS</span></span>

### <span data-ttu-id="7450d-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="7450d-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="7450d-137">출력</span><span class="sxs-lookup"><span data-stu-id="7450d-137">OUTPUTS</span></span>

### <span data-ttu-id="7450d-138">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="7450d-138">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="7450d-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7450d-139">NOTES</span></span>

## <span data-ttu-id="7450d-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7450d-140">RELATED LINKS</span></span>
