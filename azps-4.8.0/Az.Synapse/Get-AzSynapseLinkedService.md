---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapselinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseLinkedService.md
ms.openlocfilehash: d7f494b6ba943214106363a5b7dfe4dfb5cdd877
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048567"
---
# <span data-ttu-id="246ca-101">Get-AzSynapseLinkedService</span><span class="sxs-lookup"><span data-stu-id="246ca-101">Get-AzSynapseLinkedService</span></span>

## <span data-ttu-id="246ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="246ca-102">SYNOPSIS</span></span>
<span data-ttu-id="246ca-103">작업 영역에서 연결 된 서비스에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="246ca-103">Gets information about linked services in workspace.</span></span>

## <span data-ttu-id="246ca-104">구문과</span><span class="sxs-lookup"><span data-stu-id="246ca-104">SYNTAX</span></span>

### <span data-ttu-id="246ca-105">GetByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="246ca-105">GetByName (Default)</span></span>
```
Get-AzSynapseLinkedService -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="246ca-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="246ca-106">GetByObject</span></span>
```
Get-AzSynapseLinkedService -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="246ca-107">설명은</span><span class="sxs-lookup"><span data-stu-id="246ca-107">DESCRIPTION</span></span>
<span data-ttu-id="246ca-108">**AzSynapseLinkedService** cmdlet은 작업 영역의 연결 된 서비스에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="246ca-108">The **Get-AzSynapseLinkedService** cmdlet gets information about linked services in workspace.</span></span>
<span data-ttu-id="246ca-109">연결 된 서비스의 이름을 지정 하는 경우이 cmdlet은 연결 된 서비스에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="246ca-109">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="246ca-110">이름을 지정 하지 않으면이 cmdlet은 작업 영역의 모든 연결 된 서비스에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="246ca-110">If you do not specify a name, this cmdlet gets information about all the linked services in the workspace.</span></span>

## <span data-ttu-id="246ca-111">예제의</span><span class="sxs-lookup"><span data-stu-id="246ca-111">EXAMPLES</span></span>

### <span data-ttu-id="246ca-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="246ca-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseLinkedService -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="246ca-113">이 명령은 ContosoWorkspace 이라는 작업 영역의 모든 연결 된 서비스에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="246ca-113">This command gets information about all linked services in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="246ca-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="246ca-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
```

<span data-ttu-id="246ca-115">이 명령은 ContosoWorkspace 이라는 작업 영역에서 ContosoLinkedService 이라는 연결 된 서비스에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="246ca-115">This command gets information about the linked service named ContosoLinkedService in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="246ca-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="246ca-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseLinkedService -Name ContosoLinkedService
```

<span data-ttu-id="246ca-117">이 명령은 ContosoWorkspace ~ 파이프라인 이라는 작업 영역에서 ContosoLinkedService 이라는 연결 된 서비스에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="246ca-117">This command gets information about the linked service named ContosoLinkedService in the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="246ca-118">변수</span><span class="sxs-lookup"><span data-stu-id="246ca-118">PARAMETERS</span></span>

### <span data-ttu-id="246ca-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="246ca-119">-DefaultProfile</span></span>
<span data-ttu-id="246ca-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="246ca-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="246ca-121">-이름</span><span class="sxs-lookup"><span data-stu-id="246ca-121">-Name</span></span>
<span data-ttu-id="246ca-122">연결 된 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="246ca-122">The linked service name.</span></span>

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

### <span data-ttu-id="246ca-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="246ca-123">-WorkspaceName</span></span>
<span data-ttu-id="246ca-124">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="246ca-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="246ca-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="246ca-125">-WorkspaceObject</span></span>
<span data-ttu-id="246ca-126">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="246ca-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="246ca-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="246ca-127">CommonParameters</span></span>
<span data-ttu-id="246ca-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="246ca-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="246ca-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="246ca-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="246ca-130">입력</span><span class="sxs-lookup"><span data-stu-id="246ca-130">INPUTS</span></span>

### <span data-ttu-id="246ca-131">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="246ca-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="246ca-132">출력</span><span class="sxs-lookup"><span data-stu-id="246ca-132">OUTPUTS</span></span>

### <span data-ttu-id="246ca-133">Synapse. PSLinkedServiceResource/.</span><span class="sxs-lookup"><span data-stu-id="246ca-133">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="246ca-134">상속자</span><span class="sxs-lookup"><span data-stu-id="246ca-134">NOTES</span></span>

## <span data-ttu-id="246ca-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="246ca-135">RELATED LINKS</span></span>
