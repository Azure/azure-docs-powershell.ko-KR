---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: FDA33633-EB2E-4095-8498-DF8910F1D434
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteTable.md
ms.openlocfilehash: 8c899d975669404045aa40bee45ad287a26f8749
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193460"
---
# <span data-ttu-id="c1e4d-101">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="c1e4d-101">Remove-AzRouteTable</span></span>

## <span data-ttu-id="c1e4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1e4d-102">SYNOPSIS</span></span>
<span data-ttu-id="c1e4d-103">경로 테이블을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c1e4d-103">Removes a route table.</span></span>

## <span data-ttu-id="c1e4d-104">구문</span><span class="sxs-lookup"><span data-stu-id="c1e4d-104">SYNTAX</span></span>

```
Remove-AzRouteTable -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1e4d-105">설명</span><span class="sxs-lookup"><span data-stu-id="c1e4d-105">DESCRIPTION</span></span>
<span data-ttu-id="c1e4d-106">**Remove-AzRouteTable** cmdlet은 Azure 경로 테이블을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c1e4d-106">The **Remove-AzRouteTable** cmdlet removes an Azure route table.</span></span>

## <span data-ttu-id="c1e4d-107">예제</span><span class="sxs-lookup"><span data-stu-id="c1e4d-107">EXAMPLES</span></span>

### <span data-ttu-id="c1e4d-108">예제 1: 경로 테이블 제거</span><span class="sxs-lookup"><span data-stu-id="c1e4d-108">Example 1: Remove a route table</span></span>
```
PS C:\>Remove-AzRouteTable -ResourceGroupName "ResourceGroup11 -Name "RouteTable01"
Confirm
Are you sure you want to remove resource 'RouteTable01'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="c1e4d-109">이 명령은 ResourceGroup11이라는 리소스 그룹에서 RouteTable01이라는 경로 테이블을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c1e4d-109">This command removes the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>
<span data-ttu-id="c1e4d-110">cmdlet은 테이블을 제거하기 전에 확인을 요청합니다.</span><span class="sxs-lookup"><span data-stu-id="c1e4d-110">The cmdlet prompts you for confirmation before it removes the table.</span></span>

## <span data-ttu-id="c1e4d-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c1e4d-111">PARAMETERS</span></span>

### <span data-ttu-id="c1e4d-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c1e4d-112">-AsJob</span></span>
<span data-ttu-id="c1e4d-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="c1e4d-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c1e4d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1e4d-114">-DefaultProfile</span></span>
<span data-ttu-id="c1e4d-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c1e4d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1e4d-116">-Force</span><span class="sxs-lookup"><span data-stu-id="c1e4d-116">-Force</span></span>
<span data-ttu-id="c1e4d-117">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="c1e4d-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c1e4d-118">-Name</span><span class="sxs-lookup"><span data-stu-id="c1e4d-118">-Name</span></span>
<span data-ttu-id="c1e4d-119">이 cmdlet이 제거하는 경로 테이블의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c1e4d-119">Specifies the name of the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c1e4d-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c1e4d-120">-PassThru</span></span>
<span data-ttu-id="c1e4d-121">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="c1e4d-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c1e4d-122">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c1e4d-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c1e4d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1e4d-123">-ResourceGroupName</span></span>
<span data-ttu-id="c1e4d-124">이 cmdlet에서 제거하는 경로 테이블을 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c1e4d-124">Specifies the name of the resource group that contains the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c1e4d-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c1e4d-125">-Confirm</span></span>
<span data-ttu-id="c1e4d-126">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c1e4d-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1e4d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1e4d-127">-WhatIf</span></span>
<span data-ttu-id="c1e4d-128">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c1e4d-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1e4d-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c1e4d-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1e4d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1e4d-130">CommonParameters</span></span>
<span data-ttu-id="c1e4d-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c1e4d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1e4d-132">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c1e4d-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1e4d-133">입력</span><span class="sxs-lookup"><span data-stu-id="c1e4d-133">INPUTS</span></span>

### <span data-ttu-id="c1e4d-134">System.String</span><span class="sxs-lookup"><span data-stu-id="c1e4d-134">System.String</span></span>

## <span data-ttu-id="c1e4d-135">출력</span><span class="sxs-lookup"><span data-stu-id="c1e4d-135">OUTPUTS</span></span>

### <span data-ttu-id="c1e4d-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c1e4d-136">System.Boolean</span></span>

## <span data-ttu-id="c1e4d-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c1e4d-137">NOTES</span></span>

## <span data-ttu-id="c1e4d-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c1e4d-138">RELATED LINKS</span></span>

[<span data-ttu-id="c1e4d-139">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="c1e4d-139">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="c1e4d-140">New-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="c1e4d-140">New-AzRouteTable</span></span>](./New-AzRouteTable.md)

[<span data-ttu-id="c1e4d-141">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="c1e4d-141">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)


