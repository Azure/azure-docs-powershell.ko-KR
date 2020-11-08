---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: FB5E4ED2-8EF3-462F-A053-7EC82C767E8D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementVirtualNetwork.md
ms.openlocfilehash: c7cf4783c7f374f16a51de9ac4794d5fef441e44
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213762"
---
# <span data-ttu-id="d7693-101">New-AzApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d7693-101">New-AzApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="d7693-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7693-102">SYNOPSIS</span></span>
<span data-ttu-id="d7693-103">PsApiManagementVirtualNetwork의 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d7693-103">Creates an instance of PsApiManagementVirtualNetwork.</span></span>

## <span data-ttu-id="d7693-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d7693-104">SYNTAX</span></span>

```
New-AzApiManagementVirtualNetwork -SubnetResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d7693-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d7693-105">DESCRIPTION</span></span>
<span data-ttu-id="d7693-106">**AzApiManagementVirtualNetwork** Cmdlet은 **PsApiManagementVirtualNetwork** 의 인스턴스를 만드는 도우미 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="d7693-106">The **New-AzApiManagementVirtualNetwork** cmdlet is a helper command to create an instance of **PsApiManagementVirtualNetwork**.</span></span>
<span data-ttu-id="d7693-107">이 명령은 **Set-AzApiManagement** 및 **New-AzApiManagement** cmdlet에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7693-107">This command is used with **Set-AzApiManagement** and **New-AzApiManagement** cmdlet.</span></span>

## <span data-ttu-id="d7693-108">예제의</span><span class="sxs-lookup"><span data-stu-id="d7693-108">EXAMPLES</span></span>

### <span data-ttu-id="d7693-109">예제 1: 가상 네트워크 만들기 및 VNET에 기존 APIM 서비스 업데이트</span><span class="sxs-lookup"><span data-stu-id="d7693-109">Example 1: Create a virtual network and Update an existing APIM service into the VNET</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.Network/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.VpnType = "External"
PS C:\> $apim.VirtualNetwork = $virtualNetwork
PS C:\> Set-AzApiManagement -InputObject $apim
```

<span data-ttu-id="d7693-110">이 예제에서는 가상 네트워크를 만든 다음 **AzApiManagement** cmdlet을 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7693-110">This example creates a virtual network and then calls the **Set-AzApiManagement** cmdlet.</span></span>

### <span data-ttu-id="d7693-111">예제 2: 외부 가상 네트워크에 대 한 API Management 서비스 만들기</span><span class="sxs-lookup"><span data-stu-id="d7693-111">Example 2: Create an API Management service for an external virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="d7693-112">이 예제에서는 mode의 가상 네트워크에 새 APIM 서비스를 만듭니다. `External`</span><span class="sxs-lookup"><span data-stu-id="d7693-112">This example creates a new APIM service into a Virtual Network in `External` mode</span></span>

## <span data-ttu-id="d7693-113">변수</span><span class="sxs-lookup"><span data-stu-id="d7693-113">PARAMETERS</span></span>

### <span data-ttu-id="d7693-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7693-114">-DefaultProfile</span></span>
<span data-ttu-id="d7693-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d7693-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7693-116">-SubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="d7693-116">-SubnetResourceId</span></span>
<span data-ttu-id="d7693-117">가상 네트워크의 서브넷 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7693-117">Specifies the subnet resource ID of the virtual network.</span></span>

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

### <span data-ttu-id="d7693-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7693-118">CommonParameters</span></span>
<span data-ttu-id="d7693-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7693-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7693-120">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d7693-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7693-121">입력</span><span class="sxs-lookup"><span data-stu-id="d7693-121">INPUTS</span></span>

### <span data-ttu-id="d7693-122">않아야</span><span class="sxs-lookup"><span data-stu-id="d7693-122">None</span></span>

## <span data-ttu-id="d7693-123">출력</span><span class="sxs-lookup"><span data-stu-id="d7693-123">OUTPUTS</span></span>

### <span data-ttu-id="d7693-124">ApiManagement. PsApiManagementVirtualNetwork/.</span><span class="sxs-lookup"><span data-stu-id="d7693-124">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="d7693-125">상속자</span><span class="sxs-lookup"><span data-stu-id="d7693-125">NOTES</span></span>

## <span data-ttu-id="d7693-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d7693-126">RELATED LINKS</span></span>

<span data-ttu-id="d7693-127">[Set-AzApiManagement](./Set-AzApiManagement.md) 
 [새로운 AzApiManagement](./New-AzApiManagement.md)</span><span class="sxs-lookup"><span data-stu-id="d7693-127">[Set-AzApiManagement](./Set-AzApiManagement.md)
[New-AzApiManagement](./New-AzApiManagement.md)</span></span>

