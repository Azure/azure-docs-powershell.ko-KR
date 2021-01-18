---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: 4a9f785519710b7a6653b1ece27d7b526fceab31
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494594"
---
# <span data-ttu-id="a3ba9-101">Set-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="a3ba9-101">Set-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="a3ba9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3ba9-102">SYNOPSIS</span></span>
<span data-ttu-id="a3ba9-103">서비스 토폴로지 업데이트</span><span class="sxs-lookup"><span data-stu-id="a3ba9-103">Updates the service topology.</span></span>

## <span data-ttu-id="a3ba9-104">구문</span><span class="sxs-lookup"><span data-stu-id="a3ba9-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3ba9-105">설명</span><span class="sxs-lookup"><span data-stu-id="a3ba9-105">DESCRIPTION</span></span>
<span data-ttu-id="a3ba9-106">**Set-AzDeploymentManagerServiceTopology** cmdlet은 지정된 서비스 토폴로지 개체를 통해 서비스 토폴로지 업데이트를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a3ba9-106">The **Set-AzDeploymentManagerServiceTopology** cmdlet updates a service topology with the specified service topology object.</span></span>
<span data-ttu-id="a3ba9-107">cmdlet은 업데이트된 서비스 토폴로지 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="a3ba9-107">The cmdlet returns the updated service topology object.</span></span>

## <span data-ttu-id="a3ba9-108">예제</span><span class="sxs-lookup"><span data-stu-id="a3ba9-108">EXAMPLES</span></span>

### <span data-ttu-id="a3ba9-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="a3ba9-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="a3ba9-110">이 명령은 이름 및 ResourceGroup이 각각 이름 및 ResourceGroupName 속성과 일치하는 서비스 토폴로지 $serviceTopologyObject 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a3ba9-110">This command updates a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>
<span data-ttu-id="a3ba9-111">이 명령은 업데이트된 서비스 토폴로지 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="a3ba9-111">The command returns the updated service topology object.</span></span>

## <span data-ttu-id="a3ba9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3ba9-112">PARAMETERS</span></span>

### <span data-ttu-id="a3ba9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3ba9-113">-DefaultProfile</span></span>
<span data-ttu-id="a3ba9-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a3ba9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3ba9-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3ba9-115">-InputObject</span></span>
<span data-ttu-id="a3ba9-116">서비스 토폴로지 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a3ba9-116">The service topology object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3ba9-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a3ba9-117">-Confirm</span></span>
<span data-ttu-id="a3ba9-118">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3ba9-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3ba9-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3ba9-119">-WhatIf</span></span>
<span data-ttu-id="a3ba9-120">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a3ba9-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3ba9-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a3ba9-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3ba9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3ba9-122">CommonParameters</span></span>
<span data-ttu-id="a3ba9-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a3ba9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3ba9-124">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a3ba9-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3ba9-125">입력</span><span class="sxs-lookup"><span data-stu-id="a3ba9-125">INPUTS</span></span>

### <span data-ttu-id="a3ba9-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="a3ba9-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="a3ba9-127">출력</span><span class="sxs-lookup"><span data-stu-id="a3ba9-127">OUTPUTS</span></span>

### <span data-ttu-id="a3ba9-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="a3ba9-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="a3ba9-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a3ba9-129">NOTES</span></span>

## <span data-ttu-id="a3ba9-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a3ba9-130">RELATED LINKS</span></span>
