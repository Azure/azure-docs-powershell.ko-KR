---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: FB5E4ED2-8EF3-462F-A053-7EC82C767E8D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementVirtualNetwork.md
ms.openlocfilehash: 67020f99129dfa920aa1bbc5e22ac59c16affb32
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869470"
---
# <span data-ttu-id="62132-101">New-AzApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="62132-101">New-AzApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="62132-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62132-102">SYNOPSIS</span></span>
<span data-ttu-id="62132-103">PsApiManagementVirtualNetwork의 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="62132-103">Creates an instance of PsApiManagementVirtualNetwork.</span></span>

## <span data-ttu-id="62132-104">구문과</span><span class="sxs-lookup"><span data-stu-id="62132-104">SYNTAX</span></span>

```
New-AzApiManagementVirtualNetwork -SubnetResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="62132-105">설명은</span><span class="sxs-lookup"><span data-stu-id="62132-105">DESCRIPTION</span></span>
<span data-ttu-id="62132-106">**AzApiManagementVirtualNetwork** Cmdlet은 **PsApiManagementVirtualNetwork** 의 인스턴스를 만드는 도우미 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="62132-106">The **New-AzApiManagementVirtualNetwork** cmdlet is a helper command to create an instance of **PsApiManagementVirtualNetwork**.</span></span>
<span data-ttu-id="62132-107">이 명령은 **AzApiManagementDeployment** cmdlet에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="62132-107">This command is used with **Update-AzApiManagementDeployment** cmdlet.</span></span>

## <span data-ttu-id="62132-108">예제의</span><span class="sxs-lookup"><span data-stu-id="62132-108">EXAMPLES</span></span>

### <span data-ttu-id="62132-109">예제 1: 가상 네트워크 만들기</span><span class="sxs-lookup"><span data-stu-id="62132-109">Example 1: Create a virtual network</span></span>
```
PS C:\>$vnetName = "myvnet"
PS C:\>$subnetName = "default"
PS C:\>$subnet = New-AzVirtualNetworkSubnetConfig -Name $subnetName -AddressPrefix 10.0.1.0/24
PS C:\>$vnet = New-AzvirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroupName -Location $location -AddressPrefix 10.0.0.0/16 -Subnet $subnet

# Create a Virtual Network Object
PS C:\>$virtualNetwork = New-AzApiManagementVirtualNetwork -Location $location -SubnetResourceId $vnet.Subnets[0].Id

# Get the service
PS C:\>$service = Get-AzApiManagement -ResourceGroupName $resourceGroupName -Name $apiManagementName    
PS C:\>$service.VirtualNetwork = $virtualNetwork
PS C:\>$service.VpnType = "External"

# Update the Deployment with Virtual Network
PS C:\>Update-AzApiManagementDeployment -ApiManagement $service
```

<span data-ttu-id="62132-110">이 예제에서는 가상 네트워크를 만든 다음 **AzApiManagementDeployment** cmdlet을 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="62132-110">This example creates a virtual network and then calls the **Update-AzApiManagementDeployment** cmdlet.</span></span>

## <span data-ttu-id="62132-111">변수</span><span class="sxs-lookup"><span data-stu-id="62132-111">PARAMETERS</span></span>

### <span data-ttu-id="62132-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62132-112">-DefaultProfile</span></span>
<span data-ttu-id="62132-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="62132-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62132-114">-SubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="62132-114">-SubnetResourceId</span></span>
<span data-ttu-id="62132-115">가상 네트워크의 서브넷 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="62132-115">Specifies the subnet resource ID of the virtual network.</span></span>

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

### <span data-ttu-id="62132-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62132-116">CommonParameters</span></span>
<span data-ttu-id="62132-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="62132-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62132-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62132-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62132-119">입력</span><span class="sxs-lookup"><span data-stu-id="62132-119">INPUTS</span></span>

### <span data-ttu-id="62132-120">않아야</span><span class="sxs-lookup"><span data-stu-id="62132-120">None</span></span>

## <span data-ttu-id="62132-121">출력</span><span class="sxs-lookup"><span data-stu-id="62132-121">OUTPUTS</span></span>

### <span data-ttu-id="62132-122">ApiManagement. PsApiManagementVirtualNetwork/.</span><span class="sxs-lookup"><span data-stu-id="62132-122">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="62132-123">상속자</span><span class="sxs-lookup"><span data-stu-id="62132-123">NOTES</span></span>

## <span data-ttu-id="62132-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="62132-124">RELATED LINKS</span></span>

[<span data-ttu-id="62132-125">업데이트-AzApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="62132-125">Update-AzApiManagementDeployment</span></span>](./Update-AzApiManagementDeployment.md)

