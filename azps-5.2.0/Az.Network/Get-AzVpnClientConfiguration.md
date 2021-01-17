---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientConfiguration.md
ms.openlocfilehash: ba73b61d34e0f6422defb9e9d6f84c22945ec124
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372569"
---
# <span data-ttu-id="fbaca-101">Get-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="fbaca-101">Get-AzVpnClientConfiguration</span></span>

## <span data-ttu-id="fbaca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbaca-102">SYNOPSIS</span></span>
<span data-ttu-id="fbaca-103">사용자가 New-AzVpnClientConfiguration 사용하여 생성된 Vpn 프로필 패키지를 쉽게 다운로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbaca-103">Allows users to easily download the Vpn Profile package that was generated using the New-AzVpnClientConfiguration commandlet.</span></span>

## <span data-ttu-id="fbaca-104">구문</span><span class="sxs-lookup"><span data-stu-id="fbaca-104">SYNTAX</span></span>

```
Get-AzVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbaca-105">설명</span><span class="sxs-lookup"><span data-stu-id="fbaca-105">DESCRIPTION</span></span>
<span data-ttu-id="fbaca-106">이 Get-AzVpnClientConfiguration VPN 클라이언트를 다운로드할 수 있는 URL을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="fbaca-106">The Get-AzVpnClientConfiguration returns the URL where the VPN client can be downloaded from.</span></span>

## <span data-ttu-id="fbaca-107">예제</span><span class="sxs-lookup"><span data-stu-id="fbaca-107">EXAMPLES</span></span>

### <span data-ttu-id="fbaca-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="fbaca-108">Example 1</span></span>
```
PS C:\> New-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -AuthenticationMethod "EAPTLS" -RadiusRootCert "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"

PS C:\> Get-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="fbaca-109">이전에 New-AzVpnClientConfiguration 명령을 사용하여 생성된 VpnClient 프로필을 다운로드하는 URL을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="fbaca-109">Gets the URL to download a VpnClient profile that has been previously generated using the New-AzVpnClientConfiguration command.</span></span>

## <span data-ttu-id="fbaca-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fbaca-110">PARAMETERS</span></span>

### <span data-ttu-id="fbaca-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbaca-111">-DefaultProfile</span></span>
<span data-ttu-id="fbaca-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fbaca-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fbaca-113">-Name</span><span class="sxs-lookup"><span data-stu-id="fbaca-113">-Name</span></span>
<span data-ttu-id="fbaca-114">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fbaca-114">The resource name.</span></span>

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

### <span data-ttu-id="fbaca-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbaca-115">-ResourceGroupName</span></span>
<span data-ttu-id="fbaca-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fbaca-116">The resource group name.</span></span>

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

### <span data-ttu-id="fbaca-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fbaca-117">-Confirm</span></span>
<span data-ttu-id="fbaca-118">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fbaca-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbaca-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbaca-119">-WhatIf</span></span>
<span data-ttu-id="fbaca-120">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="fbaca-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fbaca-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fbaca-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbaca-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbaca-122">CommonParameters</span></span>
<span data-ttu-id="fbaca-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fbaca-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbaca-124">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fbaca-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbaca-125">입력</span><span class="sxs-lookup"><span data-stu-id="fbaca-125">INPUTS</span></span>

### <span data-ttu-id="fbaca-126">System.String</span><span class="sxs-lookup"><span data-stu-id="fbaca-126">System.String</span></span>

## <span data-ttu-id="fbaca-127">출력</span><span class="sxs-lookup"><span data-stu-id="fbaca-127">OUTPUTS</span></span>

### <span data-ttu-id="fbaca-128">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="fbaca-128">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="fbaca-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fbaca-129">NOTES</span></span>

## <span data-ttu-id="fbaca-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fbaca-130">RELATED LINKS</span></span>

[<span data-ttu-id="fbaca-131">New-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="fbaca-131">New-AzVpnClientConfiguration</span></span>](./New-AzVpnClientConfiguration.md)
