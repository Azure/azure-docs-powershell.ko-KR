---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateLinkService.md
ms.openlocfilehash: 4b95610996aad93144ccaa749c41319cf513ff7f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369251"
---
# <span data-ttu-id="ddd5e-101">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ddd5e-101">Remove-AzPrivateLinkService</span></span>

## <span data-ttu-id="ddd5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddd5e-102">SYNOPSIS</span></span>
<span data-ttu-id="ddd5e-103">개인 링크 서비스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ddd5e-103">Removes a private link service</span></span>

## <span data-ttu-id="ddd5e-104">구문</span><span class="sxs-lookup"><span data-stu-id="ddd5e-104">SYNTAX</span></span>

```
Remove-AzPrivateLinkService -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddd5e-105">설명</span><span class="sxs-lookup"><span data-stu-id="ddd5e-105">DESCRIPTION</span></span>
<span data-ttu-id="ddd5e-106">**Remove-AzPrivateLinkService** cmdlet은 개인 링크 서비스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ddd5e-106">The **Remove-AzPrivateLinkService** cmdlet removes a private link service</span></span>

## <span data-ttu-id="ddd5e-107">예제</span><span class="sxs-lookup"><span data-stu-id="ddd5e-107">EXAMPLES</span></span>

### <span data-ttu-id="ddd5e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ddd5e-108">Example 1</span></span>
```
Remove-AzPrivateLinkService -ResourceGroupName TestResourceGroup -Name TestPrivateLinkService
```

<span data-ttu-id="ddd5e-109">이 예제에서는 TestPrivateLinkService라는 개인 링크 서비스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ddd5e-109">This example removes a private link service named TestPrivateLinkService.</span></span>

## <span data-ttu-id="ddd5e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ddd5e-110">PARAMETERS</span></span>

### <span data-ttu-id="ddd5e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ddd5e-111">-AsJob</span></span>
<span data-ttu-id="ddd5e-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="ddd5e-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ddd5e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddd5e-113">-DefaultProfile</span></span>
<span data-ttu-id="ddd5e-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ddd5e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddd5e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ddd5e-115">-Force</span></span>
<span data-ttu-id="ddd5e-116">리소스를 삭제하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ddd5e-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="ddd5e-117">-Name</span><span class="sxs-lookup"><span data-stu-id="ddd5e-117">-Name</span></span>
<span data-ttu-id="ddd5e-118">서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ddd5e-118">The name of the service.</span></span>

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

### <span data-ttu-id="ddd5e-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ddd5e-119">-PassThru</span></span>
<span data-ttu-id="ddd5e-120">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ddd5e-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ddd5e-121">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ddd5e-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ddd5e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddd5e-122">-ResourceGroupName</span></span>
<span data-ttu-id="ddd5e-123">개인 링크 서비스의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ddd5e-123">The resource group name of the private link service.</span></span>

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

### <span data-ttu-id="ddd5e-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ddd5e-124">-Confirm</span></span>
<span data-ttu-id="ddd5e-125">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ddd5e-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddd5e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddd5e-126">-WhatIf</span></span>
<span data-ttu-id="ddd5e-127">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ddd5e-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddd5e-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ddd5e-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddd5e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddd5e-129">CommonParameters</span></span>
<span data-ttu-id="ddd5e-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ddd5e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddd5e-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ddd5e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddd5e-132">입력</span><span class="sxs-lookup"><span data-stu-id="ddd5e-132">INPUTS</span></span>

### <span data-ttu-id="ddd5e-133">System.String</span><span class="sxs-lookup"><span data-stu-id="ddd5e-133">System.String</span></span>

## <span data-ttu-id="ddd5e-134">출력</span><span class="sxs-lookup"><span data-stu-id="ddd5e-134">OUTPUTS</span></span>

### <span data-ttu-id="ddd5e-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ddd5e-135">System.Boolean</span></span>

## <span data-ttu-id="ddd5e-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ddd5e-136">NOTES</span></span>

## <span data-ttu-id="ddd5e-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ddd5e-137">RELATED LINKS</span></span>

[<span data-ttu-id="ddd5e-138">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ddd5e-138">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="ddd5e-139">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ddd5e-139">New-AzPrivateLinkService</span></span>](./New-AzPrivateLinkService.md)