---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/new-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/New-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/New-AzDevSpacesController.md
ms.openlocfilehash: 0429eebf0425a950bcf093d7659a2d87b3b661f1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93696623"
---
# <span data-ttu-id="00814-101">New-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="00814-101">New-AzDevSpacesController</span></span>

## <span data-ttu-id="00814-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00814-102">SYNOPSIS</span></span>
<span data-ttu-id="00814-103">새 Azure DevSpaces 컨트롤러를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="00814-103">Create a new Azure DevSpaces controller.</span></span>

## <span data-ttu-id="00814-104">구문과</span><span class="sxs-lookup"><span data-stu-id="00814-104">SYNTAX</span></span>

```
New-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-TargetResourceGroupName] <String>
 [-TargetClusterName] <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00814-105">설명은</span><span class="sxs-lookup"><span data-stu-id="00814-105">DESCRIPTION</span></span>
<span data-ttu-id="00814-106">새 Azure DevSpaces 컨트롤러를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="00814-106">Create a new Azure DevSpaces controller.</span></span>

## <span data-ttu-id="00814-107">예제의</span><span class="sxs-lookup"><span data-stu-id="00814-107">EXAMPLES</span></span>

### <span data-ttu-id="00814-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="00814-108">Example 1</span></span>
```powershell
PS C:\> New-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -TargetResourceGroupName clusterResourceGroup -TargetClusterName clusterName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="00814-109">이름 devSpaceName를 사용 하 여 resourcegroup devSpaceResourceGroup에 DevSpaces 컨트롤러를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="00814-109">Create a DevSpaces controller in resourcegroup devSpaceResourceGroup with a name devSpaceName.</span></span> <span data-ttu-id="00814-110">이 컨트롤러의 대상으로 clusterName 클러스터를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="00814-110">Use clusterName cluster as a target for this controller.</span></span>

## <span data-ttu-id="00814-111">변수</span><span class="sxs-lookup"><span data-stu-id="00814-111">PARAMETERS</span></span>

### <span data-ttu-id="00814-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="00814-112">-AsJob</span></span>
<span data-ttu-id="00814-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="00814-113">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00814-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00814-114">-DefaultProfile</span></span>
<span data-ttu-id="00814-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="00814-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00814-116">-이름</span><span class="sxs-lookup"><span data-stu-id="00814-116">-Name</span></span>
<span data-ttu-id="00814-117">DevSpaces 컨트롤러 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="00814-117">DevSpaces Controller Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00814-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00814-118">-ResourceGroupName</span></span>
<span data-ttu-id="00814-119">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="00814-119">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00814-120">태그</span><span class="sxs-lookup"><span data-stu-id="00814-120">-Tag</span></span>
<span data-ttu-id="00814-121">리소스 태그를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="00814-121">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="00814-122">-TargetClusterName</span><span class="sxs-lookup"><span data-stu-id="00814-122">-TargetClusterName</span></span>
<span data-ttu-id="00814-123">대상 클러스터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="00814-123">Target Cluster Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00814-124">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00814-124">-TargetResourceGroupName</span></span>
<span data-ttu-id="00814-125">대상 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="00814-125">Target Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00814-126">-확인</span><span class="sxs-lookup"><span data-stu-id="00814-126">-Confirm</span></span>
<span data-ttu-id="00814-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="00814-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00814-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00814-128">-WhatIf</span></span>
<span data-ttu-id="00814-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="00814-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00814-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="00814-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00814-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00814-131">CommonParameters</span></span>
<span data-ttu-id="00814-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="00814-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00814-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00814-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00814-134">입력</span><span class="sxs-lookup"><span data-stu-id="00814-134">INPUTS</span></span>

### <span data-ttu-id="00814-135">않아야</span><span class="sxs-lookup"><span data-stu-id="00814-135">None</span></span>

## <span data-ttu-id="00814-136">출력</span><span class="sxs-lookup"><span data-stu-id="00814-136">OUTPUTS</span></span>

### <span data-ttu-id="00814-137">Microsoft. Vspaces. 모델. PSController</span><span class="sxs-lookup"><span data-stu-id="00814-137">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="00814-138">상속자</span><span class="sxs-lookup"><span data-stu-id="00814-138">NOTES</span></span>

## <span data-ttu-id="00814-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="00814-139">RELATED LINKS</span></span>
