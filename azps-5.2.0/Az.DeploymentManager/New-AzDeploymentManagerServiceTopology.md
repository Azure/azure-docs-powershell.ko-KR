---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: c104f074b972e42aaa21ce4e85c6076294ec5aa2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355917"
---
# <span data-ttu-id="05a4f-101">New-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="05a4f-101">New-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="05a4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05a4f-102">SYNOPSIS</span></span>
<span data-ttu-id="05a4f-103">서비스 토폴로지 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="05a4f-103">Creates a service topology.</span></span>

## <span data-ttu-id="05a4f-104">구문</span><span class="sxs-lookup"><span data-stu-id="05a4f-104">SYNTAX</span></span>

```
New-AzDeploymentManagerServiceTopology -ResourceGroupName <String> -Name <String> -Location <String>
 [-ArtifactSourceId <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05a4f-105">설명</span><span class="sxs-lookup"><span data-stu-id="05a4f-105">DESCRIPTION</span></span>
<span data-ttu-id="05a4f-106">**New-AzDeploymentManagerServiceTopology** cmdlet은 서비스 토폴로지가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="05a4f-106">The **New-AzDeploymentManagerServiceTopology** cmdlet creates a service topology.</span></span>

<span data-ttu-id="05a4f-107">반환된 ServiceTopology 개체를 로컬로 수정한 다음, Set-AzDeploymentManagerServiceTopology cmdlet을 사용하여 토폴로지에 변경 내용을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="05a4f-107">You can modify the returned ServiceTopology object locally, and then apply changes to the topology by using the Set-AzDeploymentManagerServiceTopology cmdlet.</span></span>
<span data-ttu-id="05a4f-108">반환된 개체</span><span class="sxs-lookup"><span data-stu-id="05a4f-108">The returned object</span></span> 

<span data-ttu-id="05a4f-109">반환된 개체에는 이 서비스 토폴로지에서 선언된 서비스가 롤아웃에 배포될 것임을 나타내기 위해 롤아웃 리소스에서 참조할 수 있는 ResourceId 필드가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="05a4f-109">The returned object has a ResourceId field which can be referenced in a rollout resource to indicate that the services declared in this service topology would be deployed in the rollout.</span></span>

## <span data-ttu-id="05a4f-110">예제</span><span class="sxs-lookup"><span data-stu-id="05a4f-110">EXAMPLES</span></span>

### <span data-ttu-id="05a4f-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="05a4f-111">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology -Location "Central US" -ArtifactSourceId "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="05a4f-112">이 cmdlet은 ContosoServiceTopology 이름이 ContosoServiceTopology인 리소스 그룹 ContosoResourceGroup 및 미국 중부 위치에 새 서비스 토폴로지가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="05a4f-112">This cmdlet creates a new service topology in the resource group ContosoResourceGroup with the name ContosoServiceTopology and in location Central US.</span></span> <span data-ttu-id="05a4f-113">아티팩트 원본 ResourceId는 이 토폴로지의 서비스 단위 정의에 필요한 아티팩트를 지정된 아티팩트 원본에서 읽어야 하다는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="05a4f-113">The artifact source ResourceId indicates that the artifacts required for the service unit definitions in this topology need to be read from the specified artifact source.</span></span>

### <span data-ttu-id="05a4f-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="05a4f-114">Example 2</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology -Location "Central US"
```

<span data-ttu-id="05a4f-115">이 cmdlet은 ContosoServiceTopology 이름이 ContosoServiceTopology인 리소스 그룹 ContosoResourceGroup 및 미국 중부 위치에 새 서비스 토폴로지가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="05a4f-115">This cmdlet creates a new service topology in the resource group ContosoResourceGroup with the name ContosoServiceTopology and in location Central US.</span></span> <span data-ttu-id="05a4f-116">아티팩트 원본 참조가 없는 것은 이 토폴로지의 서비스 단위 정의에 필요한 아티팩트가 서비스 단위에서 절대 SAS URIS로 제공될 것임을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="05a4f-116">The absence of an artifact source reference indicates that the artifacts required for the service unit definitions in this topology would be provided as absolute SAS URIs in the service unit.</span></span>

## <span data-ttu-id="05a4f-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="05a4f-117">PARAMETERS</span></span>

### <span data-ttu-id="05a4f-118">-ArtifactSourceId</span><span class="sxs-lookup"><span data-stu-id="05a4f-118">-ArtifactSourceId</span></span>
<span data-ttu-id="05a4f-119">토폴로지로 만드는 아티팩트가 저장되는 아티팩트 원본의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="05a4f-119">The identifier of the artifact source, where the artifacts that make up the topology are stored.</span></span>

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

### <span data-ttu-id="05a4f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05a4f-120">-DefaultProfile</span></span>
<span data-ttu-id="05a4f-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="05a4f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05a4f-122">-Location</span><span class="sxs-lookup"><span data-stu-id="05a4f-122">-Location</span></span>
<span data-ttu-id="05a4f-123">토폴로지의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="05a4f-123">The location of the topology.</span></span>

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

### <span data-ttu-id="05a4f-124">-Name</span><span class="sxs-lookup"><span data-stu-id="05a4f-124">-Name</span></span>
<span data-ttu-id="05a4f-125">토폴로지의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="05a4f-125">The name of the topology.</span></span>

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

### <span data-ttu-id="05a4f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05a4f-126">-ResourceGroupName</span></span>
<span data-ttu-id="05a4f-127">리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="05a4f-127">The resource group.</span></span>

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

### <span data-ttu-id="05a4f-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="05a4f-128">-Tag</span></span>
<span data-ttu-id="05a4f-129">리소스 태그를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="05a4f-129">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05a4f-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="05a4f-130">-Confirm</span></span>
<span data-ttu-id="05a4f-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="05a4f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05a4f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05a4f-132">-WhatIf</span></span>
<span data-ttu-id="05a4f-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="05a4f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05a4f-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="05a4f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05a4f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05a4f-135">CommonParameters</span></span>
<span data-ttu-id="05a4f-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="05a4f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05a4f-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="05a4f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05a4f-138">입력</span><span class="sxs-lookup"><span data-stu-id="05a4f-138">INPUTS</span></span>

### <span data-ttu-id="05a4f-139">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="05a4f-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="05a4f-140">출력</span><span class="sxs-lookup"><span data-stu-id="05a4f-140">OUTPUTS</span></span>

### <span data-ttu-id="05a4f-141">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="05a4f-141">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="05a4f-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="05a4f-142">NOTES</span></span>

## <span data-ttu-id="05a4f-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="05a4f-143">RELATED LINKS</span></span>
