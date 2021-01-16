---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerService.md
ms.openlocfilehash: fb3f7ccab164370e1c55992a666ac7256b5a4a95
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333614"
---
# <span data-ttu-id="c769e-101">Set-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="c769e-101">Set-AzDeploymentManagerService</span></span>

## <span data-ttu-id="c769e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c769e-102">SYNOPSIS</span></span>
<span data-ttu-id="c769e-103">서비스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c769e-103">Updates the service.</span></span>

## <span data-ttu-id="c769e-104">구문</span><span class="sxs-lookup"><span data-stu-id="c769e-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c769e-105">설명</span><span class="sxs-lookup"><span data-stu-id="c769e-105">DESCRIPTION</span></span>
<span data-ttu-id="c769e-106">**Set-AzDeploymentManagerService** cmdlet은 지정된 서비스 개체를 통해 서비스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c769e-106">The **Set-AzDeploymentManagerService** cmdlet updates a service with the specified service object.</span></span>
<span data-ttu-id="c769e-107">cmdlet은 업데이트된 서비스 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="c769e-107">The cmdlet returns the updated service object.</span></span>

## <span data-ttu-id="c769e-108">예제</span><span class="sxs-lookup"><span data-stu-id="c769e-108">EXAMPLES</span></span>

### <span data-ttu-id="c769e-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="c769e-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="c769e-110">이 명령은 이름, 서비스 토폴로지 이름 및 ResourceGroup이 각각 이름, ServiceTopologyName 및 ResourceGroupName 속성과 일치하는 서비스를 $serviceObject 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c769e-110">This command updates a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>
<span data-ttu-id="c769e-111">서비스는 서비스에서 설정한 속성으로 $serviceObject.</span><span class="sxs-lookup"><span data-stu-id="c769e-111">The service would be updated to the properties set in the $serviceObject.</span></span>

## <span data-ttu-id="c769e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c769e-112">PARAMETERS</span></span>

### <span data-ttu-id="c769e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c769e-113">-DefaultProfile</span></span>
<span data-ttu-id="c769e-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c769e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c769e-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c769e-115">-InputObject</span></span>
<span data-ttu-id="c769e-116">서비스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="c769e-116">The service object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c769e-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c769e-117">-Confirm</span></span>
<span data-ttu-id="c769e-118">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c769e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c769e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c769e-119">-WhatIf</span></span>
<span data-ttu-id="c769e-120">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c769e-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c769e-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c769e-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c769e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c769e-122">CommonParameters</span></span>
<span data-ttu-id="c769e-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c769e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c769e-124">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c769e-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c769e-125">입력</span><span class="sxs-lookup"><span data-stu-id="c769e-125">INPUTS</span></span>

### <span data-ttu-id="c769e-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="c769e-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="c769e-127">출력</span><span class="sxs-lookup"><span data-stu-id="c769e-127">OUTPUTS</span></span>

### <span data-ttu-id="c769e-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="c769e-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="c769e-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c769e-129">NOTES</span></span>

## <span data-ttu-id="c769e-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c769e-130">RELATED LINKS</span></span>
