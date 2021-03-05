---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 31B0FBEF-366A-41AF-9182-2EB087019F36
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancer.md
ms.openlocfilehash: efe24ad1feae60ed71bd65206c52cfbf0b27df18
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996296"
---
# <span data-ttu-id="f1d9e-101">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f1d9e-101">Remove-AzLoadBalancer</span></span>

## <span data-ttu-id="f1d9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1d9e-102">SYNOPSIS</span></span>
<span data-ttu-id="f1d9e-103">부하 균형 조정기를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d9e-103">Removes a load balancer.</span></span>

## <span data-ttu-id="f1d9e-104">구문</span><span class="sxs-lookup"><span data-stu-id="f1d9e-104">SYNTAX</span></span>

```
Remove-AzLoadBalancer -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1d9e-105">설명</span><span class="sxs-lookup"><span data-stu-id="f1d9e-105">DESCRIPTION</span></span>
<span data-ttu-id="f1d9e-106">**Remove-AzLoadBalancer** cmdlet은 Azure 부하 분산기를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d9e-106">The **Remove-AzLoadBalancer** cmdlet removes an Azure load balancer.</span></span>

## <span data-ttu-id="f1d9e-107">예제</span><span class="sxs-lookup"><span data-stu-id="f1d9e-107">EXAMPLES</span></span>

### <span data-ttu-id="f1d9e-108">예제 1: 부하 균형 조정기 제거</span><span class="sxs-lookup"><span data-stu-id="f1d9e-108">Example 1: Remove a load balancer</span></span>
```
PS C:\>Remove-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="f1d9e-109">이 명령은 MyResourceGroup이라는 리소스 그룹에서 MyLoadBalancer라는 부하 분산기 를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d9e-109">This command deletes a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="f1d9e-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f1d9e-110">PARAMETERS</span></span>

### <span data-ttu-id="f1d9e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f1d9e-111">-AsJob</span></span>
<span data-ttu-id="f1d9e-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="f1d9e-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f1d9e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1d9e-113">-DefaultProfile</span></span>
<span data-ttu-id="f1d9e-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f1d9e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1d9e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f1d9e-115">-Force</span></span>
<span data-ttu-id="f1d9e-116">리소스가 할당되어 있는지 여부에 관계없이 이 cmdlet이 부하 균형 조정기를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d9e-116">Indicates that this cmdlet removes the load balancer regardless of whether resources are assigned to it.</span></span>

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

### <span data-ttu-id="f1d9e-117">-Name</span><span class="sxs-lookup"><span data-stu-id="f1d9e-117">-Name</span></span>
<span data-ttu-id="f1d9e-118">제거할 부하 균형 조정기 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d9e-118">Specifies the name of the load balancer to remove.</span></span>

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

### <span data-ttu-id="f1d9e-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f1d9e-119">-PassThru</span></span>
<span data-ttu-id="f1d9e-120">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d9e-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f1d9e-121">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f1d9e-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f1d9e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1d9e-122">-ResourceGroupName</span></span>
<span data-ttu-id="f1d9e-123">제거할 부하 균형 조정기를 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d9e-123">Specifies the name of the resource group that contains the load balancer to remove.</span></span>

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

### <span data-ttu-id="f1d9e-124">-확인</span><span class="sxs-lookup"><span data-stu-id="f1d9e-124">-Confirm</span></span>
<span data-ttu-id="f1d9e-125">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f1d9e-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1d9e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1d9e-126">-WhatIf</span></span>
<span data-ttu-id="f1d9e-127">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="f1d9e-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1d9e-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f1d9e-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1d9e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1d9e-129">CommonParameters</span></span>
<span data-ttu-id="f1d9e-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d9e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1d9e-131">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f1d9e-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1d9e-132">입력</span><span class="sxs-lookup"><span data-stu-id="f1d9e-132">INPUTS</span></span>

### <span data-ttu-id="f1d9e-133">System.String</span><span class="sxs-lookup"><span data-stu-id="f1d9e-133">System.String</span></span>

## <span data-ttu-id="f1d9e-134">출력</span><span class="sxs-lookup"><span data-stu-id="f1d9e-134">OUTPUTS</span></span>

### <span data-ttu-id="f1d9e-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f1d9e-135">System.Boolean</span></span>

## <span data-ttu-id="f1d9e-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f1d9e-136">NOTES</span></span>

## <span data-ttu-id="f1d9e-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f1d9e-137">RELATED LINKS</span></span>

[<span data-ttu-id="f1d9e-138">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f1d9e-138">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="f1d9e-139">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f1d9e-139">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="f1d9e-140">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f1d9e-140">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)


