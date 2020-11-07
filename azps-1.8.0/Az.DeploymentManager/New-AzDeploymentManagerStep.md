---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerStep.md
ms.openlocfilehash: 2013f1722ee246db023f4d26d456eafffa8f40eb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700991"
---
# <span data-ttu-id="6a5a1-101">New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="6a5a1-101">New-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="6a5a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a5a1-102">SYNOPSIS</span></span>
<span data-ttu-id="6a5a1-103">단계를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6a5a1-103">Creates a step.</span></span>

## <span data-ttu-id="6a5a1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6a5a1-104">SYNTAX</span></span>

```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String> -Duration <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a5a1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6a5a1-105">DESCRIPTION</span></span>
<span data-ttu-id="6a5a1-106">**AzDeploymentManagerStep** cmdlet은 롤아웃에서 참조할 수 있는 배포 단계를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6a5a1-106">The **New-AzDeploymentManagerStep** cmdlet creates a deployment step that can be referenced in rollouts.</span></span>
<span data-ttu-id="6a5a1-107">*Name* , *ResourceGroupName* 및 required 속성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a5a1-107">Specify the *Name* , *ResourceGroupName* and required properties.</span></span>

<span data-ttu-id="6a5a1-108">반환 된 개체를 로컬로 수정한 다음 Set-AzDeploymentManagerStep cmdlet을 사용 하 여 단계에 변경 내용을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6a5a1-108">You can modify the returned object locally and then apply the changes to the step by using the Set-AzDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="6a5a1-109">예제의</span><span class="sxs-lookup"><span data-stu-id="6a5a1-109">EXAMPLES</span></span>

### <span data-ttu-id="6a5a1-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="6a5a1-110">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep -Location "Central US" -Duration PT20M
```

<span data-ttu-id="6a5a1-111">중앙 US와 이름이 ContosoService1WaitStep 인 ContosoResourceGroup에 리소스 위치로 이동 하는 단계를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6a5a1-111">Creates a step in the ContosoResourceGroup with the name ContosoService1WaitStep with Central US as the location of the resource.</span></span> <span data-ttu-id="6a5a1-112">Duration 속성은 다음 단계를 실행 하기 전에 롤아웃이 대기 하는 기간을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a5a1-112">The Duration property provides the duration the rollout will wait before running the next step.</span></span>

## <span data-ttu-id="6a5a1-113">변수</span><span class="sxs-lookup"><span data-stu-id="6a5a1-113">PARAMETERS</span></span>

### <span data-ttu-id="6a5a1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a5a1-114">-DefaultProfile</span></span>
<span data-ttu-id="6a5a1-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6a5a1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a5a1-116">-기간</span><span class="sxs-lookup"><span data-stu-id="6a5a1-116">-Duration</span></span>
<span data-ttu-id="6a5a1-117">ISO 8601 형식으로 대기할 기간입니다.</span><span class="sxs-lookup"><span data-stu-id="6a5a1-117">The duration to wait in ISO 8601 format.</span></span>
<span data-ttu-id="6a5a1-118">예: PT30M, PT1H</span><span class="sxs-lookup"><span data-stu-id="6a5a1-118">E.g.: PT30M, PT1H</span></span>

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

### <span data-ttu-id="6a5a1-119">-위치</span><span class="sxs-lookup"><span data-stu-id="6a5a1-119">-Location</span></span>
<span data-ttu-id="6a5a1-120">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="6a5a1-120">The location of the resource.</span></span>

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

### <span data-ttu-id="6a5a1-121">-이름</span><span class="sxs-lookup"><span data-stu-id="6a5a1-121">-Name</span></span>
<span data-ttu-id="6a5a1-122">단계의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6a5a1-122">The name of the step.</span></span>

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

### <span data-ttu-id="6a5a1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a5a1-123">-ResourceGroupName</span></span>
<span data-ttu-id="6a5a1-124">리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="6a5a1-124">The resource group.</span></span>

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

### <span data-ttu-id="6a5a1-125">태그</span><span class="sxs-lookup"><span data-stu-id="6a5a1-125">-Tag</span></span>
<span data-ttu-id="6a5a1-126">리소스 태그를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="6a5a1-126">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a5a1-127">-확인</span><span class="sxs-lookup"><span data-stu-id="6a5a1-127">-Confirm</span></span>
<span data-ttu-id="6a5a1-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a5a1-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a5a1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a5a1-129">-WhatIf</span></span>
<span data-ttu-id="6a5a1-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6a5a1-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a5a1-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6a5a1-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a5a1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a5a1-132">CommonParameters</span></span>
<span data-ttu-id="6a5a1-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a5a1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a5a1-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a5a1-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a5a1-135">입력</span><span class="sxs-lookup"><span data-stu-id="6a5a1-135">INPUTS</span></span>

### <span data-ttu-id="6a5a1-136">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="6a5a1-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6a5a1-137">출력</span><span class="sxs-lookup"><span data-stu-id="6a5a1-137">OUTPUTS</span></span>

### <span data-ttu-id="6a5a1-138">PSStepResource-. m i 매니저.</span><span class="sxs-lookup"><span data-stu-id="6a5a1-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="6a5a1-139">상속자</span><span class="sxs-lookup"><span data-stu-id="6a5a1-139">NOTES</span></span>

## <span data-ttu-id="6a5a1-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6a5a1-140">RELATED LINKS</span></span>
