---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/Remove-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 54468717f979188d31d6ba318556be87c37e50b9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993636"
---
# <span data-ttu-id="8631e-101">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="8631e-101">Remove-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="8631e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8631e-102">SYNOPSIS</span></span>
<span data-ttu-id="8631e-103">주어진 네트워크 인터페이스에서 탭 구성 제거</span><span class="sxs-lookup"><span data-stu-id="8631e-103">Removes a tap configuration from given network interface</span></span>

## <span data-ttu-id="8631e-104">구문</span><span class="sxs-lookup"><span data-stu-id="8631e-104">SYNTAX</span></span>

### <span data-ttu-id="8631e-105">RemoveByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="8631e-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzNetworkInterfaceTapConfig -ResourceGroupName <String> -NetworkInterfaceName <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8631e-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8631e-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzNetworkInterfaceTapConfig -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8631e-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8631e-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzNetworkInterfaceTapConfig -InputObject <PSNetworkInterfaceTapConfiguration> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8631e-108">설명</span><span class="sxs-lookup"><span data-stu-id="8631e-108">DESCRIPTION</span></span>
<span data-ttu-id="8631e-109">**Remove-AzNetworkInterfaceTapConfig** cmdlet은 네트워크 인터페이스 목록에서 Azure 탭 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="8631e-109">The **Remove-AzNetworkInterfaceTapConfig** cmdlet removes an Azure tap configuration from a network interface list.</span></span>

## <span data-ttu-id="8631e-110">예제</span><span class="sxs-lookup"><span data-stu-id="8631e-110">EXAMPLES</span></span>

### <span data-ttu-id="8631e-111">예제 1: 탭 구성 제거</span><span class="sxs-lookup"><span data-stu-id="8631e-111">Example 1: Remove a tap configuration</span></span>
```
PS C:\>Remove-AzNetworkInterfaceTapConfig -Name "TapConfiguration" -NetworkInterfaceName "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="8631e-112">이 명령은 ResourceGroup1 리소스 그룹에서 NetworkInterface1에서 TapConfiguration을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="8631e-112">This command removes the TapConfiguration from NetworkInterface1 in a resource group ResourceGroup1.</span></span>
<span data-ttu-id="8631e-113">Force *매개* 변수를 사용할 수 없습니다. 사용자에게 이 작업을 확인하라는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8631e-113">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="8631e-114">예제 2: 네트워크 인터페이스 제거</span><span class="sxs-lookup"><span data-stu-id="8631e-114">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzNetworkInterfaceTapConfig -Name "TapConfiguration" -NetworkInterfaceName "NetworkInterface1" -ResourceGroup "ResourceGroup1" | Remove-AzNetworkInterfaceTapConfig -Force
```

<span data-ttu-id="8631e-115">이 명령은 ResourceGroup1 리소스 그룹에서 NetworkInterface1에서 TapConfiguration을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="8631e-115">This command removes the TapConfiguration from NetworkInterface1 in a resource group ResourceGroup1.</span></span>
<span data-ttu-id="8631e-116">Force *매개* 변수가 사용되어 있기 때문에 사용자는 확인을 묻는 메시지가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="8631e-116">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="8631e-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="8631e-117">PARAMETERS</span></span>

### <span data-ttu-id="8631e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8631e-118">-DefaultProfile</span></span>
<span data-ttu-id="8631e-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8631e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8631e-120">-Force</span><span class="sxs-lookup"><span data-stu-id="8631e-120">-Force</span></span>
<span data-ttu-id="8631e-121">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8631e-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="8631e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8631e-122">-InputObject</span></span>
<span data-ttu-id="8631e-123">NetworkInterfaceTapConfig를 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="8631e-123">Reference to NetworkInterfaceTapConfig.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8631e-124">-Name</span><span class="sxs-lookup"><span data-stu-id="8631e-124">-Name</span></span>
<span data-ttu-id="8631e-125">가상 네트워크 피어링 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8631e-125">The virtual network peering name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8631e-126">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="8631e-126">-NetworkInterfaceName</span></span>
<span data-ttu-id="8631e-127">가상 네트워크 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8631e-127">The virtual network name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8631e-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8631e-128">-PassThru</span></span>
<span data-ttu-id="8631e-129">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="8631e-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8631e-130">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8631e-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8631e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8631e-131">-ResourceGroupName</span></span>
<span data-ttu-id="8631e-132">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8631e-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8631e-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8631e-133">-ResourceId</span></span>
<span data-ttu-id="8631e-134">NetworkInterfaceTapConfig 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8631e-134">NetworkInterfaceTapConfig resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8631e-135">-확인</span><span class="sxs-lookup"><span data-stu-id="8631e-135">-Confirm</span></span>
<span data-ttu-id="8631e-136">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8631e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8631e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8631e-137">-WhatIf</span></span>
<span data-ttu-id="8631e-138">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="8631e-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8631e-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8631e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8631e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8631e-140">CommonParameters</span></span>
<span data-ttu-id="8631e-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8631e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8631e-142">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="8631e-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8631e-143">입력</span><span class="sxs-lookup"><span data-stu-id="8631e-143">INPUTS</span></span>

### <span data-ttu-id="8631e-144">System.String</span><span class="sxs-lookup"><span data-stu-id="8631e-144">System.String</span></span>

### <span data-ttu-id="8631e-145">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="8631e-145">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="8631e-146">출력</span><span class="sxs-lookup"><span data-stu-id="8631e-146">OUTPUTS</span></span>

### <span data-ttu-id="8631e-147">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="8631e-147">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="8631e-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8631e-148">NOTES</span></span>

## <span data-ttu-id="8631e-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8631e-149">RELATED LINKS</span></span>

[<span data-ttu-id="8631e-150">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="8631e-150">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="8631e-151">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="8631e-151">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="8631e-152">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="8631e-152">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)
