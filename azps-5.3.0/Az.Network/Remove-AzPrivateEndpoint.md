---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpoint.md
ms.openlocfilehash: 716606214bcd23bd51286fa3a7a0e4f8c0c4ff70
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98496635"
---
# <span data-ttu-id="d3e18-101">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="d3e18-101">Remove-AzPrivateEndpoint</span></span>

## <span data-ttu-id="d3e18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3e18-102">SYNOPSIS</span></span>
<span data-ttu-id="d3e18-103">개인 엔드포인트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d3e18-103">Removes a private endpoint.</span></span>

## <span data-ttu-id="d3e18-104">구문</span><span class="sxs-lookup"><span data-stu-id="d3e18-104">SYNTAX</span></span>

```
Remove-AzPrivateEndpoint -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3e18-105">설명</span><span class="sxs-lookup"><span data-stu-id="d3e18-105">DESCRIPTION</span></span>
<span data-ttu-id="d3e18-106">**Remove-AzPrivateEndpoint** cmdlet은 개인 엔드포인트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d3e18-106">The **Remove-AzPrivateEndpoint** cmdlet removes a private endpoint.</span></span> 

## <span data-ttu-id="d3e18-107">예제</span><span class="sxs-lookup"><span data-stu-id="d3e18-107">EXAMPLES</span></span>

### <span data-ttu-id="d3e18-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="d3e18-108">Example 1</span></span>
```
Remove-AzPrivateEndpoint -Name MyPrivateEndpoint1 -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="d3e18-109">이 예제에서는 MyPrivateEndpoint1이라는 개인 엔드포인트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d3e18-109">This example remove a private endpoint named MyPrivateEndpoint1.</span></span>

## <span data-ttu-id="d3e18-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3e18-110">PARAMETERS</span></span>

### <span data-ttu-id="d3e18-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d3e18-111">-AsJob</span></span>
<span data-ttu-id="d3e18-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="d3e18-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d3e18-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3e18-113">-DefaultProfile</span></span>
<span data-ttu-id="d3e18-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d3e18-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3e18-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d3e18-115">-Force</span></span>
<span data-ttu-id="d3e18-116">리소스를 삭제하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d3e18-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="d3e18-117">-Name</span><span class="sxs-lookup"><span data-stu-id="d3e18-117">-Name</span></span>
<span data-ttu-id="d3e18-118">개인 엔드포인트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d3e18-118">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="d3e18-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d3e18-119">-PassThru</span></span>
<span data-ttu-id="d3e18-120">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="d3e18-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d3e18-121">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d3e18-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d3e18-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3e18-122">-ResourceGroupName</span></span>
<span data-ttu-id="d3e18-123">개인 엔드포인트의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d3e18-123">The resource group name of the private endpoint.</span></span>

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

### <span data-ttu-id="d3e18-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d3e18-124">-Confirm</span></span>
<span data-ttu-id="d3e18-125">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3e18-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3e18-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3e18-126">-WhatIf</span></span>
<span data-ttu-id="d3e18-127">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d3e18-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3e18-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d3e18-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3e18-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3e18-129">CommonParameters</span></span>
<span data-ttu-id="d3e18-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d3e18-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3e18-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d3e18-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3e18-132">입력</span><span class="sxs-lookup"><span data-stu-id="d3e18-132">INPUTS</span></span>

### <span data-ttu-id="d3e18-133">System.String</span><span class="sxs-lookup"><span data-stu-id="d3e18-133">System.String</span></span>

## <span data-ttu-id="d3e18-134">출력</span><span class="sxs-lookup"><span data-stu-id="d3e18-134">OUTPUTS</span></span>

### <span data-ttu-id="d3e18-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d3e18-135">System.Boolean</span></span>

## <span data-ttu-id="d3e18-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d3e18-136">NOTES</span></span>

## <span data-ttu-id="d3e18-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d3e18-137">RELATED LINKS</span></span>

[<span data-ttu-id="d3e18-138">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="d3e18-138">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="d3e18-139">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="d3e18-139">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)