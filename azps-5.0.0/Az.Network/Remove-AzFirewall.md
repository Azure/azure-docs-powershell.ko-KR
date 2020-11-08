---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9DBD5ADF-C30E-4D1A-A4CB-4D70C21088F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewall.md
ms.openlocfilehash: 52d2907769ac59a9c71fccef6baf08cc4d13bae8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226355"
---
# <span data-ttu-id="7195e-101">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="7195e-101">Remove-AzFirewall</span></span>

## <span data-ttu-id="7195e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7195e-102">SYNOPSIS</span></span>
<span data-ttu-id="7195e-103">방화벽을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7195e-103">Remove a Firewall.</span></span>

## <span data-ttu-id="7195e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7195e-104">SYNTAX</span></span>

```
Remove-AzFirewall -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7195e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7195e-105">DESCRIPTION</span></span>
<span data-ttu-id="7195e-106">**AzFirewall** Cmdlet은 Azure 방화벽을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7195e-106">The **Remove-AzFirewall** cmdlet removes an Azure Firewall.</span></span>

## <span data-ttu-id="7195e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7195e-107">EXAMPLES</span></span>

### <span data-ttu-id="7195e-108">예제 1: 방화벽 만들기 및 삭제</span><span class="sxs-lookup"><span data-stu-id="7195e-108">Example 1: Create and delete a Firewall</span></span>
```powershell
New-AzFirewall -Name "azFw" -ResourceGroupName "rgName" -Location centralus 

Remove-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
Confirm
Are you sure you want to remove resource 'azFw'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="7195e-109">이 예제에서는 방화벽을 만든 다음 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="7195e-109">This example creates a Firewall and then deletes it.</span></span> <span data-ttu-id="7195e-110">방화벽을 삭제할 때 메시지가 표시 되지 않도록 하려면-Force 플래그를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7195e-110">To suppress the prompt when deleting the Firewall, use the -Force flag.</span></span>

## <span data-ttu-id="7195e-111">변수</span><span class="sxs-lookup"><span data-stu-id="7195e-111">PARAMETERS</span></span>

### <span data-ttu-id="7195e-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7195e-112">-AsJob</span></span>
<span data-ttu-id="7195e-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="7195e-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7195e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7195e-114">-DefaultProfile</span></span>
<span data-ttu-id="7195e-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7195e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7195e-116">-Force</span><span class="sxs-lookup"><span data-stu-id="7195e-116">-Force</span></span>
<span data-ttu-id="7195e-117">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="7195e-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7195e-118">-이름</span><span class="sxs-lookup"><span data-stu-id="7195e-118">-Name</span></span>
<span data-ttu-id="7195e-119">이 cmdlet이 제거 하는 방화벽의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7195e-119">Specifies the name of the firewall that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7195e-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7195e-120">-PassThru</span></span>
<span data-ttu-id="7195e-121">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7195e-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7195e-122">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7195e-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7195e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7195e-123">-ResourceGroupName</span></span>
<span data-ttu-id="7195e-124">이 cmdlet이 제거 하는 방화벽을 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7195e-124">Specifies the name of the resource group that contains the firewall that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7195e-125">-확인</span><span class="sxs-lookup"><span data-stu-id="7195e-125">-Confirm</span></span>
<span data-ttu-id="7195e-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7195e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7195e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7195e-127">-WhatIf</span></span>
<span data-ttu-id="7195e-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7195e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7195e-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7195e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7195e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7195e-130">CommonParameters</span></span>
<span data-ttu-id="7195e-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7195e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7195e-132">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7195e-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7195e-133">입력</span><span class="sxs-lookup"><span data-stu-id="7195e-133">INPUTS</span></span>

### <span data-ttu-id="7195e-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7195e-134">System.String</span></span>

## <span data-ttu-id="7195e-135">출력</span><span class="sxs-lookup"><span data-stu-id="7195e-135">OUTPUTS</span></span>

### <span data-ttu-id="7195e-136">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="7195e-136">System.Boolean</span></span>

## <span data-ttu-id="7195e-137">상속자</span><span class="sxs-lookup"><span data-stu-id="7195e-137">NOTES</span></span>

## <span data-ttu-id="7195e-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7195e-138">RELATED LINKS</span></span>

[<span data-ttu-id="7195e-139">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="7195e-139">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="7195e-140">새로운 AzFirewall</span><span class="sxs-lookup"><span data-stu-id="7195e-140">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="7195e-141">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="7195e-141">Set-AzFirewall</span></span>](./Set-AzFirewall.md)
