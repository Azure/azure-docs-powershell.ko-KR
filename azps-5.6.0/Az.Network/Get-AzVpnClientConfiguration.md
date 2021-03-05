---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientConfiguration.md
ms.openlocfilehash: 03ed4fe9ad6e8b2e7c5af0b24e29c351a2b776f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010427"
---
# <span data-ttu-id="bf31e-101">Get-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="bf31e-101">Get-AzVpnClientConfiguration</span></span>

## <span data-ttu-id="bf31e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf31e-102">SYNOPSIS</span></span>
<span data-ttu-id="bf31e-103">사용자가 명령줄을 사용하여 생성된 Vpn Profile 패키지를 New-AzVpnClientConfiguration 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bf31e-103">Allows users to easily download the Vpn Profile package that was generated using the New-AzVpnClientConfiguration commandlet.</span></span>

## <span data-ttu-id="bf31e-104">구문</span><span class="sxs-lookup"><span data-stu-id="bf31e-104">SYNTAX</span></span>

```
Get-AzVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf31e-105">설명</span><span class="sxs-lookup"><span data-stu-id="bf31e-105">DESCRIPTION</span></span>
<span data-ttu-id="bf31e-106">이 Get-AzVpnClientConfiguration VPN 클라이언트를 다운로드할 수 있는 URL을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="bf31e-106">The Get-AzVpnClientConfiguration returns the URL where the VPN client can be downloaded from.</span></span>

## <span data-ttu-id="bf31e-107">예제</span><span class="sxs-lookup"><span data-stu-id="bf31e-107">EXAMPLES</span></span>

### <span data-ttu-id="bf31e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="bf31e-108">Example 1</span></span>
```
PS C:\> New-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -AuthenticationMethod "EAPTLS" -RadiusRootCert "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"

PS C:\> Get-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="bf31e-109">이전에 New-AzVpnClientConfiguration VPNClient 프로필을 다운로드하는 URL을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bf31e-109">Gets the URL to download a VpnClient profile that has been previously generated using the New-AzVpnClientConfiguration command.</span></span>

## <span data-ttu-id="bf31e-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="bf31e-110">PARAMETERS</span></span>

### <span data-ttu-id="bf31e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf31e-111">-DefaultProfile</span></span>
<span data-ttu-id="bf31e-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bf31e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf31e-113">-Name</span><span class="sxs-lookup"><span data-stu-id="bf31e-113">-Name</span></span>
<span data-ttu-id="bf31e-114">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bf31e-114">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf31e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf31e-115">-ResourceGroupName</span></span>
<span data-ttu-id="bf31e-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bf31e-116">The resource group name.</span></span>

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

### <span data-ttu-id="bf31e-117">-확인</span><span class="sxs-lookup"><span data-stu-id="bf31e-117">-Confirm</span></span>
<span data-ttu-id="bf31e-118">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bf31e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf31e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf31e-119">-WhatIf</span></span>
<span data-ttu-id="bf31e-120">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="bf31e-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bf31e-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bf31e-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf31e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf31e-122">CommonParameters</span></span>
<span data-ttu-id="bf31e-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bf31e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf31e-124">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bf31e-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf31e-125">입력</span><span class="sxs-lookup"><span data-stu-id="bf31e-125">INPUTS</span></span>

### <span data-ttu-id="bf31e-126">System.String</span><span class="sxs-lookup"><span data-stu-id="bf31e-126">System.String</span></span>

## <span data-ttu-id="bf31e-127">출력</span><span class="sxs-lookup"><span data-stu-id="bf31e-127">OUTPUTS</span></span>

### <span data-ttu-id="bf31e-128">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="bf31e-128">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="bf31e-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bf31e-129">NOTES</span></span>

## <span data-ttu-id="bf31e-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bf31e-130">RELATED LINKS</span></span>

[<span data-ttu-id="bf31e-131">New-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="bf31e-131">New-AzVpnClientConfiguration</span></span>](./New-AzVpnClientConfiguration.md)
