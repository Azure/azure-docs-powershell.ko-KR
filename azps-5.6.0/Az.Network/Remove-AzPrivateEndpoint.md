---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpoint.md
ms.openlocfilehash: 3e1caeb5dec11188cf824bdcddf2b0de78f707c9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996156"
---
# <span data-ttu-id="ebcda-101">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ebcda-101">Remove-AzPrivateEndpoint</span></span>

## <span data-ttu-id="ebcda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ebcda-102">SYNOPSIS</span></span>
<span data-ttu-id="ebcda-103">개인 엔드포인트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ebcda-103">Removes a private endpoint.</span></span>

## <span data-ttu-id="ebcda-104">구문</span><span class="sxs-lookup"><span data-stu-id="ebcda-104">SYNTAX</span></span>

```
Remove-AzPrivateEndpoint -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ebcda-105">설명</span><span class="sxs-lookup"><span data-stu-id="ebcda-105">DESCRIPTION</span></span>
<span data-ttu-id="ebcda-106">**Remove-AzPrivateEndpoint** cmdlet은 개인 엔드포인트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ebcda-106">The **Remove-AzPrivateEndpoint** cmdlet removes a private endpoint.</span></span> 

## <span data-ttu-id="ebcda-107">예제</span><span class="sxs-lookup"><span data-stu-id="ebcda-107">EXAMPLES</span></span>

### <span data-ttu-id="ebcda-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ebcda-108">Example 1</span></span>
```
Remove-AzPrivateEndpoint -Name MyPrivateEndpoint1 -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="ebcda-109">이 예제에서는 MyPrivateEndpoint1이라는 개인 엔드포인트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ebcda-109">This example remove a private endpoint named MyPrivateEndpoint1.</span></span>

## <span data-ttu-id="ebcda-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ebcda-110">PARAMETERS</span></span>

### <span data-ttu-id="ebcda-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ebcda-111">-AsJob</span></span>
<span data-ttu-id="ebcda-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="ebcda-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ebcda-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebcda-113">-DefaultProfile</span></span>
<span data-ttu-id="ebcda-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ebcda-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ebcda-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ebcda-115">-Force</span></span>
<span data-ttu-id="ebcda-116">리소스를 삭제하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ebcda-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="ebcda-117">-Name</span><span class="sxs-lookup"><span data-stu-id="ebcda-117">-Name</span></span>
<span data-ttu-id="ebcda-118">개인 엔드포인트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ebcda-118">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="ebcda-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ebcda-119">-PassThru</span></span>
<span data-ttu-id="ebcda-120">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ebcda-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ebcda-121">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ebcda-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ebcda-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebcda-122">-ResourceGroupName</span></span>
<span data-ttu-id="ebcda-123">개인 엔드포인트의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ebcda-123">The resource group name of the private endpoint.</span></span>

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

### <span data-ttu-id="ebcda-124">-확인</span><span class="sxs-lookup"><span data-stu-id="ebcda-124">-Confirm</span></span>
<span data-ttu-id="ebcda-125">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ebcda-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebcda-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebcda-126">-WhatIf</span></span>
<span data-ttu-id="ebcda-127">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ebcda-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ebcda-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ebcda-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ebcda-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebcda-129">CommonParameters</span></span>
<span data-ttu-id="ebcda-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ebcda-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebcda-131">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ebcda-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebcda-132">입력</span><span class="sxs-lookup"><span data-stu-id="ebcda-132">INPUTS</span></span>

### <span data-ttu-id="ebcda-133">System.String</span><span class="sxs-lookup"><span data-stu-id="ebcda-133">System.String</span></span>

## <span data-ttu-id="ebcda-134">출력</span><span class="sxs-lookup"><span data-stu-id="ebcda-134">OUTPUTS</span></span>

### <span data-ttu-id="ebcda-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ebcda-135">System.Boolean</span></span>

## <span data-ttu-id="ebcda-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ebcda-136">NOTES</span></span>

## <span data-ttu-id="ebcda-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ebcda-137">RELATED LINKS</span></span>

[<span data-ttu-id="ebcda-138">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ebcda-138">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="ebcda-139">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ebcda-139">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)