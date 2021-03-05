---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9DBD5ADF-C30E-4D1A-A4CB-4D70C21088F3
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewall.md
ms.openlocfilehash: 4be419ab76180174fd6132335822c361008ec872
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993776"
---
# <span data-ttu-id="4fed9-101">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="4fed9-101">Remove-AzFirewall</span></span>

## <span data-ttu-id="4fed9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4fed9-102">SYNOPSIS</span></span>
<span data-ttu-id="4fed9-103">방화벽을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4fed9-103">Remove a Firewall.</span></span>

## <span data-ttu-id="4fed9-104">구문</span><span class="sxs-lookup"><span data-stu-id="4fed9-104">SYNTAX</span></span>

```
Remove-AzFirewall -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fed9-105">설명</span><span class="sxs-lookup"><span data-stu-id="4fed9-105">DESCRIPTION</span></span>
<span data-ttu-id="4fed9-106">**Remove-AzFirewall** cmdlet은 Azure 방화벽을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4fed9-106">The **Remove-AzFirewall** cmdlet removes an Azure Firewall.</span></span>

## <span data-ttu-id="4fed9-107">예제</span><span class="sxs-lookup"><span data-stu-id="4fed9-107">EXAMPLES</span></span>

### <span data-ttu-id="4fed9-108">예제 1: 방화벽 만들기 및 삭제</span><span class="sxs-lookup"><span data-stu-id="4fed9-108">Example 1: Create and delete a Firewall</span></span>
```powershell
New-AzFirewall -Name "azFw" -ResourceGroupName "rgName" -Location centralus 

Remove-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
Confirm
Are you sure you want to remove resource 'azFw'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="4fed9-109">이 예제에서는 방화벽을 만든 다음 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="4fed9-109">This example creates a Firewall and then deletes it.</span></span> <span data-ttu-id="4fed9-110">방화벽을 삭제할 때 프롬프트를 표시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4fed9-110">To suppress the prompt when deleting the Firewall, use the -Force flag.</span></span>

## <span data-ttu-id="4fed9-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="4fed9-111">PARAMETERS</span></span>

### <span data-ttu-id="4fed9-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4fed9-112">-AsJob</span></span>
<span data-ttu-id="4fed9-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="4fed9-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4fed9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fed9-114">-DefaultProfile</span></span>
<span data-ttu-id="4fed9-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4fed9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4fed9-116">-Force</span><span class="sxs-lookup"><span data-stu-id="4fed9-116">-Force</span></span>
<span data-ttu-id="4fed9-117">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="4fed9-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4fed9-118">-Name</span><span class="sxs-lookup"><span data-stu-id="4fed9-118">-Name</span></span>
<span data-ttu-id="4fed9-119">이 cmdlet이 제거하는 방화벽 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4fed9-119">Specifies the name of the firewall that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4fed9-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4fed9-120">-PassThru</span></span>
<span data-ttu-id="4fed9-121">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="4fed9-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4fed9-122">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4fed9-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4fed9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fed9-123">-ResourceGroupName</span></span>
<span data-ttu-id="4fed9-124">이 cmdlet이 제거하는 방화벽을 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4fed9-124">Specifies the name of the resource group that contains the firewall that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4fed9-125">-확인</span><span class="sxs-lookup"><span data-stu-id="4fed9-125">-Confirm</span></span>
<span data-ttu-id="4fed9-126">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4fed9-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fed9-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fed9-127">-WhatIf</span></span>
<span data-ttu-id="4fed9-128">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="4fed9-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fed9-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4fed9-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fed9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fed9-130">CommonParameters</span></span>
<span data-ttu-id="4fed9-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4fed9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fed9-132">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4fed9-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fed9-133">입력</span><span class="sxs-lookup"><span data-stu-id="4fed9-133">INPUTS</span></span>

### <span data-ttu-id="4fed9-134">System.String</span><span class="sxs-lookup"><span data-stu-id="4fed9-134">System.String</span></span>

## <span data-ttu-id="4fed9-135">출력</span><span class="sxs-lookup"><span data-stu-id="4fed9-135">OUTPUTS</span></span>

### <span data-ttu-id="4fed9-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4fed9-136">System.Boolean</span></span>

## <span data-ttu-id="4fed9-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4fed9-137">NOTES</span></span>

## <span data-ttu-id="4fed9-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4fed9-138">RELATED LINKS</span></span>

[<span data-ttu-id="4fed9-139">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="4fed9-139">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="4fed9-140">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="4fed9-140">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="4fed9-141">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="4fed9-141">Set-AzFirewall</span></span>](./Set-AzFirewall.md)
