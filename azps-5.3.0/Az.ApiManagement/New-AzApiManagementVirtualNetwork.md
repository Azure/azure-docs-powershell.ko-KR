---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: FB5E4ED2-8EF3-462F-A053-7EC82C767E8D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementVirtualNetwork.md
ms.openlocfilehash: c7cf4783c7f374f16a51de9ac4794d5fef441e44
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382292"
---
# <span data-ttu-id="e393f-101">New-AzApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e393f-101">New-AzApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="e393f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e393f-102">SYNOPSIS</span></span>
<span data-ttu-id="e393f-103">PsApiManagementVirtualNetwork의 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e393f-103">Creates an instance of PsApiManagementVirtualNetwork.</span></span>

## <span data-ttu-id="e393f-104">구문</span><span class="sxs-lookup"><span data-stu-id="e393f-104">SYNTAX</span></span>

```
New-AzApiManagementVirtualNetwork -SubnetResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e393f-105">설명</span><span class="sxs-lookup"><span data-stu-id="e393f-105">DESCRIPTION</span></span>
<span data-ttu-id="e393f-106">**New-AzApiManagementVirtualNetwork** cmdlet은 **PsApiManagementVirtualNetwork의** 인스턴스를 만드는 도우미 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="e393f-106">The **New-AzApiManagementVirtualNetwork** cmdlet is a helper command to create an instance of **PsApiManagementVirtualNetwork**.</span></span>
<span data-ttu-id="e393f-107">이 명령은 **Set-AzApiManagement** 및 **New-AzApiManagement** cmdlet과 함께 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="e393f-107">This command is used with **Set-AzApiManagement** and **New-AzApiManagement** cmdlet.</span></span>

## <span data-ttu-id="e393f-108">예제</span><span class="sxs-lookup"><span data-stu-id="e393f-108">EXAMPLES</span></span>

### <span data-ttu-id="e393f-109">예제 1: 가상 네트워크 만들기 및 VNET에 기존 APIM 서비스 업데이트</span><span class="sxs-lookup"><span data-stu-id="e393f-109">Example 1: Create a virtual network and Update an existing APIM service into the VNET</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.Network/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.VpnType = "External"
PS C:\> $apim.VirtualNetwork = $virtualNetwork
PS C:\> Set-AzApiManagement -InputObject $apim
```

<span data-ttu-id="e393f-110">이 예제에서는 가상 네트워크를 만든 다음 **Set-AzApiManagement** cmdlet을 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="e393f-110">This example creates a virtual network and then calls the **Set-AzApiManagement** cmdlet.</span></span>

### <span data-ttu-id="e393f-111">예제 2: 외부 가상 네트워크에 대한 API Management 서비스 만들기</span><span class="sxs-lookup"><span data-stu-id="e393f-111">Example 2: Create an API Management service for an external virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="e393f-112">이 예제에서는 모드에서 Virtual Network에 새 APIM 서비스를 `External` 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e393f-112">This example creates a new APIM service into a Virtual Network in `External` mode</span></span>

## <span data-ttu-id="e393f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e393f-113">PARAMETERS</span></span>

### <span data-ttu-id="e393f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e393f-114">-DefaultProfile</span></span>
<span data-ttu-id="e393f-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e393f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e393f-116">-SubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="e393f-116">-SubnetResourceId</span></span>
<span data-ttu-id="e393f-117">가상 네트워크의 서브넷 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e393f-117">Specifies the subnet resource ID of the virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e393f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e393f-118">CommonParameters</span></span>
<span data-ttu-id="e393f-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e393f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e393f-120">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e393f-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e393f-121">입력</span><span class="sxs-lookup"><span data-stu-id="e393f-121">INPUTS</span></span>

### <span data-ttu-id="e393f-122">없음</span><span class="sxs-lookup"><span data-stu-id="e393f-122">None</span></span>

## <span data-ttu-id="e393f-123">출력</span><span class="sxs-lookup"><span data-stu-id="e393f-123">OUTPUTS</span></span>

### <span data-ttu-id="e393f-124">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e393f-124">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="e393f-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e393f-125">NOTES</span></span>

## <span data-ttu-id="e393f-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e393f-126">RELATED LINKS</span></span>

<span data-ttu-id="e393f-127">[Set-AzApiManagement](./Set-AzApiManagement.md) 
 [New-AzApiManagement](./New-AzApiManagement.md)</span><span class="sxs-lookup"><span data-stu-id="e393f-127">[Set-AzApiManagement](./Set-AzApiManagement.md)
[New-AzApiManagement](./New-AzApiManagement.md)</span></span>

