---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: 7d2a7916e73b20e4c4e7a3602dc23bc10a67c744
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196489"
---
# <span data-ttu-id="1431a-101">Set-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="1431a-101">Set-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="1431a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1431a-102">SYNOPSIS</span></span>
<span data-ttu-id="1431a-103">서비스 단위를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="1431a-103">Updates the service unit.</span></span>

## <span data-ttu-id="1431a-104">구문</span><span class="sxs-lookup"><span data-stu-id="1431a-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerServiceUnit [-InputObject] <PSServiceUnitResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1431a-105">설명</span><span class="sxs-lookup"><span data-stu-id="1431a-105">DESCRIPTION</span></span>
<span data-ttu-id="1431a-106">**Set-AzDeploymentManagerServiceUnit** cmdlet은 지정된 서비스 단위 개체로 서비스 단위를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="1431a-106">The **Set-AzDeploymentManagerServiceUnit** cmdlet updates a service unit with the specified service unit object.</span></span>
<span data-ttu-id="1431a-107">cmdlet은 업데이트된 서비스 단위 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="1431a-107">The cmdlet returns the updated service unit object.</span></span>

## <span data-ttu-id="1431a-108">예제</span><span class="sxs-lookup"><span data-stu-id="1431a-108">EXAMPLES</span></span>

### <span data-ttu-id="1431a-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="1431a-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerServiceUnit -InputObject $serviceUnitObject
```

<span data-ttu-id="1431a-110">이 명령은 이름, 서비스 이름, 서비스 토폴로지 이름 및 ResourceGroup이 각각 이름, ServiceName, ServiceTopologyName 및 ResourceGroupName 속성과 일치하는 서비스 $serviceUnitObject 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="1431a-110">This command updates a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>
<span data-ttu-id="1431a-111">이 명령은 업데이트된 서비스 단위 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="1431a-111">The command returns the updated service unit object.</span></span>

## <span data-ttu-id="1431a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1431a-112">PARAMETERS</span></span>

### <span data-ttu-id="1431a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1431a-113">-DefaultProfile</span></span>
<span data-ttu-id="1431a-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1431a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1431a-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1431a-115">-InputObject</span></span>
<span data-ttu-id="1431a-116">서비스 단위 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="1431a-116">The service unit object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1431a-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1431a-117">-Confirm</span></span>
<span data-ttu-id="1431a-118">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1431a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1431a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1431a-119">-WhatIf</span></span>
<span data-ttu-id="1431a-120">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1431a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1431a-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1431a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1431a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1431a-122">CommonParameters</span></span>
<span data-ttu-id="1431a-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1431a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1431a-124">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1431a-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1431a-125">입력</span><span class="sxs-lookup"><span data-stu-id="1431a-125">INPUTS</span></span>

### <span data-ttu-id="1431a-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="1431a-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="1431a-127">출력</span><span class="sxs-lookup"><span data-stu-id="1431a-127">OUTPUTS</span></span>

### <span data-ttu-id="1431a-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="1431a-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="1431a-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1431a-129">NOTES</span></span>

## <span data-ttu-id="1431a-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1431a-130">RELATED LINKS</span></span>
