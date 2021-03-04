---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 1c46cb01a2b30853248ca941cbb61d8b0429fc49
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954555"
---
# <span data-ttu-id="5c627-101">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="5c627-101">Get-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="5c627-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c627-102">SYNOPSIS</span></span>
<span data-ttu-id="5c627-103">탭 구성 리소스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5c627-103">Gets a Tap configuration resource.</span></span>

## <span data-ttu-id="5c627-104">구문</span><span class="sxs-lookup"><span data-stu-id="5c627-104">SYNTAX</span></span>

### <span data-ttu-id="5c627-105">GetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="5c627-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzNetworkInterfaceTapConfig -ResourceGroupName <String> -NetworkInterfaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c627-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c627-106">GetByResourceIdParameterSet</span></span>
```
Get-AzNetworkInterfaceTapConfig -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c627-107">설명</span><span class="sxs-lookup"><span data-stu-id="5c627-107">DESCRIPTION</span></span>
<span data-ttu-id="5c627-108">**Get-AzNetworkInterfaceTapConfig** cmdlet은 리소스 그룹 및 네트워크 인터페이스에서 지정한 리소스 그룹, 네트워크 인터페이스 및 탭 구성 이름 또는 탭 구성 목록을 탭하는 Azure Tap 구성을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="5c627-108">The **Get-AzNetworkInterfaceTapConfig** cmdlet gets an Azure Tap Configuration for a given resource group, network interface and tap configuration name or list of tap configurations in a resource group and network interface.</span></span>

## <span data-ttu-id="5c627-109">예제</span><span class="sxs-lookup"><span data-stu-id="5c627-109">EXAMPLES</span></span>

### <span data-ttu-id="5c627-110">예제 1: 주어진 네트워크 인터페이스에 대한 모든 탭 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5c627-110">Example 1: Get all tap configurations for a given network interface</span></span>
```
PS C:\> Get-AzNetworkInterfaceTapConfig -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName"
```

<span data-ttu-id="5c627-111">이 명령은 주어진 네트워크 인터페이스에 대해 탭 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5c627-111">This command gets tap configurations added for the given network interface.</span></span>

### <span data-ttu-id="5c627-112">예제 2: 주어진 탭 구성을 얻다</span><span class="sxs-lookup"><span data-stu-id="5c627-112">Example 2: Get a given tap configuration</span></span>
```
PS C:\> Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
```

<span data-ttu-id="5c627-113">이 명령은 특정 네트워크 인터페이스에 대해 추가된 특정 탭 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5c627-113">This command gets specific tap configuration added for the given network interface.</span></span>

### <span data-ttu-id="5c627-114">예제 3: 주어진 탭 구성을 얻다</span><span class="sxs-lookup"><span data-stu-id="5c627-114">Example 3: Get a given tap configuration</span></span>
```
PS C:\> Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfig*"
```

<span data-ttu-id="5c627-115">이 명령은 "tapconfig"로 시작하는 이름으로 지정한 네트워크 인터페이스에 대해 탭 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5c627-115">This command gets tap configurations added for the given network interface with name starting with "tapconfig".</span></span>

## <span data-ttu-id="5c627-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="5c627-116">PARAMETERS</span></span>

### <span data-ttu-id="5c627-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c627-117">-DefaultProfile</span></span>
<span data-ttu-id="5c627-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5c627-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c627-119">-Name</span><span class="sxs-lookup"><span data-stu-id="5c627-119">-Name</span></span>
<span data-ttu-id="5c627-120">특정 탭 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5c627-120">Name of the specific tap configuration.</span></span>

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

### <span data-ttu-id="5c627-121">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="5c627-121">-NetworkInterfaceName</span></span>
<span data-ttu-id="5c627-122">네트워크 인터페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5c627-122">The Network Interface name.</span></span>

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

### <span data-ttu-id="5c627-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c627-123">-ResourceGroupName</span></span>
<span data-ttu-id="5c627-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5c627-124">The resource group name.</span></span>

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

### <span data-ttu-id="5c627-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5c627-125">-ResourceId</span></span>
<span data-ttu-id="5c627-126">TapConfiguration 리소스의 ResourceId</span><span class="sxs-lookup"><span data-stu-id="5c627-126">ResourceId of the TapConfiguration resource</span></span>

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

### <span data-ttu-id="5c627-127">-확인</span><span class="sxs-lookup"><span data-stu-id="5c627-127">-Confirm</span></span>
<span data-ttu-id="5c627-128">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5c627-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c627-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c627-129">-WhatIf</span></span>
<span data-ttu-id="5c627-130">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="5c627-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5c627-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5c627-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c627-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c627-132">CommonParameters</span></span>
<span data-ttu-id="5c627-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5c627-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c627-134">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5c627-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c627-135">입력</span><span class="sxs-lookup"><span data-stu-id="5c627-135">INPUTS</span></span>

### <span data-ttu-id="5c627-136">System.String</span><span class="sxs-lookup"><span data-stu-id="5c627-136">System.String</span></span>

## <span data-ttu-id="5c627-137">출력</span><span class="sxs-lookup"><span data-stu-id="5c627-137">OUTPUTS</span></span>

### <span data-ttu-id="5c627-138">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c627-138">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="5c627-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5c627-139">NOTES</span></span>

## <span data-ttu-id="5c627-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5c627-140">RELATED LINKS</span></span>

[<span data-ttu-id="5c627-141">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="5c627-141">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="5c627-142">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="5c627-142">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="5c627-143">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="5c627-143">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)
