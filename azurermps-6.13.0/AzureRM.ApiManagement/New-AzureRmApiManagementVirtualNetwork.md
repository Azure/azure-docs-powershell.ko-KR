---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: FB5E4ED2-8EF3-462F-A053-7EC82C767E8D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementVirtualNetwork.md
ms.openlocfilehash: abfcbec55ba3f53986a63a8c0964320c10fc91ec
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533479"
---
# <span data-ttu-id="5a82d-101">New-AzureRmApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5a82d-101">New-AzureRmApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="5a82d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a82d-102">SYNOPSIS</span></span>
<span data-ttu-id="5a82d-103">PsApiManagementVirtualNetwork의 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5a82d-103">Creates an instance of PsApiManagementVirtualNetwork.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a82d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5a82d-104">SYNTAX</span></span>

```
New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a82d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5a82d-105">DESCRIPTION</span></span>
<span data-ttu-id="5a82d-106">**AzureRmApiManagementVirtualNetwork** Cmdlet은 **PsApiManagementVirtualNetwork** 의 인스턴스를 만드는 도우미 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="5a82d-106">The **New-AzureRmApiManagementVirtualNetwork** cmdlet is a helper command to create an instance of **PsApiManagementVirtualNetwork**.</span></span>
<span data-ttu-id="5a82d-107">이 명령은 **AzureRmApiManagementDeployment** cmdlet에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5a82d-107">This command is used with **Update-AzureRmApiManagementDeployment** cmdlet.</span></span>

## <span data-ttu-id="5a82d-108">예제의</span><span class="sxs-lookup"><span data-stu-id="5a82d-108">EXAMPLES</span></span>

### <span data-ttu-id="5a82d-109">예제 1: 가상 네트워크 만들기</span><span class="sxs-lookup"><span data-stu-id="5a82d-109">Example 1: Create a virtual network</span></span>
```
PS C:\>$vnetName = "myvnet"
PS C:\>$subnetName = "default"
PS C:\>$subnet = New-AzureRmVirtualNetworkSubnetConfig -Name $subnetName -AddressPrefix 10.0.1.0/24
PS C:\>$vnet = New-AzureRmvirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroupName -Location $location -AddressPrefix 10.0.0.0/16 -Subnet $subnet

# Create a Virtual Network Object
PS C:\>$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location $location -SubnetResourceId $vnet.Subnets[0].Id

# Get the service
PS C:\>$service = Get-AzureRmApiManagement -ResourceGroupName $resourceGroupName -Name $apiManagementName    
PS C:\>$service.VirtualNetwork = $virtualNetwork
PS C:\>$service.VpnType = "External"

# Update the Deployment with Virtual Network
PS C:\>Update-AzureRmApiManagementDeployment -ApiManagement $service
```

<span data-ttu-id="5a82d-110">이 예제에서는 가상 네트워크를 만든 다음 **AzureRmApiManagementDeployment** cmdlet을 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a82d-110">This example creates a virtual network and then calls the **Update-AzureRmApiManagementDeployment** cmdlet.</span></span>

## <span data-ttu-id="5a82d-111">변수</span><span class="sxs-lookup"><span data-stu-id="5a82d-111">PARAMETERS</span></span>

### <span data-ttu-id="5a82d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a82d-112">-DefaultProfile</span></span>
<span data-ttu-id="5a82d-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5a82d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a82d-114">-위치</span><span class="sxs-lookup"><span data-stu-id="5a82d-114">-Location</span></span>
<span data-ttu-id="5a82d-115">Api Management 서비스에 대해 지원 되는 지역에서의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a82d-115">Specifies the location amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="5a82d-116">유효한 위치를 얻으려면 cmdlet Get-AzureRmResourceProvider ProviderNamespace "ApiManagement" |을 (를) 사용 하세요. 여기서 {$ _. ResourceTypes [0]. ResourceTypeName-eq "서비스"} | Select-Object 위치</span><span class="sxs-lookup"><span data-stu-id="5a82d-116">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="5a82d-117">-SubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="5a82d-117">-SubnetResourceId</span></span>
<span data-ttu-id="5a82d-118">가상 네트워크의 서브넷 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a82d-118">Specifies the subnet resource ID of the virtual network.</span></span>

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

### <span data-ttu-id="5a82d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a82d-119">CommonParameters</span></span>
<span data-ttu-id="5a82d-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a82d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a82d-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a82d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a82d-122">입력</span><span class="sxs-lookup"><span data-stu-id="5a82d-122">INPUTS</span></span>

### <span data-ttu-id="5a82d-123">않아야</span><span class="sxs-lookup"><span data-stu-id="5a82d-123">None</span></span>

## <span data-ttu-id="5a82d-124">출력</span><span class="sxs-lookup"><span data-stu-id="5a82d-124">OUTPUTS</span></span>

### <span data-ttu-id="5a82d-125">ApiManagement. PsApiManagementVirtualNetwork/.</span><span class="sxs-lookup"><span data-stu-id="5a82d-125">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="5a82d-126">상속자</span><span class="sxs-lookup"><span data-stu-id="5a82d-126">NOTES</span></span>

## <span data-ttu-id="5a82d-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5a82d-127">RELATED LINKS</span></span>

[<span data-ttu-id="5a82d-128">업데이트-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="5a82d-128">Update-AzureRmApiManagementDeployment</span></span>](./Update-AzureRmApiManagementDeployment.md)
