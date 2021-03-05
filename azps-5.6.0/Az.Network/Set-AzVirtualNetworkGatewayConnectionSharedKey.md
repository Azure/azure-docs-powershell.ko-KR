---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 78BADAF3-6001-4A25-A74D-F6B50079FCB4
online version: https://docs.microsoft.com/powershell/module/az.network/set-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 2c32263d52f8e260c67395484b2a9a2e3e479ecb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973648"
---
# <span data-ttu-id="f9889-101">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="f9889-101">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="f9889-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9889-102">SYNOPSIS</span></span>
<span data-ttu-id="f9889-103">가상 네트워크 게이트웨이 연결의 공유 키를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="f9889-103">Configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="f9889-104">구문</span><span class="sxs-lookup"><span data-stu-id="f9889-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -Value <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9889-105">설명</span><span class="sxs-lookup"><span data-stu-id="f9889-105">DESCRIPTION</span></span>
<span data-ttu-id="f9889-106">**Set-AzVirtualNetworkGatewayConnectionSharedKey** cmdlet은 가상 네트워크 게이트웨이 연결의 공유 키를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="f9889-106">The **Set-AzVirtualNetworkGatewayConnectionSharedKey** cmdlet configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="f9889-107">예제</span><span class="sxs-lookup"><span data-stu-id="f9889-107">EXAMPLES</span></span>

### <span data-ttu-id="f9889-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="f9889-108">Example 1</span></span>
```powershell
PS C:\Users\alzam> Set-AzVirtualNetworkGatewayConnectionSharedKey -ResourceGroupName VPNGatewayV3 -Name VNet1toVNet2 -Value abcd1234

Confirm
Are you sure you want to overwrite resource 'VNet1toVNet2'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
abcd1234
```

## <span data-ttu-id="f9889-109">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f9889-109">PARAMETERS</span></span>

### <span data-ttu-id="f9889-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9889-110">-DefaultProfile</span></span>
<span data-ttu-id="f9889-111">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f9889-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9889-112">-Force</span><span class="sxs-lookup"><span data-stu-id="f9889-112">-Force</span></span>
<span data-ttu-id="f9889-113">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="f9889-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f9889-114">-Name</span><span class="sxs-lookup"><span data-stu-id="f9889-114">-Name</span></span>
<span data-ttu-id="f9889-115">가상 네트워크 게이트웨이 공유 키의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f9889-115">Specifies the name of the virtual network gateway shared key.</span></span>

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

### <span data-ttu-id="f9889-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9889-116">-ResourceGroupName</span></span>
<span data-ttu-id="f9889-117">가상 네트워크 게이트웨이가 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f9889-117">Specifies the name of the resource group that the virtual network gateway belongs to</span></span>

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

### <span data-ttu-id="f9889-118">-Value</span><span class="sxs-lookup"><span data-stu-id="f9889-118">-Value</span></span>
<span data-ttu-id="f9889-119">공유 키의 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f9889-119">Specifies the value of the shared key.</span></span>

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

### <span data-ttu-id="f9889-120">-확인</span><span class="sxs-lookup"><span data-stu-id="f9889-120">-Confirm</span></span>
<span data-ttu-id="f9889-121">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9889-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9889-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9889-122">-WhatIf</span></span>
<span data-ttu-id="f9889-123">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="f9889-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9889-124">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f9889-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9889-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9889-125">CommonParameters</span></span>
<span data-ttu-id="f9889-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f9889-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9889-127">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f9889-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9889-128">입력</span><span class="sxs-lookup"><span data-stu-id="f9889-128">INPUTS</span></span>

### <span data-ttu-id="f9889-129">System.String</span><span class="sxs-lookup"><span data-stu-id="f9889-129">System.String</span></span>

## <span data-ttu-id="f9889-130">출력</span><span class="sxs-lookup"><span data-stu-id="f9889-130">OUTPUTS</span></span>

### <span data-ttu-id="f9889-131">System.String</span><span class="sxs-lookup"><span data-stu-id="f9889-131">System.String</span></span>

## <span data-ttu-id="f9889-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f9889-132">NOTES</span></span>

## <span data-ttu-id="f9889-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f9889-133">RELATED LINKS</span></span>

[<span data-ttu-id="f9889-134">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="f9889-134">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="f9889-135">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="f9889-135">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzVirtualNetworkGatewayConnectionSharedKey.md)
