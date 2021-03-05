---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapselinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseLinkedService.md
ms.openlocfilehash: 61ddc7c6a71dcc5545b8bdc2751e619d7da8e3bd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967216"
---
# <span data-ttu-id="ac0f5-101">Get-AzSynapseLinkedService</span><span class="sxs-lookup"><span data-stu-id="ac0f5-101">Get-AzSynapseLinkedService</span></span>

## <span data-ttu-id="ac0f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac0f5-102">SYNOPSIS</span></span>
<span data-ttu-id="ac0f5-103">작업 영역의 연결된 서비스에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ac0f5-103">Gets information about linked services in workspace.</span></span>

## <span data-ttu-id="ac0f5-104">구문</span><span class="sxs-lookup"><span data-stu-id="ac0f5-104">SYNTAX</span></span>

### <span data-ttu-id="ac0f5-105">GetByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="ac0f5-105">GetByName (Default)</span></span>
```
Get-AzSynapseLinkedService -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ac0f5-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="ac0f5-106">GetByObject</span></span>
```
Get-AzSynapseLinkedService -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac0f5-107">설명</span><span class="sxs-lookup"><span data-stu-id="ac0f5-107">DESCRIPTION</span></span>
<span data-ttu-id="ac0f5-108">**Get-AzSynapseLinkedService** cmdlet은 작업 영역의 연결된 서비스에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ac0f5-108">The **Get-AzSynapseLinkedService** cmdlet gets information about linked services in workspace.</span></span>
<span data-ttu-id="ac0f5-109">연결된 서비스의 이름을 지정하는 경우 이 cmdlet은 연결된 서비스에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ac0f5-109">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="ac0f5-110">이름을 지정하지 않으면 이 cmdlet은 작업 영역의 모든 연결된 서비스에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ac0f5-110">If you do not specify a name, this cmdlet gets information about all the linked services in the workspace.</span></span>

## <span data-ttu-id="ac0f5-111">예제</span><span class="sxs-lookup"><span data-stu-id="ac0f5-111">EXAMPLES</span></span>

### <span data-ttu-id="ac0f5-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="ac0f5-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseLinkedService -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="ac0f5-113">이 명령은 ContosoWorkspace라는 작업 영역의 모든 연결된 서비스에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ac0f5-113">This command gets information about all linked services in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="ac0f5-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="ac0f5-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
```

<span data-ttu-id="ac0f5-115">이 명령은 ContosoWorkspace라는 작업 영역의 ContosoLinkedService라는 연결된 서비스에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ac0f5-115">This command gets information about the linked service named ContosoLinkedService in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="ac0f5-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="ac0f5-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseLinkedService -Name ContosoLinkedService
```

<span data-ttu-id="ac0f5-117">이 명령은 파이프라인을 통해 ContosoWorkspace라는 작업 영역의 ContosoLinkedService라는 연결된 서비스에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ac0f5-117">This command gets information about the linked service named ContosoLinkedService in the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="ac0f5-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ac0f5-118">PARAMETERS</span></span>

### <span data-ttu-id="ac0f5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac0f5-119">-DefaultProfile</span></span>
<span data-ttu-id="ac0f5-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ac0f5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac0f5-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ac0f5-121">-Name</span></span>
<span data-ttu-id="ac0f5-122">연결된 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ac0f5-122">The linked service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: LinkedServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac0f5-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ac0f5-123">-WorkspaceName</span></span>
<span data-ttu-id="ac0f5-124">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ac0f5-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac0f5-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ac0f5-125">-WorkspaceObject</span></span>
<span data-ttu-id="ac0f5-126">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ac0f5-126">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac0f5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac0f5-127">CommonParameters</span></span>
<span data-ttu-id="ac0f5-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ac0f5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac0f5-129">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ac0f5-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac0f5-130">입력</span><span class="sxs-lookup"><span data-stu-id="ac0f5-130">INPUTS</span></span>

### <span data-ttu-id="ac0f5-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ac0f5-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="ac0f5-132">출력</span><span class="sxs-lookup"><span data-stu-id="ac0f5-132">OUTPUTS</span></span>

### <span data-ttu-id="ac0f5-133">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="ac0f5-133">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="ac0f5-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ac0f5-134">NOTES</span></span>

## <span data-ttu-id="ac0f5-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ac0f5-135">RELATED LINKS</span></span>
