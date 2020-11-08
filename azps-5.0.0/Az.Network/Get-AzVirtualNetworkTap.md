---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkTap.md
ms.openlocfilehash: dc6ca5c41e5f819c8f1db3d0c601b48273e3d78e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215978"
---
# <span data-ttu-id="0c86e-101">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="0c86e-101">Get-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="0c86e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c86e-102">SYNOPSIS</span></span>
<span data-ttu-id="0c86e-103">가상 네트워크 탭을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0c86e-103">Gets a virtual network tap</span></span>

## <span data-ttu-id="0c86e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0c86e-104">SYNTAX</span></span>

### <span data-ttu-id="0c86e-105">ListParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="0c86e-105">ListParameterSet (Default)</span></span>
```
Get-AzVirtualNetworkTap [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c86e-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c86e-106">GetByResourceIdParameterSet</span></span>
```
Get-AzVirtualNetworkTap -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0c86e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="0c86e-107">DESCRIPTION</span></span>
<span data-ttu-id="0c86e-108">**AzVirtualNetworkTap** Cmdlet은 azure 가상 네트워크 탭 또는 리소스 그룹의 azure 가상 네트워크 탭 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0c86e-108">The **Get-AzVirtualNetworkTap** cmdlet gets an Azure virtual network tap or a list of Azure virtual network taps in a resource group.</span></span>

## <span data-ttu-id="0c86e-109">예제의</span><span class="sxs-lookup"><span data-stu-id="0c86e-109">EXAMPLES</span></span>

### <span data-ttu-id="0c86e-110">예제 1: 가상 네트워크 가져오기 탭</span><span class="sxs-lookup"><span data-stu-id="0c86e-110">Example 1: Get a virtual network tap</span></span>
```
PS C:\> Get-AzVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
```

<span data-ttu-id="0c86e-111">이 명령은 "ResourceGroup1"의 지정 된 "VirtualTap1"에 대 한 VirtualNetwork 탭 참조를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0c86e-111">This command gets a VirtualNetwork tap reference for given "VirtualTap1" in "ResourceGroup1".</span></span>

### <span data-ttu-id="0c86e-112">예제 2: 필터링을 사용 하 여 모든 가상 네트워크 탭 가져오기</span><span class="sxs-lookup"><span data-stu-id="0c86e-112">Example 2: Get all virtual network taps using filtering</span></span>
```
PS C:\> Get-AzVirtualNetworkTap -Name "VirtualTap*"
```

<span data-ttu-id="0c86e-113">이 명령은 "VirtualTap"로 시작 하는 모든 VirtualNetwork 탭 참조를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0c86e-113">This command gets all VirtualNetwork tap references that start with "VirtualTap".</span></span>

## <span data-ttu-id="0c86e-114">변수</span><span class="sxs-lookup"><span data-stu-id="0c86e-114">PARAMETERS</span></span>

### <span data-ttu-id="0c86e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c86e-115">-DefaultProfile</span></span>
<span data-ttu-id="0c86e-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0c86e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c86e-117">-이름</span><span class="sxs-lookup"><span data-stu-id="0c86e-117">-Name</span></span>
<span data-ttu-id="0c86e-118">탭의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0c86e-118">The name of the tap.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="0c86e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c86e-119">-ResourceGroupName</span></span>
<span data-ttu-id="0c86e-120">가상 네트워크의 리소스 그룹 이름 탭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c86e-120">The resource group name of the virtual network tap.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="0c86e-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0c86e-121">-ResourceId</span></span>
<span data-ttu-id="0c86e-122">VirtualNetworkTap 리소스의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="0c86e-122">ResourceId of the VirtualNetworkTap resource</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c86e-123">-확인</span><span class="sxs-lookup"><span data-stu-id="0c86e-123">-Confirm</span></span>
<span data-ttu-id="0c86e-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c86e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c86e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c86e-125">-WhatIf</span></span>
<span data-ttu-id="0c86e-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0c86e-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0c86e-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0c86e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c86e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c86e-128">CommonParameters</span></span>
<span data-ttu-id="0c86e-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c86e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c86e-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0c86e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c86e-131">입력</span><span class="sxs-lookup"><span data-stu-id="0c86e-131">INPUTS</span></span>

### <span data-ttu-id="0c86e-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0c86e-132">System.String</span></span>

## <span data-ttu-id="0c86e-133">출력</span><span class="sxs-lookup"><span data-stu-id="0c86e-133">OUTPUTS</span></span>

### <span data-ttu-id="0c86e-134">PSVirtualNetworkTap에 대 한.</span><span class="sxs-lookup"><span data-stu-id="0c86e-134">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="0c86e-135">상속자</span><span class="sxs-lookup"><span data-stu-id="0c86e-135">NOTES</span></span>

## <span data-ttu-id="0c86e-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0c86e-136">RELATED LINKS</span></span>

[<span data-ttu-id="0c86e-137">새로운 AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="0c86e-137">New-AzVirtualNetworkTap</span></span>](./New-AzVirtualNetworkTap.md)

[<span data-ttu-id="0c86e-138">제거-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="0c86e-138">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)

[<span data-ttu-id="0c86e-139">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="0c86e-139">Set-AzVirtualNetworkTap</span></span>](./Set-AzVirtualNetworkTap.md)
