---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 31B0FBEF-366A-41AF-9182-2EB087019F36
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancer.md
ms.openlocfilehash: 271033c39e049a423a15228968ad20c985b57036
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193505"
---
# <span data-ttu-id="fb408-101">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fb408-101">Remove-AzLoadBalancer</span></span>

## <span data-ttu-id="fb408-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb408-102">SYNOPSIS</span></span>
<span data-ttu-id="fb408-103">부하 균형 조정기를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="fb408-103">Removes a load balancer.</span></span>

## <span data-ttu-id="fb408-104">구문</span><span class="sxs-lookup"><span data-stu-id="fb408-104">SYNTAX</span></span>

```
Remove-AzLoadBalancer -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb408-105">설명</span><span class="sxs-lookup"><span data-stu-id="fb408-105">DESCRIPTION</span></span>
<span data-ttu-id="fb408-106">**Remove-AzLoadBalancer** cmdlet은 Azure Load Balancer를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="fb408-106">The **Remove-AzLoadBalancer** cmdlet removes an Azure load balancer.</span></span>

## <span data-ttu-id="fb408-107">예제</span><span class="sxs-lookup"><span data-stu-id="fb408-107">EXAMPLES</span></span>

### <span data-ttu-id="fb408-108">예제 1: 부하 균형 조정기 제거</span><span class="sxs-lookup"><span data-stu-id="fb408-108">Example 1: Remove a load balancer</span></span>
```
PS C:\>Remove-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="fb408-109">이 명령은 MyResourceGroup이라는 리소스 그룹에서 MyLoadBalancer라는 부하 분산 파일을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="fb408-109">This command deletes a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="fb408-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fb408-110">PARAMETERS</span></span>

### <span data-ttu-id="fb408-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fb408-111">-AsJob</span></span>
<span data-ttu-id="fb408-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="fb408-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fb408-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb408-113">-DefaultProfile</span></span>
<span data-ttu-id="fb408-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fb408-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb408-115">-Force</span><span class="sxs-lookup"><span data-stu-id="fb408-115">-Force</span></span>
<span data-ttu-id="fb408-116">이 cmdlet은 리소스가 할당되어 있는지 여부에 관계없이 부하 균형 조정기를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="fb408-116">Indicates that this cmdlet removes the load balancer regardless of whether resources are assigned to it.</span></span>

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

### <span data-ttu-id="fb408-117">-Name</span><span class="sxs-lookup"><span data-stu-id="fb408-117">-Name</span></span>
<span data-ttu-id="fb408-118">제거할 부하 균형 조정기 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fb408-118">Specifies the name of the load balancer to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb408-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fb408-119">-PassThru</span></span>
<span data-ttu-id="fb408-120">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="fb408-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fb408-121">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fb408-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fb408-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb408-122">-ResourceGroupName</span></span>
<span data-ttu-id="fb408-123">제거할 부하 균형 조정기를 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fb408-123">Specifies the name of the resource group that contains the load balancer to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb408-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fb408-124">-Confirm</span></span>
<span data-ttu-id="fb408-125">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fb408-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb408-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb408-126">-WhatIf</span></span>
<span data-ttu-id="fb408-127">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="fb408-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb408-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fb408-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb408-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb408-129">CommonParameters</span></span>
<span data-ttu-id="fb408-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fb408-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb408-131">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="fb408-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb408-132">입력</span><span class="sxs-lookup"><span data-stu-id="fb408-132">INPUTS</span></span>

### <span data-ttu-id="fb408-133">System.String</span><span class="sxs-lookup"><span data-stu-id="fb408-133">System.String</span></span>

## <span data-ttu-id="fb408-134">출력</span><span class="sxs-lookup"><span data-stu-id="fb408-134">OUTPUTS</span></span>

### <span data-ttu-id="fb408-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fb408-135">System.Boolean</span></span>

## <span data-ttu-id="fb408-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fb408-136">NOTES</span></span>

## <span data-ttu-id="fb408-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fb408-137">RELATED LINKS</span></span>

[<span data-ttu-id="fb408-138">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fb408-138">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="fb408-139">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fb408-139">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="fb408-140">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fb408-140">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)


