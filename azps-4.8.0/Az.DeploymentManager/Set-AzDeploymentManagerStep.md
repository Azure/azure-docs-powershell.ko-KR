---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerStep.md
ms.openlocfilehash: 2cd73cad57f36130ed11e37ad6dc2147e6c081ae
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212805"
---
# <span data-ttu-id="7cd1f-101">Set-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="7cd1f-101">Set-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="7cd1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7cd1f-102">SYNOPSIS</span></span>
<span data-ttu-id="7cd1f-103">단계를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7cd1f-103">Updates the step.</span></span>

## <span data-ttu-id="7cd1f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7cd1f-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7cd1f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7cd1f-105">DESCRIPTION</span></span>
<span data-ttu-id="7cd1f-106">**AzDeploymentManagerStep** cmdlet은 지정 된 step 개체를 사용 하 여 단계를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7cd1f-106">The **Set-AzDeploymentManagerStep** cmdlet updates a step with the specified step object.</span></span>
<span data-ttu-id="7cd1f-107">Cmdlet은 업데이트 된 step 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7cd1f-107">The cmdlet returns the updated step object.</span></span>

## <span data-ttu-id="7cd1f-108">예제의</span><span class="sxs-lookup"><span data-stu-id="7cd1f-108">EXAMPLES</span></span>

### <span data-ttu-id="7cd1f-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="7cd1f-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerStep -InputObject $stepObject
```

<span data-ttu-id="7cd1f-110">이 명령은 name 및 ResourceGroup이 $stepObject의 Name 및 ResourceGroupName 속성과 각각 일치 하는 단계를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7cd1f-110">This command updates a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>
<span data-ttu-id="7cd1f-111">단계가 $stepObject에 설정 된 속성으로 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7cd1f-111">The step would be updated to the properties set in the $stepObject.</span></span>

## <span data-ttu-id="7cd1f-112">변수</span><span class="sxs-lookup"><span data-stu-id="7cd1f-112">PARAMETERS</span></span>

### <span data-ttu-id="7cd1f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cd1f-113">-DefaultProfile</span></span>
<span data-ttu-id="7cd1f-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7cd1f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7cd1f-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7cd1f-115">-InputObject</span></span>
<span data-ttu-id="7cd1f-116">Step 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7cd1f-116">The step object.</span></span>

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

### <span data-ttu-id="7cd1f-117">-확인</span><span class="sxs-lookup"><span data-stu-id="7cd1f-117">-Confirm</span></span>
<span data-ttu-id="7cd1f-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7cd1f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cd1f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cd1f-119">-WhatIf</span></span>
<span data-ttu-id="7cd1f-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7cd1f-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cd1f-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7cd1f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cd1f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cd1f-122">CommonParameters</span></span>
<span data-ttu-id="7cd1f-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7cd1f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cd1f-124">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7cd1f-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cd1f-125">입력</span><span class="sxs-lookup"><span data-stu-id="7cd1f-125">INPUTS</span></span>

### <span data-ttu-id="7cd1f-126">PSStepResource-. m i 매니저.</span><span class="sxs-lookup"><span data-stu-id="7cd1f-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="7cd1f-127">출력</span><span class="sxs-lookup"><span data-stu-id="7cd1f-127">OUTPUTS</span></span>

### <span data-ttu-id="7cd1f-128">PSStepResource-. m i 매니저.</span><span class="sxs-lookup"><span data-stu-id="7cd1f-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="7cd1f-129">상속자</span><span class="sxs-lookup"><span data-stu-id="7cd1f-129">NOTES</span></span>

## <span data-ttu-id="7cd1f-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7cd1f-130">RELATED LINKS</span></span>
