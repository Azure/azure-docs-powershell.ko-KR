---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: c104f074b972e42aaa21ce4e85c6076294ec5aa2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047808"
---
# <span data-ttu-id="76e3c-101">New-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="76e3c-101">New-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="76e3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76e3c-102">SYNOPSIS</span></span>
<span data-ttu-id="76e3c-103">서비스 토폴로지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="76e3c-103">Creates a service topology.</span></span>

## <span data-ttu-id="76e3c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="76e3c-104">SYNTAX</span></span>

```
New-AzDeploymentManagerServiceTopology -ResourceGroupName <String> -Name <String> -Location <String>
 [-ArtifactSourceId <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76e3c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="76e3c-105">DESCRIPTION</span></span>
<span data-ttu-id="76e3c-106">**새 AzDeploymentManagerServiceTopology** cmdlet은 서비스 토폴로지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="76e3c-106">The **New-AzDeploymentManagerServiceTopology** cmdlet creates a service topology.</span></span>

<span data-ttu-id="76e3c-107">반환 된 ServiceTopology 개체를 로컬로 수정한 다음 Set-AzDeploymentManagerServiceTopology cmdlet을 사용 하 여 토폴로지에 변경 내용을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76e3c-107">You can modify the returned ServiceTopology object locally, and then apply changes to the topology by using the Set-AzDeploymentManagerServiceTopology cmdlet.</span></span>
<span data-ttu-id="76e3c-108">반환 된 개체</span><span class="sxs-lookup"><span data-stu-id="76e3c-108">The returned object</span></span> 

<span data-ttu-id="76e3c-109">반환 된 개체에는 롤아웃 리소스에서 참조할 수 있는 ResourceId 필드가 있으며,이는이 서비스 토폴로지에 선언 된 서비스가 롤아웃에 배포 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="76e3c-109">The returned object has a ResourceId field which can be referenced in a rollout resource to indicate that the services declared in this service topology would be deployed in the rollout.</span></span>

## <span data-ttu-id="76e3c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="76e3c-110">EXAMPLES</span></span>

### <span data-ttu-id="76e3c-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="76e3c-111">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology -Location "Central US" -ArtifactSourceId "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="76e3c-112">이 cmdlet은 이름 ContosoServiceTopology 및 in 위치 중앙 US를 사용 하 여 리소스 그룹 ContosoResourceGroup에 새 서비스 토폴로지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="76e3c-112">This cmdlet creates a new service topology in the resource group ContosoResourceGroup with the name ContosoServiceTopology and in location Central US.</span></span> <span data-ttu-id="76e3c-113">아티팩트 원본 ResourceId는이 토폴로지의 서비스 단위 정의에 필요한 아티팩트를 지정 된 아티팩트 원본에서 읽어야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="76e3c-113">The artifact source ResourceId indicates that the artifacts required for the service unit definitions in this topology need to be read from the specified artifact source.</span></span>

### <span data-ttu-id="76e3c-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="76e3c-114">Example 2</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology -Location "Central US"
```

<span data-ttu-id="76e3c-115">이 cmdlet은 이름 ContosoServiceTopology 및 in 위치 중앙 US를 사용 하 여 리소스 그룹 ContosoResourceGroup에 새 서비스 토폴로지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="76e3c-115">This cmdlet creates a new service topology in the resource group ContosoResourceGroup with the name ContosoServiceTopology and in location Central US.</span></span> <span data-ttu-id="76e3c-116">아티팩트 원본 참조가 없으면이 토폴로지의 서비스 단위 정의에 필요한 아티팩트가 서비스 단위에서 절대 SAS Uri로 제공 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="76e3c-116">The absence of an artifact source reference indicates that the artifacts required for the service unit definitions in this topology would be provided as absolute SAS URIs in the service unit.</span></span>

## <span data-ttu-id="76e3c-117">변수</span><span class="sxs-lookup"><span data-stu-id="76e3c-117">PARAMETERS</span></span>

### <span data-ttu-id="76e3c-118">-ArtifactSourceId</span><span class="sxs-lookup"><span data-stu-id="76e3c-118">-ArtifactSourceId</span></span>
<span data-ttu-id="76e3c-119">토폴로지를 구성 하는 아티팩트가 저장 되는 아티팩트 소스의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="76e3c-119">The identifier of the artifact source, where the artifacts that make up the topology are stored.</span></span>

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

### <span data-ttu-id="76e3c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76e3c-120">-DefaultProfile</span></span>
<span data-ttu-id="76e3c-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="76e3c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76e3c-122">-위치</span><span class="sxs-lookup"><span data-stu-id="76e3c-122">-Location</span></span>
<span data-ttu-id="76e3c-123">토폴로지의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="76e3c-123">The location of the topology.</span></span>

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

### <span data-ttu-id="76e3c-124">-이름</span><span class="sxs-lookup"><span data-stu-id="76e3c-124">-Name</span></span>
<span data-ttu-id="76e3c-125">토폴로지 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="76e3c-125">The name of the topology.</span></span>

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

### <span data-ttu-id="76e3c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76e3c-126">-ResourceGroupName</span></span>
<span data-ttu-id="76e3c-127">리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="76e3c-127">The resource group.</span></span>

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

### <span data-ttu-id="76e3c-128">태그</span><span class="sxs-lookup"><span data-stu-id="76e3c-128">-Tag</span></span>
<span data-ttu-id="76e3c-129">리소스 태그를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="76e3c-129">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="76e3c-130">-확인</span><span class="sxs-lookup"><span data-stu-id="76e3c-130">-Confirm</span></span>
<span data-ttu-id="76e3c-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="76e3c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76e3c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76e3c-132">-WhatIf</span></span>
<span data-ttu-id="76e3c-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="76e3c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76e3c-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="76e3c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76e3c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76e3c-135">CommonParameters</span></span>
<span data-ttu-id="76e3c-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="76e3c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76e3c-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="76e3c-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76e3c-138">입력</span><span class="sxs-lookup"><span data-stu-id="76e3c-138">INPUTS</span></span>

### <span data-ttu-id="76e3c-139">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="76e3c-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="76e3c-140">출력</span><span class="sxs-lookup"><span data-stu-id="76e3c-140">OUTPUTS</span></span>

### <span data-ttu-id="76e3c-141">PSServiceTopologyResource-. m i 매니저.</span><span class="sxs-lookup"><span data-stu-id="76e3c-141">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="76e3c-142">상속자</span><span class="sxs-lookup"><span data-stu-id="76e3c-142">NOTES</span></span>

## <span data-ttu-id="76e3c-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="76e3c-143">RELATED LINKS</span></span>
