---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateLinkService.md
ms.openlocfilehash: e06a29422a7abed55dbf1e8508c8715a36cf7d76
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996137"
---
# <span data-ttu-id="e8292-101">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e8292-101">Remove-AzPrivateLinkService</span></span>

## <span data-ttu-id="e8292-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8292-102">SYNOPSIS</span></span>
<span data-ttu-id="e8292-103">개인 링크 서비스 제거</span><span class="sxs-lookup"><span data-stu-id="e8292-103">Removes a private link service</span></span>

## <span data-ttu-id="e8292-104">구문</span><span class="sxs-lookup"><span data-stu-id="e8292-104">SYNTAX</span></span>

```
Remove-AzPrivateLinkService -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8292-105">설명</span><span class="sxs-lookup"><span data-stu-id="e8292-105">DESCRIPTION</span></span>
<span data-ttu-id="e8292-106">**Remove-AzPrivateLinkService** cmdlet은 개인 링크 서비스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e8292-106">The **Remove-AzPrivateLinkService** cmdlet removes a private link service</span></span>

## <span data-ttu-id="e8292-107">예제</span><span class="sxs-lookup"><span data-stu-id="e8292-107">EXAMPLES</span></span>

### <span data-ttu-id="e8292-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="e8292-108">Example 1</span></span>
```
Remove-AzPrivateLinkService -ResourceGroupName TestResourceGroup -Name TestPrivateLinkService
```

<span data-ttu-id="e8292-109">이 예제에서는 TestPrivateLinkService라는 개인 링크 서비스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e8292-109">This example removes a private link service named TestPrivateLinkService.</span></span>

## <span data-ttu-id="e8292-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e8292-110">PARAMETERS</span></span>

### <span data-ttu-id="e8292-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e8292-111">-AsJob</span></span>
<span data-ttu-id="e8292-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e8292-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e8292-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8292-113">-DefaultProfile</span></span>
<span data-ttu-id="e8292-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e8292-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8292-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e8292-115">-Force</span></span>
<span data-ttu-id="e8292-116">리소스를 삭제하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e8292-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="e8292-117">-Name</span><span class="sxs-lookup"><span data-stu-id="e8292-117">-Name</span></span>
<span data-ttu-id="e8292-118">서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e8292-118">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8292-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e8292-119">-PassThru</span></span>
<span data-ttu-id="e8292-120">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="e8292-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e8292-121">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e8292-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e8292-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8292-122">-ResourceGroupName</span></span>
<span data-ttu-id="e8292-123">개인 링크 서비스의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e8292-123">The resource group name of the private link service.</span></span>

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

### <span data-ttu-id="e8292-124">-확인</span><span class="sxs-lookup"><span data-stu-id="e8292-124">-Confirm</span></span>
<span data-ttu-id="e8292-125">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8292-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8292-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8292-126">-WhatIf</span></span>
<span data-ttu-id="e8292-127">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e8292-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8292-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e8292-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8292-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8292-129">CommonParameters</span></span>
<span data-ttu-id="e8292-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e8292-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8292-131">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e8292-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8292-132">입력</span><span class="sxs-lookup"><span data-stu-id="e8292-132">INPUTS</span></span>

### <span data-ttu-id="e8292-133">System.String</span><span class="sxs-lookup"><span data-stu-id="e8292-133">System.String</span></span>

## <span data-ttu-id="e8292-134">출력</span><span class="sxs-lookup"><span data-stu-id="e8292-134">OUTPUTS</span></span>

### <span data-ttu-id="e8292-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e8292-135">System.Boolean</span></span>

## <span data-ttu-id="e8292-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e8292-136">NOTES</span></span>

## <span data-ttu-id="e8292-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e8292-137">RELATED LINKS</span></span>

[<span data-ttu-id="e8292-138">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e8292-138">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="e8292-139">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e8292-139">New-AzPrivateLinkService</span></span>](./New-AzPrivateLinkService.md)