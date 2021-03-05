---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 01F56553-1685-43D4-89E6-DDCDF17D1E00
online version: https://docs.microsoft.com/powershell/module/az.network/remove-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityGroup.md
ms.openlocfilehash: 27822e64c697ace3a69e6faf5f291215a2d89935
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993631"
---
# <span data-ttu-id="cb5ad-101">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="cb5ad-101">Remove-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="cb5ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb5ad-102">SYNOPSIS</span></span>
<span data-ttu-id="cb5ad-103">네트워크 보안 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="cb5ad-103">Removes a network security group.</span></span>

## <span data-ttu-id="cb5ad-104">구문</span><span class="sxs-lookup"><span data-stu-id="cb5ad-104">SYNTAX</span></span>

```
Remove-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb5ad-105">설명</span><span class="sxs-lookup"><span data-stu-id="cb5ad-105">DESCRIPTION</span></span>
<span data-ttu-id="cb5ad-106">**Remove-AzNetworkSecurityGroup** cmdlet은 Azure 네트워크 보안 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="cb5ad-106">The **Remove-AzNetworkSecurityGroup** cmdlet removes an Azure network security group.</span></span>

## <span data-ttu-id="cb5ad-107">예제</span><span class="sxs-lookup"><span data-stu-id="cb5ad-107">EXAMPLES</span></span>

### <span data-ttu-id="cb5ad-108">예제 1: 네트워크 보안 그룹 제거</span><span class="sxs-lookup"><span data-stu-id="cb5ad-108">Example 1: Remove a network security group</span></span>
```
PS C:\>Remove-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
```

<span data-ttu-id="cb5ad-109">이 명령은 TestRG라는 리소스 NSG-FrontEnd 그룹에서 보안 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="cb5ad-109">This command removes the security group named NSG-FrontEnd in the resource group named TestRG.</span></span>

## <span data-ttu-id="cb5ad-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="cb5ad-110">PARAMETERS</span></span>

### <span data-ttu-id="cb5ad-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cb5ad-111">-AsJob</span></span>
<span data-ttu-id="cb5ad-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="cb5ad-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cb5ad-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb5ad-113">-DefaultProfile</span></span>
<span data-ttu-id="cb5ad-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cb5ad-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb5ad-115">-Force</span><span class="sxs-lookup"><span data-stu-id="cb5ad-115">-Force</span></span>
<span data-ttu-id="cb5ad-116">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="cb5ad-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cb5ad-117">-Name</span><span class="sxs-lookup"><span data-stu-id="cb5ad-117">-Name</span></span>
<span data-ttu-id="cb5ad-118">이 cmdlet이 제거한 네트워크 보안 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cb5ad-118">Specifies the name of the network security group that this cmdlet removes.</span></span>

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

### <span data-ttu-id="cb5ad-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cb5ad-119">-PassThru</span></span>
<span data-ttu-id="cb5ad-120">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="cb5ad-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cb5ad-121">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cb5ad-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cb5ad-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb5ad-122">-ResourceGroupName</span></span>
<span data-ttu-id="cb5ad-123">이 cmdlet에서 네트워크 보안 그룹을 제거하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cb5ad-123">Specifies the name of a resource group that this cmdlet removes a network security group from.</span></span>

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

### <span data-ttu-id="cb5ad-124">-확인</span><span class="sxs-lookup"><span data-stu-id="cb5ad-124">-Confirm</span></span>
<span data-ttu-id="cb5ad-125">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="cb5ad-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb5ad-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb5ad-126">-WhatIf</span></span>
<span data-ttu-id="cb5ad-127">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="cb5ad-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb5ad-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cb5ad-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb5ad-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb5ad-129">CommonParameters</span></span>
<span data-ttu-id="cb5ad-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cb5ad-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb5ad-131">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cb5ad-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb5ad-132">입력</span><span class="sxs-lookup"><span data-stu-id="cb5ad-132">INPUTS</span></span>

### <span data-ttu-id="cb5ad-133">System.String</span><span class="sxs-lookup"><span data-stu-id="cb5ad-133">System.String</span></span>

## <span data-ttu-id="cb5ad-134">출력</span><span class="sxs-lookup"><span data-stu-id="cb5ad-134">OUTPUTS</span></span>

### <span data-ttu-id="cb5ad-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cb5ad-135">System.Boolean</span></span>

## <span data-ttu-id="cb5ad-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cb5ad-136">NOTES</span></span>

## <span data-ttu-id="cb5ad-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cb5ad-137">RELATED LINKS</span></span>

[<span data-ttu-id="cb5ad-138">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="cb5ad-138">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="cb5ad-139">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="cb5ad-139">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="cb5ad-140">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="cb5ad-140">Set-AzNetworkSecurityGroup</span></span>](./Set-AzNetworkSecurityGroup.md)


