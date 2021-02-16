---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: fa4c6db39de9f0d27fa80c4ee09e4decb319e2aa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179873"
---
# <span data-ttu-id="53763-101">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="53763-101">Get-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="53763-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53763-102">SYNOPSIS</span></span>
<span data-ttu-id="53763-103">탭 구성 리소스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="53763-103">Gets a Tap configuration resource.</span></span>

## <span data-ttu-id="53763-104">구문</span><span class="sxs-lookup"><span data-stu-id="53763-104">SYNTAX</span></span>

### <span data-ttu-id="53763-105">GetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="53763-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzNetworkInterfaceTapConfig -ResourceGroupName <String> -NetworkInterfaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53763-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="53763-106">GetByResourceIdParameterSet</span></span>
```
Get-AzNetworkInterfaceTapConfig -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53763-107">설명</span><span class="sxs-lookup"><span data-stu-id="53763-107">DESCRIPTION</span></span>
<span data-ttu-id="53763-108">**Get-AzNetworkInterfaceTapConfig** cmdlet은 주어진 리소스 그룹, 네트워크 인터페이스에 대한 Azure Tap 구성을, 리소스 그룹 및 네트워크 인터페이스에서 구성 이름 또는 탭 구성 목록을 탭합니다.</span><span class="sxs-lookup"><span data-stu-id="53763-108">The **Get-AzNetworkInterfaceTapConfig** cmdlet gets an Azure Tap Configuration for a given resource group, network interface and tap configuration name or list of tap configurations in a resource group and network interface.</span></span>

## <span data-ttu-id="53763-109">예제</span><span class="sxs-lookup"><span data-stu-id="53763-109">EXAMPLES</span></span>

### <span data-ttu-id="53763-110">예제 1: 주어진 네트워크 인터페이스에 대한 모든 탭 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="53763-110">Example 1: Get all tap configurations for a given network interface</span></span>
```
PS C:\> Get-AzNetworkInterfaceTapConfig -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName"
```

<span data-ttu-id="53763-111">이 명령은 주어진 네트워크 인터페이스에 대해 추가된 탭 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="53763-111">This command gets tap configurations added for the given network interface.</span></span>

### <span data-ttu-id="53763-112">예제 2: 주어진 탭 구성을 얻게</span><span class="sxs-lookup"><span data-stu-id="53763-112">Example 2: Get a given tap configuration</span></span>
```
PS C:\> Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
```

<span data-ttu-id="53763-113">이 명령은 주어진 네트워크 인터페이스에 대해 추가된 특정 탭 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="53763-113">This command gets specific tap configuration added for the given network interface.</span></span>

### <span data-ttu-id="53763-114">예제 3: 주어진 탭 구성을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="53763-114">Example 3: Get a given tap configuration</span></span>
```
PS C:\> Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfig*"
```

<span data-ttu-id="53763-115">이 명령은 "tapconfig"로 시작하는 이름으로 지정한 네트워크 인터페이스에 대해 추가된 탭 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="53763-115">This command gets tap configurations added for the given network interface with name starting with "tapconfig".</span></span>

## <span data-ttu-id="53763-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53763-116">PARAMETERS</span></span>

### <span data-ttu-id="53763-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53763-117">-DefaultProfile</span></span>
<span data-ttu-id="53763-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="53763-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53763-119">-Name</span><span class="sxs-lookup"><span data-stu-id="53763-119">-Name</span></span>
<span data-ttu-id="53763-120">특정 탭 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="53763-120">Name of the specific tap configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="53763-121">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="53763-121">-NetworkInterfaceName</span></span>
<span data-ttu-id="53763-122">네트워크 인터페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="53763-122">The Network Interface name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53763-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53763-123">-ResourceGroupName</span></span>
<span data-ttu-id="53763-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="53763-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53763-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="53763-125">-ResourceId</span></span>
<span data-ttu-id="53763-126">TapConfiguration 리소스의 ResourceId</span><span class="sxs-lookup"><span data-stu-id="53763-126">ResourceId of the TapConfiguration resource</span></span>

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

### <span data-ttu-id="53763-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="53763-127">-Confirm</span></span>
<span data-ttu-id="53763-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="53763-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53763-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53763-129">-WhatIf</span></span>
<span data-ttu-id="53763-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="53763-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="53763-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="53763-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53763-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53763-132">CommonParameters</span></span>
<span data-ttu-id="53763-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="53763-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53763-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="53763-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53763-135">입력</span><span class="sxs-lookup"><span data-stu-id="53763-135">INPUTS</span></span>

### <span data-ttu-id="53763-136">System.String</span><span class="sxs-lookup"><span data-stu-id="53763-136">System.String</span></span>

## <span data-ttu-id="53763-137">출력</span><span class="sxs-lookup"><span data-stu-id="53763-137">OUTPUTS</span></span>

### <span data-ttu-id="53763-138">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="53763-138">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="53763-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="53763-139">NOTES</span></span>

## <span data-ttu-id="53763-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="53763-140">RELATED LINKS</span></span>

[<span data-ttu-id="53763-141">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="53763-141">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="53763-142">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="53763-142">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="53763-143">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="53763-143">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)
