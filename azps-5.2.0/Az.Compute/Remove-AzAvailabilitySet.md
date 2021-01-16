---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7320B832-50FD-48AE-9089-445318F3B08A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzAvailabilitySet.md
ms.openlocfilehash: 15ecd8c0e22438016ea0f589cf798ecbcb65188f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330117"
---
# <span data-ttu-id="64b96-101">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="64b96-101">Remove-AzAvailabilitySet</span></span>

## <span data-ttu-id="64b96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64b96-102">SYNOPSIS</span></span>
<span data-ttu-id="64b96-103">Azure에서 가용성 집합을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="64b96-103">Removes an availability set from Azure.</span></span>

## <span data-ttu-id="64b96-104">구문</span><span class="sxs-lookup"><span data-stu-id="64b96-104">SYNTAX</span></span>

```
Remove-AzAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64b96-105">설명</span><span class="sxs-lookup"><span data-stu-id="64b96-105">DESCRIPTION</span></span>
<span data-ttu-id="64b96-106">**Remove-AzAvailabilitySet** cmdlet은 Azure에서 가용성 집합을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="64b96-106">The **Remove-AzAvailabilitySet** cmdlet removes an availability set from Azure.</span></span>

## <span data-ttu-id="64b96-107">예제</span><span class="sxs-lookup"><span data-stu-id="64b96-107">EXAMPLES</span></span>

### <span data-ttu-id="64b96-108">예제 1: 가용성 집합 제거</span><span class="sxs-lookup"><span data-stu-id="64b96-108">Example 1: Remove an availability set</span></span>
```
PS C:\> Remove-AzAvailabilitySet -Name "AvailabilitySet03" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="64b96-109">이 명령은 ResourceGroup11이라는 리소스 그룹에서 AvailabilitySet03이라는 가용성 집합을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="64b96-109">This command removes an availability set named AvailabilitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="64b96-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="64b96-110">PARAMETERS</span></span>

### <span data-ttu-id="64b96-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="64b96-111">-AsJob</span></span>
<span data-ttu-id="64b96-112">백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="64b96-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="64b96-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64b96-113">-DefaultProfile</span></span>
<span data-ttu-id="64b96-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="64b96-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64b96-115">-Force</span><span class="sxs-lookup"><span data-stu-id="64b96-115">-Force</span></span>
<span data-ttu-id="64b96-116">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="64b96-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64b96-117">-Name</span><span class="sxs-lookup"><span data-stu-id="64b96-117">-Name</span></span>
<span data-ttu-id="64b96-118">가용성 집합 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="64b96-118">The availability set name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64b96-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64b96-119">-ResourceGroupName</span></span>
<span data-ttu-id="64b96-120">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="64b96-120">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64b96-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="64b96-121">-Confirm</span></span>
<span data-ttu-id="64b96-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="64b96-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64b96-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64b96-123">-WhatIf</span></span>
<span data-ttu-id="64b96-124">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="64b96-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64b96-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="64b96-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64b96-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64b96-126">CommonParameters</span></span>
<span data-ttu-id="64b96-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="64b96-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64b96-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="64b96-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64b96-129">입력</span><span class="sxs-lookup"><span data-stu-id="64b96-129">INPUTS</span></span>

### <span data-ttu-id="64b96-130">System.String</span><span class="sxs-lookup"><span data-stu-id="64b96-130">System.String</span></span>

## <span data-ttu-id="64b96-131">출력</span><span class="sxs-lookup"><span data-stu-id="64b96-131">OUTPUTS</span></span>

### <span data-ttu-id="64b96-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="64b96-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="64b96-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="64b96-133">NOTES</span></span>

## <span data-ttu-id="64b96-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="64b96-134">RELATED LINKS</span></span>

[<span data-ttu-id="64b96-135">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="64b96-135">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="64b96-136">New-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="64b96-136">New-AzAvailabilitySet</span></span>](./New-AzAvailabilitySet.md)


