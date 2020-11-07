---
external help file: Microsoft.Azure.Commands.DevSpaces.dll-Help.xml
Module Name: AzureRM.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devspaces/new-azureevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevSpaces/Commands.DevSpaces/help/New-AzureRmDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevSpaces/Commands.DevSpaces/help/New-AzureRmDevSpacesController.md
ms.openlocfilehash: 13fea6a0f7c7fda06e171538c92fe52db969fe36
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702950"
---
# <span data-ttu-id="3f2ec-101">New-AzureRmDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="3f2ec-101">New-AzureRmDevSpacesController</span></span>

## <span data-ttu-id="3f2ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f2ec-102">SYNOPSIS</span></span>
<span data-ttu-id="3f2ec-103">새 Azure DevSpaces 컨트롤러를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3f2ec-103">Create a new Azure DevSpaces controller.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f2ec-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3f2ec-104">SYNTAX</span></span>

```
New-AzureRmDevSpacesController [-ResourceGroupName] <String> [-Name] <String>
 [-TargetResourceGroupName] <String> [-TargetClusterName] <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f2ec-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3f2ec-105">DESCRIPTION</span></span>
<span data-ttu-id="3f2ec-106">새 Azure DevSpaces 컨트롤러를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3f2ec-106">Create a new Azure DevSpaces controller.</span></span>

## <span data-ttu-id="3f2ec-107">예제의</span><span class="sxs-lookup"><span data-stu-id="3f2ec-107">EXAMPLES</span></span>

### <span data-ttu-id="3f2ec-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="3f2ec-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -TargetResourceGroupName clusterResourceGroup -TargetClusterName clusterName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="3f2ec-109">Crreate는 리소스 devSpaceResourceGroup 이름 devSpaceName와 함께 DevSpaces 컨트롤러를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f2ec-109">Crreate a DevSpaces controller in resourcegroup devSpaceResourceGroup with a name devSpaceName.</span></span> <span data-ttu-id="3f2ec-110">이 컨트롤러의 대상으로 clusterName 클러스터를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f2ec-110">Use clusterName cluster as a target for this controller.</span></span>

## <span data-ttu-id="3f2ec-111">변수</span><span class="sxs-lookup"><span data-stu-id="3f2ec-111">PARAMETERS</span></span>

### <span data-ttu-id="3f2ec-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3f2ec-112">-AsJob</span></span>
<span data-ttu-id="3f2ec-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="3f2ec-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3f2ec-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f2ec-114">-DefaultProfile</span></span>
<span data-ttu-id="3f2ec-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3f2ec-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f2ec-116">-이름</span><span class="sxs-lookup"><span data-stu-id="3f2ec-116">-Name</span></span>
<span data-ttu-id="3f2ec-117">DevSpaces 컨트롤러 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3f2ec-117">DevSpaces Controller Name.</span></span>

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

### <span data-ttu-id="3f2ec-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f2ec-118">-ResourceGroupName</span></span>
<span data-ttu-id="3f2ec-119">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3f2ec-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="3f2ec-120">태그</span><span class="sxs-lookup"><span data-stu-id="3f2ec-120">-Tag</span></span>
<span data-ttu-id="3f2ec-121">리소스 태그를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="3f2ec-121">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="3f2ec-122">-TargetClusterName</span><span class="sxs-lookup"><span data-stu-id="3f2ec-122">-TargetClusterName</span></span>
<span data-ttu-id="3f2ec-123">대상 클러스터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3f2ec-123">Target Cluster Name.</span></span>

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

### <span data-ttu-id="3f2ec-124">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f2ec-124">-TargetResourceGroupName</span></span>
<span data-ttu-id="3f2ec-125">대상 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3f2ec-125">Target Resource Group Name.</span></span>

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

### <span data-ttu-id="3f2ec-126">-확인</span><span class="sxs-lookup"><span data-stu-id="3f2ec-126">-Confirm</span></span>
<span data-ttu-id="3f2ec-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f2ec-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f2ec-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f2ec-128">-WhatIf</span></span>
<span data-ttu-id="3f2ec-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3f2ec-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f2ec-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3f2ec-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f2ec-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f2ec-131">CommonParameters</span></span>
<span data-ttu-id="3f2ec-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f2ec-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f2ec-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f2ec-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f2ec-134">입력</span><span class="sxs-lookup"><span data-stu-id="3f2ec-134">INPUTS</span></span>

### <span data-ttu-id="3f2ec-135">않아야</span><span class="sxs-lookup"><span data-stu-id="3f2ec-135">None</span></span>

## <span data-ttu-id="3f2ec-136">출력</span><span class="sxs-lookup"><span data-stu-id="3f2ec-136">OUTPUTS</span></span>

### <span data-ttu-id="3f2ec-137">Microsoft. Vspaces. 모델. PSController</span><span class="sxs-lookup"><span data-stu-id="3f2ec-137">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="3f2ec-138">상속자</span><span class="sxs-lookup"><span data-stu-id="3f2ec-138">NOTES</span></span>

## <span data-ttu-id="3f2ec-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3f2ec-139">RELATED LINKS</span></span>
