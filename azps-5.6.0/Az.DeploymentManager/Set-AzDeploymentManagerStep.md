---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/set-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerStep.md
ms.openlocfilehash: f8412ac037372d89373c64c77f43c10db1730100
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966224"
---
# <span data-ttu-id="b0b6a-101">Set-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="b0b6a-101">Set-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="b0b6a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0b6a-102">SYNOPSIS</span></span>
<span data-ttu-id="b0b6a-103">단계를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="b0b6a-103">Updates the step.</span></span>

## <span data-ttu-id="b0b6a-104">구문</span><span class="sxs-lookup"><span data-stu-id="b0b6a-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0b6a-105">설명</span><span class="sxs-lookup"><span data-stu-id="b0b6a-105">DESCRIPTION</span></span>
<span data-ttu-id="b0b6a-106">**Set-AzDeploymentManagerStep** cmdlet은 지정된 단계 개체로 단계를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="b0b6a-106">The **Set-AzDeploymentManagerStep** cmdlet updates a step with the specified step object.</span></span>
<span data-ttu-id="b0b6a-107">cmdlet은 업데이트된 단계 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="b0b6a-107">The cmdlet returns the updated step object.</span></span>

## <span data-ttu-id="b0b6a-108">예제</span><span class="sxs-lookup"><span data-stu-id="b0b6a-108">EXAMPLES</span></span>

### <span data-ttu-id="b0b6a-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="b0b6a-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerStep -InputObject $stepObject
```

<span data-ttu-id="b0b6a-110">이 명령은 이름과 ResourceGroup이 각각 해당 이름 및 ResourceGroupName 속성과 일치하는 $stepObject 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="b0b6a-110">This command updates a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>
<span data-ttu-id="b0b6a-111">이 단계는 에 설정된 속성으로 $stepObject.</span><span class="sxs-lookup"><span data-stu-id="b0b6a-111">The step would be updated to the properties set in the $stepObject.</span></span>

## <span data-ttu-id="b0b6a-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b0b6a-112">PARAMETERS</span></span>

### <span data-ttu-id="b0b6a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0b6a-113">-DefaultProfile</span></span>
<span data-ttu-id="b0b6a-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b0b6a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0b6a-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0b6a-115">-InputObject</span></span>
<span data-ttu-id="b0b6a-116">단계 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b0b6a-116">The step object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0b6a-117">-확인</span><span class="sxs-lookup"><span data-stu-id="b0b6a-117">-Confirm</span></span>
<span data-ttu-id="b0b6a-118">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b0b6a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0b6a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0b6a-119">-WhatIf</span></span>
<span data-ttu-id="b0b6a-120">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="b0b6a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0b6a-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b0b6a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0b6a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0b6a-122">CommonParameters</span></span>
<span data-ttu-id="b0b6a-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b0b6a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0b6a-124">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b0b6a-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0b6a-125">입력</span><span class="sxs-lookup"><span data-stu-id="b0b6a-125">INPUTS</span></span>

### <span data-ttu-id="b0b6a-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="b0b6a-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="b0b6a-127">출력</span><span class="sxs-lookup"><span data-stu-id="b0b6a-127">OUTPUTS</span></span>

### <span data-ttu-id="b0b6a-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="b0b6a-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="b0b6a-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b0b6a-129">NOTES</span></span>

## <span data-ttu-id="b0b6a-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b0b6a-130">RELATED LINKS</span></span>
