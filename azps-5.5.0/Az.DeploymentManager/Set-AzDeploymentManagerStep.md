---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerStep.md
ms.openlocfilehash: 2cd73cad57f36130ed11e37ad6dc2147e6c081ae
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209752"
---
# <span data-ttu-id="08377-101">Set-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="08377-101">Set-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="08377-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08377-102">SYNOPSIS</span></span>
<span data-ttu-id="08377-103">단계를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="08377-103">Updates the step.</span></span>

## <span data-ttu-id="08377-104">구문</span><span class="sxs-lookup"><span data-stu-id="08377-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08377-105">설명</span><span class="sxs-lookup"><span data-stu-id="08377-105">DESCRIPTION</span></span>
<span data-ttu-id="08377-106">**Set-AzDeploymentManagerStep** cmdlet은 지정된 단계 개체를 통해 단계를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="08377-106">The **Set-AzDeploymentManagerStep** cmdlet updates a step with the specified step object.</span></span>
<span data-ttu-id="08377-107">cmdlet은 업데이트된 단계 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="08377-107">The cmdlet returns the updated step object.</span></span>

## <span data-ttu-id="08377-108">예제</span><span class="sxs-lookup"><span data-stu-id="08377-108">EXAMPLES</span></span>

### <span data-ttu-id="08377-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="08377-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerStep -InputObject $stepObject
```

<span data-ttu-id="08377-110">이 명령은 이름 및 ResourceGroup이 각각 이름 및 ResourceGroupName 속성과 일치하는 단계를 $stepObject 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="08377-110">This command updates a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>
<span data-ttu-id="08377-111">이 단계는 다음 단계에서 설정한 속성으로 $stepObject.</span><span class="sxs-lookup"><span data-stu-id="08377-111">The step would be updated to the properties set in the $stepObject.</span></span>

## <span data-ttu-id="08377-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="08377-112">PARAMETERS</span></span>

### <span data-ttu-id="08377-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08377-113">-DefaultProfile</span></span>
<span data-ttu-id="08377-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="08377-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08377-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="08377-115">-InputObject</span></span>
<span data-ttu-id="08377-116">단계 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="08377-116">The step object.</span></span>

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

### <span data-ttu-id="08377-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="08377-117">-Confirm</span></span>
<span data-ttu-id="08377-118">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="08377-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08377-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08377-119">-WhatIf</span></span>
<span data-ttu-id="08377-120">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="08377-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08377-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="08377-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08377-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08377-122">CommonParameters</span></span>
<span data-ttu-id="08377-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="08377-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08377-124">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="08377-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08377-125">입력</span><span class="sxs-lookup"><span data-stu-id="08377-125">INPUTS</span></span>

### <span data-ttu-id="08377-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="08377-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="08377-127">출력</span><span class="sxs-lookup"><span data-stu-id="08377-127">OUTPUTS</span></span>

### <span data-ttu-id="08377-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="08377-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="08377-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="08377-129">NOTES</span></span>

## <span data-ttu-id="08377-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="08377-130">RELATED LINKS</span></span>
